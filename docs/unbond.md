# Unbond

For the validator you have delegated, you can also take back your token by unbinding.

## Unbind operation

You can choose a validator address that you have delegated and unbind it:

```bash
hashgardcli stake unbond \
    --validator=${validator_address} \
    --shares-fraction=0.1 \
    --from=${wallet_name} \
    --chain-id=${chain-id}
```

After delegating, you can check if you have unbind successfully by checking the information in the validator.

```bash
hashgardcli stake validator ${validator_address}
```
