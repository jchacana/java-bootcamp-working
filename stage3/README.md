# Evolving your ATM simulation

Up to this point, we have learned a new technology to organize our project, as well as some standard frameworks like JPA (and ORM) or Spring.

For this stage, the requirements are:

  - Migrate your current project to a maven structure with spring boot. Don't move forward unless you've solved this point. Remember to commit your changes and keep everything in the same repository. We need to know when this migration was done.
  - Add JPA support to your project. Achieve this by adding the correct maven dependency
  - Now with JPA support, modify your model so you can map entities with tables
  - Create either a physical database or an in-memory sql database. It's up to you
  - Add support for JUnit
    - Add at least 5 unit tests
  - Provide a way (up to you) to query all the transactions made on a specific day. You have to handle dates. HINT!: Use Java 8 Date API

Remember to still support previous requirements. We're evolving an application


# Review

Each person will randomly review at least two of other person’s work.

Follow the steps below:

 - Run the application. Is the Welcome screen displayed?
 - Does the app provide all the previous functionalities? (We don't want regressions!)
 - Is the project easy to import? Try importing your workmate's project and check if it works
 - Is the repository tidy? Does it provide a .gitignore file. Does it include only source code?
 - Does it integrate with a physical or in-memory database?
 - Does it provide SQL queries?
 - Does it provide at least 5 unit tests? Can they be run regardless of the order? Can they be executed with a build?
 - Regarding the *select last 10 transactions* functionality, is it correctly integrated with database?
 - Regarding the *read from csv* functionality, is it correctly integrated with database?
 - Does all the CRUD operations actually persist to the database?


EXTRA POINTS:
 - It's possible to provide some testing data and load it automatically. Try it!



