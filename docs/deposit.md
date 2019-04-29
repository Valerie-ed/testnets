# Deposit

- The proposal will enter voting period only after the deposit reaches a certain value of min_deposit.

  You can make a deposit for the specified proposal by doing the following:

  ```bash
   hashgardcli gov deposit  ${proposal-id} ${deposit-amount} \
       --from=${wallet_name} 
  ```

  

` proposal-id` is the id number of the proposal

` deposit-amount` is the amount of deposit required

After making the deposit, you can view the deposit details of the proposal.

  ```bash
  Hashgardcli gov deposits ${proposal-id}
  ```

