# Rails Commands Quiz
## I looked at my notes from the past two days for the answers.


Fork, clone, and write your answers directly in this file. Then submit a pull request.

### Question 1

I want to start a new Rails project/app called `BunnyApp`. What command should I type in the terminal?

rails new BunnyApp --database=postgresql -T

#Answer: 1 - Correct. Capital T referes to "without tests"



### Question 2

I want to create a new model called `Bunny`, with the following attributes: name (string), color (string), and age (integer). What command should I type in the terminal?

rails generate migration CreateBunny name color age:integer
rails generate model Bunny name color age:integer

#Answer: 1 - Correct




### Question 3

What does the command in Question 2 do, exactly? What files are created, where are they located, and what does the database look like at this time? Explain.

The command in question 2 creates a migration file that links to the model, controller, and associated views that do that basic CRUD functions for Bunny.

Answers: 0.5 -It creates a migration file in db/migrate with the columns and datatypes that were specified in the Terminal Command. db/schema.rb is not created until we run the migration.

rails g model: creates a file in /app/models/bunny.rb which defines the Bunny as a Ruby class, AND  creates a migration file in /db/migrate with the columns and datatypes that were specified in the Terminal command



### Question 4

I want to create a database and make it reflect the new model I created in Question 2. What command(s) should I type in the terminal?

rake:db:create  ---->creates a migration file. If you only created a model and not a migration file, then you would do this.

rake db:migrate
rake:db:migrate:status
##rake db:create db:migrate (all on one line!)

Answer: 0.5 - If you did rails g migration, then your model files still don't exist, and you would need to create them manually.




### Question 5

I want to look at the actual database that has been created. What command should I type in the terminal?

rails db
\d

Answer: 1 - correct



### Question 6

I want to see a list of all the URLs available in my app, along with the HTTP requests and controllers associated with them. What command should I type in the terminal?

don't know the answer.

Answer- 0- rake routes



### Question 7

I have worked on my app and finally want to see it in action. What command should I type in the terminal, and where should I navigate to in my browser?

rails server
http://localhost:3000/index   ----> leave out the /index because we have not set up index yet.

Answer: 0.7
