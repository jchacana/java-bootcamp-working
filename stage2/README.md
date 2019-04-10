# Evolving your ATM simulation

We were using a fixed set of accounts and keeping them into memory. As we're evolving our app, we'll need to adjust for a few requirements

  - Read the account initial info from a csv file
    - Fields will remain ` Name `, ` PIN `, ` Balance `, ` Account Number `
  - CSV file needs to have at least 20 records. Be creative :-)
  - In order to read from CSV file, apply everything you've learned so far in this unit.
  - Add the following validations:
    - There can't be 2 different accounts with the same Account Number
    - There can't be duplicated records
    
  - We need to keep track of the transactions that have been made in our system. For that reason, model something that will help us with this requirement
  - Provide a screen that help us query the last 10 transactions of a given account

# HINT!
You can make use of everything you've learned to this point. Special attention to Lambdas, Streams and IO

