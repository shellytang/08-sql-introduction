![CF](https://i.imgur.com/7v5ASc8.png)  Lab 08: SQL and Postgres
=======
[Code of Conduct](https://github.com/codefellows/code-of-conduct)

Today we introduced several new pieces to our technology stack, including SQL (Structured Query Language) and PG (Node-Postgres). We've provided a good amount of new code in the `articles.js` file, so you will want to review that new code.

Your lab TODOs today will require you to write SQL queries and add associated data to those queries in the `server.js` file, though you need to have an understanding at this point as to how everything is working together to accomplish our full functionality. You also have one large TODO in the `article.js` file to complete the full range of loading your records.


## Getting started (DO THIS AFTER CLONING YOUR FORK)
*Don't start your Node server just yet...*

1. `cd starter-code` to change dirs to the starter code directory
2. Ensure that you have your postgres server running, using the alias that we set up in lecture: `pgstart`
3. Run the following command to create your user-db in postgres: `createdb` (If for some reason you already have a user-db, it will tell you)
4. Run the following command from the starter code dir: `bin/loadarticles`
  * This command is a local executable in the `bin/` directory (feel free to read the code, but do not get hung up on it if you don't know what's going on...)
  * It will create a connection with your local postgres db, read the contents of hackerIpsum.json, and then load each record into the DB in a table called `articles`
  * This executable also relies on the `loadDB.js` file in the `lib/` directory (feel free to read the code!).
5. In your terminal, start postgres using the `psql` command, and check that there are now records in the DB.
  * Once in the postgres shell, run `select count(*) from articles`
  * The output should read that you now have 250 records in the articles table.

You're ready to go! **Start your Node server now!**

## User Stories: MVP
 - As a developer, I want article data to persist with SQL, so that I can store more, faster and have more query flexibility.

This means you'll want to be able to do full CRUD on articles in the database. You'll have to use SQL to make a table for articles (**and clear out the table for troubleshooting**), with a class-level method attached to the constructor function (because it does not apply to any single instance). Then teach each article instance how to write or update itself to the database, or delete itself, via instance methods (available for use as needed in the code).

Crucially, you'll need to trace through the app logic, and all those callback functions to determine WHEN is the right time to load data, or convert JSON.

Look through the TODOs, which signify areas of the code with varying levels of completeness, and focus initially on writing correct SQL. Practice in the web inspector.

<!-- There is no portfolio assignment. -->
