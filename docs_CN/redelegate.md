# 重新委托
对于您曾委托过的验证人，您可以通过再次委托，对委托给前者的代币重新委托给后者

您可以通过如下操作：
```bash
 hashgardcli stake redelegate ${validator_address_source} ${validator_address_dest} \
     --from=${wallet_name}

```

```address-validator-source``` 是您需要转移委托的原验证器地址
`address-validator-dest` 是您需要转移到的新的验证器地址
