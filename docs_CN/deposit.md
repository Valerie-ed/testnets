# 抵押存款
只有存款达到一定值 min_deposit 后，才会进入投票期

您可以通过如下操作去对指定的提案进行抵押存款：
```bash
 hashgardcli gov deposit  ${proposal-id} ${deposit-amount}  \
     --from=${wallet_name} 
    
```


`proposal-id`是提案的 id 号

`deposit-amount`是需要存款的金额


在您进行存款抵押之后，您可以通过查看该提议的保证金详细情况

```bash
hashgardcli gov deposits ${proposal-id}
```

