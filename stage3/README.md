# Evolving your ATM simulation

Up to this point, we have learned a new technology to organize our project, as well as some standard frameworks like JPA (and ORM) or Spring.

For this stage, the requirements are:

  - Migrate your current project to a maven structure with spring boot. Don't move forward unless you've solved this point. Remember to commit your changes and keep everything in the same repository. We need to know when this migration was done.
  - Add JPA support to your project. Achieve this by adding the correct maven dependency
  - Now with JPA support, modify your model so you can map entities with tables
  - Create a connection to a database. You can use MySQL, PostgreSQL or MSSqlServer
  - Add support for JUnit (write at least the tests specified in the review section)
  - Provide a way (up to you) to query all the transactions made on a specific day. You have to handle dates. HINT!: Use Java 8 Date API
  - Migrate all your current screens to JSP and/or Servlet (up to you)

Remember to still support previous requirements. We're evolving an application


# Review

Each person will randomly review at least two of other person’s work.

Follow the steps below:

 - Run the application. Is the Welcome screen displayed?
 - Does the app provide all the previous functionalities? (We don't want regressions!)
 - To avoid regressions, write the following tests (make them independent):
   - When adding an account, this account is expected to be there when getting user by number account
   - When adding an account, this account is expected to be there when getting list of accounts
   - When creating a withdraw transaction to an account, this account is expected to have its balance reduced by the amount indicated in the withdraw
   - When creating a withdraw transaction to an account, and the account does not have enough funds, it's expected to receive an error
   - When creating a transfer transaction from account1 to account2, it's expected to have account1's balance reduced by the amount of the transaction and have account2's balance increased by the amount of the transaction
   - When creating a transfer transaction from account1 to account2, and account1 does not have enough funds, operation should throw an error
   - When creating a transfer transaction from account1 to account2, and account2 does not exist, then operation should fail
   - When creating a succesful transaction, it's expected to have this transaction when getting list of last 10 transactions
   - When creating a bunch of succesful transactions, it's expected to have this list of transactions when getting list of last 10 transactions
   - When creating more than 10 transactions, it's expected to have the 10 most recent transactions when getting list of last 10 transactions
   
 - Is the project easy to import? Try importing your workmate's project and check if it works
 - Is the repository tidy? Does it provide a .gitignore file. Does it include only source code?
 - Does it integrate with a physical database?
 - Does it provide SQL queries or JPQL queries?
 - Regarding the *select last 10 transactions* functionality, is it correctly integrated with database?
 - Regarding the *read from csv* functionality, is it correctly integrated with database?
 - Does all the CRUD operations actually persist to the database?


EXTRA POINTS:
 - It's possible to provide some testing data and load it automatically. Try it!



