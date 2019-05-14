# How to participate in the Genesis process



## Step 1: Create your own account 

First, if you don't have an account or forget your password, you'll need to create an account for yourself as the validator.

Please create a wallet according to
```
hashgardcli keys add -h
```
## Step 2: Initialize your node

```bash
hashgard init --moniker=${your_node_name} 
```

> Note: Skip this step if you have already done the initialization.



## Step 3: Add account information to genesis.json 

```bash
hashgard add-genesis-account ${your_wallet_name} 100000000gard 
```

> Note: name only supports ASCII characters. Using Unicode characters will make your node inaccessible.



## Step 4: Add account information to genesis.json 

```bash
hashgard gentx \
    --name=${your_wallet_name} \
    --amount=100000000gard \
    --ip=${validator_ip}
```

> Note: name only supports ASCII characters. Using Unicode characters will make your node inaccessible.

The transaction will be generated in the following directory: ~/.hashgard/config/gentx 

Create a CreateValidator transaction and sign the transaction with the validator account just created. The default commission is:

- Delegation amount: 100000000 gard 

- Commission rate: 0.1 

- Commission max rate: 0.2 

- Commission max change rate: 0.01




## Step 5: Submit your gentx.json

Submit your `gentx-node-ID.json` by creating a pull request. 

After the team has collected all the gen-tx transactions, we will release the `genesis` file. 

You can then download the final `genesis` file and launch a node.