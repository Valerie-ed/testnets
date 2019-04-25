# Create Validator

### What is a Validator?

Validators are responsible for committing new blocks to the blockchain through voting.
A validator's stake is slashed if they become unavailable or sign blocks at the same height.
Please read about Sentry Node Architecture to protect your node from DDOS attacks and to ensure high-availability.

### Create Your Validator

> Before setting up your validator node, make sure you'v already created an wallet.
>
> And got some GARD using faucet command

Your `gardvalconspub` can be used to create a new validator by staking GARD. You can find your validator pubkey by running:

```bash
hashgard tendermint show-validator
```

To create your validator, just use the following command:

```bash
hashgardcli stake create-validator \
    --from=${your_wallet_name}  \
	  --pubkey=$(hashgard tendermint show-validator) \
	  --commission-max-change-rate=0.01 \
	  --commission-rate=0.1 \
	  --commission-max-rate=0.2 \
	  --amount=40gard \
	  --moniker=${your_node_name}  \
	  --min-self-delegation=10 \
	  --chain-id=sif-4000 \
	  --fees=2gard \
	  --output=json \
	  --indent
```

> commission parameters
>
> The commission-max-change-rate is used to measure % point change over the commission-rate.
> E.g. 1% to 2% is a 100% rate increase, but only 1 percentage point.

> Min-self-delegation
>
> Min-self-delegation is a stritly positive integer that represents the minimum amount of self-delegated voting power your validator must always have.
> A min-self-delegation of 10 means your validator will never have a self-delegation lower than 10gard

### Check Validators

You can get details of your validator:

```bash
hashgardcli stake validator ${validator-address} --trust-node
```

You can confirm that you are in the validator set by using gardplorer:
[http://www.gardplorer.io/validator](http://www.gardplorer.io/validator)
