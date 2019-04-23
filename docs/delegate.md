# Delegate

You can increase your shares by delegating your token to a validator.

## Delegate tokens

You can view all the validator information by running the following command:

```bash
  Hashgardcli stake validators --trust-node
```

Next you can choose a validator address and delegate:

```bash
Hashgardcli stake delegate --validator=${validator_address} --amount=${amount} --chain-id=${chain-id} --from=${wallet_name}
```

After delegating, you can determine if you have successfully delegated by looking at the information from the validator.

```bash
Hashgardcli stake validator ${validator_address} --trust-node
```

