# Redelegate

- You can re-delegate GARD token to new validator

  You can do the following:

  ```bash
   hashgardcli stake redelegate ${validator_address_source} ${validator_address_dest} \
       --from=${wallet_name} 
  ```
  
  ```address-validator-source``` is the original validator address you need to transfer the delegation
  `address-validator-dest` is the new validator address you need to transfer to
  
