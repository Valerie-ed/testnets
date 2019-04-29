# Delegate

You can increase your shares by delegating your token to a validator.

## Delegate tokens

You can view all the validator information by running the following command:

```bash
  hashgardcli stake validators 
```

Next you can choose a validator address and delegate:

```bash
hashgardcli stake delegate ${validator_address} ${amount} \
    --from=${your_wallet_name}
```

After delegating, you can determine if you have successfully delegated by looking at the information from the validator.

```bash
hashgardcli stake validator ${validator_address} 
```

