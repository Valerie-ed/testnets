# Hashgard 通胀与 staking 方案

## 方案目标

- 通过鼓励用户成为节点，构建更加健壮的去中心化网络
- 鼓励用户更多的通过投票参与社区的重大问题治理
-  鼓励用户抵押所持 GARD ，获得抵押收益，减少流通率，提升币价

## 当前staking经济的分析

Hashgard 是采用 Cosmos SDK 开发，其共识机制 Tendermint 与其他公链有一定差别，因此本方案只针对机遇 Cosmosm SDK 开发并已上线主网的 Cosmos 与 Iris 两条公链进行分析。

### cosmos 通胀与 Staking 方案

#### 默认配置（初始配置）

- Minter:

  - Inflation: 年度通胀率，13%
  - AnnualProvisions: 预期的年度激励总量, 0

- Params:
  - MintDenom: 增发币种，uatom
  - InflationRateChange: 通胀率变化范围，13%
  - InflationMax: 最大通胀率，20%
  - InflationMin: 最小通胀率，7%
  - GoalBonded: 目标抵押率，67%
  - BlocksPerYear: 每年新增区块数，60*60 8766 / 5 (假设每5秒1个区块)



#### 计算步骤

增发量的计算在 BeginBlock 阶段进行

1. 获取总币量和抵押率

每个区块开始时，获得当前区块高度的 TotalTokens 和 BondedRatio

2. 计算当前块的通胀率

每个预设周期都会重新计算目标年度通胀率，通胀率也会受一定变化率的影响(正向或负向),具体取决于与目标抵押率(67%)的剧里。最大的通胀变化范围定义为每年13%，所以年度通胀率的上限为7%到20%
$$
NextInflationRate = Inflation + (1 - bondedRatio/GoalBonded) * InflationRateChange
$$

判断当结果大于 InflationMax ， 会强制等于  InflationMax，小于InflationMin则强制等于 InflationMin



#### 3.计算当前块的年度激励总量

根据当前的总供应量和通胀率计算:

$$
NextAnnualProvisions = NextInflationRate * TotalSupply
$$

#### 4.计算当前区块应获得的激励量



$$BlockProvision = NextAnnualProvisions / BlocksPerYear$$

BlockProvision 即为该区块的增发量

### 分析

1. 实际出块时间多于5s的话，实际通胀率会减小。
1. 每次计算增量是当前总量为基础，实际通胀率又会增大。
1. 两个区块抵押率相同，通胀率可以是不同的。
1. 只能通过升级的方式更改方案，无法通过gov模块，进行升级



### IRIS通胀公式

#### 默认配置（初始配置）

- Minter:

  - LastUpdate: 更新时间，0

  - MintDenom: 增发币种, iris-atto

  - InflationBase: 计算通胀时的总量，$$2*(10^9)*(10^{18}) iris-atto$$



- Params:

  - Inflation: 通胀率，4%

  - blocksPerYear: 每年新增区块数，$$60*60 *8766 / 5$$

####  计算步骤

1.计算当前块的年度激励总量

$$NextAnnualProvisions = Inflation * InflationBase$$



2.计算当前区块应获得的激励量

BlockProvision = NextAnnualProvisions / blocksPerYear

#### 分析

1. 每个区块增发率和计算总量一样，所以增发的数量是固定的。实际年度通胀率只受实际出块数量影响
2. 增发公式由gov模块决定，这意味着社区可以根据需要，通过链上治理的方式，改变增发方案，因此具备更多的灵活性



![image-20190513162626080](https://ws1.sinaimg.cn/large/006tNc79gy1g2zrpzgbdjj31bd0u077j.jpg)

### Hashgard 通胀公式

#### 默认配置（初始配置）

- Minter:
  - LastUpdate: 更新时间，0
  - MintDenom: 增发币种, iris-atto
  - InflationBase: 计算通胀时的总量，$$2*(10^9)*(10^{18}) iris-atto$$



- Params:
  - Inflation: 通胀率，8%
  - blocksPerYear: 每年新增区块数，$$60*60 *8766 / 5$$

#### 计算步骤

1.计算当前块的年度激励总量

$$NextAnnualProvisions = Inflation * InflationBase$$



2.计算当前区块应获得的激励量

BlockProvision = NextAnnualProvisions / blocksPerYear

亿

