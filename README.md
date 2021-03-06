# Burger
Second full stack homework project

![Image of Burger App](public/assets/images/readme/Burger_App.png)

## Instructions

### App Setup
* Create a GitHub repo called burger and clone it to your computer.
* Make a package.json file by running npm init from the command line.
* Install the Express npm package: npm install express.
* Create a server.js file.
* Install the Handlebars npm package: npm install express-handlebars.
* Install MySQL npm package: npm install mysql.

![Image of Burger Repository](public/assets/images/readme/Burger_Repository.png)

### Require the following npm packages inside of the server.js file:
* express

### DB Setup
* Inside your burger directory, create a folder named db.
* In the db folder, create a file named schema.sql. Write SQL queries this file that do the following:
* Create the burgers_db.
* Switch to or use the burgers_db.
* Create a burgers table with these fields:
    * id: an auto incrementing int that serves as the primary key.
    * burger_name: a string.
    * devoured: a boolean.
* Still in the db folder, create a seeds.sql file. In this file, write insert queries to populate the burgers table with at least three entries.
* Run the schema.sql and seeds.sql files into the mysql server from the command line
* Now you're going to run these SQL files.
    * Make sure you're in the db folder of your app.
    * Start MySQL command line tool and login: mysql -u root -p.
    * With the mysql> command line tool running
        * Enter the command source schema.sql. 
            * This will run your schema file and all of the queries in it -- in other words, you'll be creating your database.
    * Now insert the entries you defined in seeds.sql by running the file: source seeds.sql.
    * Close out of the MySQL command line tool: exit.
    
![Image of Burger Database](public/assets/images/readme/Burger_db.png)

### Config Setup
* Inside your burger directory, create a folder named config.
* Create a connection.js file inside config directory.
* Inside the connection.js file, setup the code to connect Node to MySQL.
* Export the connection.
* Create an orm.js file inside config directory.
* Import (require) connection.js into orm.js
* In the orm.js file, 
    * create the methods that will execute the necessary MySQL commands in the controllers.
        * These are the methods you will need to use in order to retrieve and store data in your database.
            * selectAll()
            * insertOne()
            * updateOne()
* Export the ORM object in module.exports.

### Model Setup
* Inside your burger directory, create a folder named models.
    * In models, make a burger.js file.
        * Inside burger.js, import orm.js into burger.js
            * Also inside burger.js, create the code that will call the ORM functions using burger specific input for the ORM.
* Export at the end of the burger.js file.

### Controller setup
* Inside your burger directory, create a folder named controllers.
* In controllers, create the burgers_controller.js file.
* Inside the burgers_controller.js file, import the following:
    * Express
    * burger.js
* Create the router for the app, and export the router at the end of your file.

### View setup
* Inside your burger directory, create a folder named views.
* Create the index.handlebars file inside views directory.
* Create the layouts directory inside views directory.
    * Create the main.handlebars file inside layouts directory.
    * Setup the main.handlebars file so it's able to be used by Handlebars.
    * Setup the index.handlebars to have the template that Handlebars can render onto.
* Create a button in index.handlebars that will submit the user input into the database.

### Directory structure

![Image of Burger Directory Structure](public/assets/images/readme/Directory_1.png)
![Image of Burger Directory Structure](public/assets/images/readme/Directory_2.png)
![Image of Burger Directory Structure](public/assets/images/readme/Directory_3.png)
![Image of Burger Directory Structure](public/assets/images/readme/Directory_4.png)
![Image of Burger Directory Structure](public/assets/images/readme/Directory_5.png)

### Reminder: Submission on BCS
Please submit both the deployed Heroku link to your homework AND the link to the Github Repository!

### Minimum Requirements
Attempt to complete homework assignment as described in instructions. If unable to complete certain portions, please pseudocode these portions to describe what remains to be completed. Hosting on Heroku and adding a README.md are required for this homework. In addition, add this homework to your portfolio, more information can be found below.

### Hosting on Heroku
Now that we have a backend to our applications, we use Heroku for hosting. Please note that while Heroku is free, it will request credit card information if you have more than 5 applications at a time or are adding a database.
* Please see Heroku’s Account Verification Information for more details.

### Create a README.md
Add a README.md to your repository describing the project. *You're reading it.*

### Add To Your Portfolio
After completing the homework please add the piece to your portfolio. Make sure to add a link to your updated portfolio in the comments section of your homework so the TAs can easily ensure you completed this step when they are grading the assignment. To receive an 'A' on any assignment, you must link to it from your portfolio.
