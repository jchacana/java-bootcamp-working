# Evolving your ATM simulation

Now that you have a Spring boot application, why don't you spend some time looking at the various starters packages available.

For this stage, we require:

 - Support all previous functional requirements
 - Add `@Transactional` support. This will enable the app to work in an transactional way. If there's an exception, a rollback should happen
 - Incorporate Spring MVC in a clean way. Up to this stage, we can assume that some layers have been defined, making the migrations smooth
 - Incorporate Spring Data JPA and manage your entities through Repositories
 - Re write the screens written in JSP/Servlet to Thymeleaf. Use the proper Controllers
 - Provide 200 accounts and some already created transactions that should load on startup. Figure out a way to do this
 - Provide a new screen that can show ALL the transactions the AUTHENTICATED USER has performed,  but as paged results. We don't want to see all results on screen at once. Make sure to read about Paged results on Repositories
 - Integrate Spring Security to login page. Then, make sure that all operations, expect login, require an authenticated user. If a non-authenticated user tries to perform an action, an exception should be thrown
 - Add logs everytime a user confirms/perform a transaction. Consider, though, that we don't want you to add log messages at each of the involved method. Instead use AOP
 - Deploy your Spring boot app on AWS. Make sure to provision a machine with Linux and your selected RDBMS. You may use a preexisting AMI or provision the server however you like. Provide a public link to access



NOTE: If you need to re create the project, you're free to do it, but keep the same repository so we can look at the history


# Review

Each person will randomly review at least two of other person’s work.

Follow the steps below:

 - Does the app run on AWS under a public ip?
 - Does the app provide a login screen
 - Does the app validate user/password via Spring Security
 - Does the app validate permissions if a user wants to access a "private" functionality?
 - Does the app provide general logs without intervening the existent code? (AOP)
 - Does the app provide the screen the see all transactions, paged, that  a user has made?
 - Does the app provide a clear way of loading 200 accounts on startup?
 - All tests running and green?


