# ATM Simulation
A program which simulate the functionalities of ATM
- ATM contains two records with the following details:
  --
   - Name          : John Doe

     PIN           : 012108

     Balance       : $100

     Account Number: 112233

   - Name          : Jane Doe

     PIN           : 932012

     Balance       : $30

     Account Number: 112244

- Welcome Screen
  --
  ```
  Enter Account Number: 112233
  Enter PIN: 443322
  ```
  - Account Number should have 6 digits length. Display message `Account Number should have 6 digits length` for invalid Account Number.
  - Account Number should only contains numbers [0-9]. Display message `Account Number should only contains numbers` for invalid Account Number.
  - PIN should have 6 digits length. Display message `PIN should have 6 digits length` for invalid PIN.
  - PIN should only contains numbers [0-9]. Display message `PIN should only contains numbers` for invalid PIN.
  - Check valid Acccount Number & PIN with ATM records. Display message `Invalid Account Number/PIN` if records is not exist.
  - Valid Account Number & PIN will take user to __Transaction Screen__.
- Transaction Screen
  --
   ````
   1. Withdraw
   2. Fund Transfer
   3. Exit
   Please choose option[3]:
   ````
   - The default option(no input needed) is 3 (Exit), cancel the process and back to __Welcome Screen__.
   - Invalid option will re-display the screen..
   - Option 1 (Withdraw) will display __Withdraw Screen__.
   - Option 2 (Fund Transfer), it will take user to __Fund Transfer Screen__.
- Withdraw Screen
  --
   ````
   1. $10
   2. $50
   3. $100
   4. Other
   5. Back
   Please choose option[5]:
   ````
   - Option [1-3] will deduct user balance and go to __Summary Screen__.
   - Option 4 (Other) will display Other __Withdraw Screen__.
   - Insufficient balance will display message `Insufficient balance $30`.
   - When users enter 5 (Back), go to Transaction Screen
   - Option 5 (Back) will display __Transaction Screen__.
- Other Withdraw Screen
  --
  ````
  Other Withdraw
  Enter amount to withdraw:
  ````
  - Maximum amount to withdraw is $1000. Display message `Maximum amount to withdraw is $1000` if withdraw amount is higher than $1000.
  - Display message `Invalid ammount` if withdraw amount is not numbers.
  - Display message `Invalid ammount` if withdraw amount is not multiple of $10.
  - Display message `Insufficient balance $10` for insufficient balance. `$10` is the withdraw amount 
  - Valid amount will deduct the user balance with withdraw amount and go to __Summary Screen__.
- Summary Screen
  -- 
  ````
  Summary
  Date : 2019-02-30 10:00 AM
  Withdraw : $50
  Balance : $10
  
  1. Transaction 
  2. Exit
  Choose option[2]:
  ````
- Fund Transfer Screen
  --
  **Fund Transfer Screen 1 :**
  ````
  Please enter destination account and 
  press enter to continue or 
  press cancel (Esc) to go back to Transaction: 
  ````
  
  **Fund Transfer Screen 2 :**
  ````
  Please enter transfer amount and 
  press enter to continue or 
  press cancel (Esc) to go back to Transaction: 
  ````
  
  **Fund Transfer Screen 3 :**
  ````
  Please enter reference number (Optional) and 
  press enter to continue or 
  press cancel (Esc) to go back to Transaction: 
  ````
  
  **Fund Transfer Screen 4 :**
  ````
  Transfer Confirmation
  Destination Account : xxx-xxx-xxx-x
  Transfer Amount     : $yy
  Reference Number    : zzzzzzzzzzzzz

  1. Confirm Trx
  2. Cancel Trx
  Choose option[2]:
  ````

  Transaction processing happens after user choose 1 (Confirm Trx)
  - Display message `Invalid account` if account is not numbers
  - Display message `Invalid account` if account is not found
  - Maximum amount to transfer is $1000. Display message `Maximum amount to withdraw is $1000` if transfer amount is higher than $1000.
  - Minimum amount to transfer is $1. Display message `Minimum amount to withdraw is $1` if transfer amount is lower than $1.
  - Display message `Invalid amount` if transfer amount is not numbers.
  - Display message `Insufficient balance $300` for insufficient balance. `$300` is the transfer amount 
  - Display message `Invalid Reference Number` if reference number is not empty and not numbers
  - Valid amount will deduct the user balance with transfer amount and will add destination account with transfer amount. After that screen will go to **Fund Transfer Summary Screen**.

- Fund Transfer Summary Screen
  --
  ````
  Fund Transfer Summary
  Destination Account : xxx-xxx-xxx-x
  Transfer Amount     : $yy
  Reference Number    : zzzzzzzzzzzzz
  Balance             : $zz
  
  1. Transaction
  2. Exit
  Choose option[2]:
  ````



## Review
Each person will randomly review at least two of other person’s work.

Follow the steps bellow:
1. Run the application. Does the Welcome Screen is displayed? (give 1 point)
2. Enter 11 for account number. Does error message is displayed? (give 1 point)
3. Enter 112211 for account number and 112211 for PIN number. Does error message is displayed? (give point 1)
4. TBD
5. TBD
6. TBD
7. Take a look on the source code and gives your comments if you think there are things that can be improved.
