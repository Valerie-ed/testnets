# Hashgard Testnet Guide

This guide is intended for someone who is looking to setup a Hashgard Node to join Hashgard Testnet.

> This document is written for testnet sif-5001, make sure your chain-id is sif-5001

> \${} for variables, you should replace it with your own value

## Run a Hashgard Node

### Step 1：Installation

You can install Hashgard according to [Hashgard Installation Guide](installation.md)。

### Step 2: Create Your Wallet

```plain
hashgardcli keys add ${your_wallet_name}
```

Remember to write your seed phrase in a safe place after you created a wallet.

It is the only way to recover your account if you ever forget your password.

Check your wallets:

```plain
hashgardcli keys list
```

### Step 3: Configure the Client

Configure the default node to connect to:

```plain
hashgardcli config chain-id sif-5001
hashgardcli config trust-node true
```

Format the output:

```plain
hashgardcli config indent true
hashgardcli config output json
```

### Step 4：Initialize the Node and Download Config Files

#### 4.1: Initialization

```bash
hashgard init \
  --chain-id=sif-5001 \
  --moniker=${your_node_name}
```

If you want to run a Validator Node in Genisis period,
you can generate a JSON file and submit it to us according to [Guide of Genesis](../docs/genesis.md).

Or you can update your node to Validator Node later by sending a `create_validator` transaction.

#### 4.2: Download Genesis and Config Files

Go to the hashgard config directory, replace the genesis and config files with the downloaded testnet sif-5001 files.

```bash
cd $HASHGARDHOME/config/
rm genesis.json
rm config.toml
curl -O https://raw.githubusercontent.com/hashgard/testnets/master/sif/sif-6000/config/config.toml
curl -O https://raw.githubusercontent.com/hashgard/testnets/master/sif/sif-6000/config/genesis.json
```

The default value of \$HASHGARDHOME in the above command is `~/.hashgard`，

#### 4.3: Modify the Config File

Edit `$HASHGARDHOME/config/config.toml`, set the value of `moniker` and `external_address`:

```toml
# A custom human readable name for this node
moniker = "${your_node_name}"
external_address = "${your_public_ip}:26656"
```

### Step 5: Run the Node

Run it with command:

```bash
hashgard start > hashgard.log &
```

Check the status of your node:

```bash
hashgardcli status
```

You will see the output below if it runs well:

```json
{
  "node_info": {
    "protocol_version": {
      "p2p": "5",
      "block": "8",
      "app": "0"
    },
    "id": "b783ac2b41da096ddc3a26c2a39e3b0c1ea49d9e",
    "listen_addr": "127.0.0.190:26656",
    "network": "hashgard",
    "version": "0.27.0",
    "channels": "4020212223303800",
    "moniker": "hashgard_test",
    "other": {
      "tx_index": "on",
      "rpc_address": "tcp://0.0.0.0:26657"
    }
  },
  "sync_info": {
    "latest_block_hash": "AFB6261A76DCC6176FF5248B3B5BEDEEBD38B6DA3D18AD21ADD4054AEDEED016",
    "latest_app_hash": "1DEAF3D71AD735F4E375439DAFD96C8934E944D8D32F6179F55C5470E219D132",
    "latest_block_height": "77280",
    "latest_block_time": "2018-12-24T07:13:53.787154732Z",
    "catching_up": false
  },
  "validator_info": {
    "address": "5959DF3D28F601407A98D0B038174E288ED45BD7",
    "pub_key": {
      "type": "tendermint/PubKeyEd25519",
      "value": "wYrxKp7cw14eQiqzfGBggEV474ZA2lc35AieJM5SM6Y="
    },
    "voting_power": "950"
  }
}
```

The value of `catching_up` is `false`, means the block data of your node has been synchronized with the testnet, or it is synchronizing.

Congratulations! You've started a Hashgard Node and joined Hashgard Testnet successfully。

Now you've complished the first incentive task, you could try more tasks according to [Incentive Tasks of sif-6000 Testnet](https://github.com/hashgard/testnets/blob/master/sif/README.md).

## Next Steps

You have an active Hashgard Full Node now. What's next?

### Step 5: Upgrade to Validator Node

If you are involved in the genesis file generation process, then your node will be a Validator Node.

If you missed it, you can upgrade your node to Validator Node according to [Create Validator](../docs/create-validator.md).

You could try [Delegate](../docs/delegate.md), [Undelegate](../docs/unbond.md), [Redelegate](../docs/redelegate.md).

### Step 6: Governance of Blockchain

You can submit a proposal or vote to a proposal in Hashgard testnet.

How to submit a proposal? see [Submit Proposal](../docs/submit-proposal.md).

Proposal needs to be activated to vote, see [Deposit](../docs/deposit.md) to activate a proposal.

You could [Vote](../docs/vote.md) to an activated proposal.
