# Redelegate

- You can re-delegate GARD token to new validator

  You can do the following:

  ```bash
    Hashgardcli stake redelegate \
        --chain-id=${chain-id} \
        --from=${wallet_name} \
        --addr-validator-source=${validator_address} \
        --addr-validator-dest=${validator_address} \
        --shares-fraction=0.1 \
        --gas=simulate
  ```

  ```addr-validator-source``` is the original validator address you need to transfer the delegation
  ``` addr-validator-dest``` is the new validator address you need to transfer to
  ```share-amount``` The number of shares transferred, positive
  ```shares-fraction``` transfer ratio, a positive number between 0 and 1

  Setting ```gas=simulate``` will automatically calculate gas

  **You can specify the number of tokens to be delegated with `--shares-amount` or `--shares-percent`. Remember that these two parameters cannot be used at the same time. **

