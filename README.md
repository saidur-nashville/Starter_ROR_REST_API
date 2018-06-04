# README

This is a basic Ruby on Rails REST API.  I will create a more complex version later.

* Ruby version
  - Ruby on Rails version 5.1.6
  - Ruby version 2.3.3

* System dependencies
  - Faker for test data
  - Run bundle install
  - Start the server

* Configuration
  - Clone this repo
  - Run 'bundle install' to install dependent gems
  - Run web server

* Database creation
  - Create database 'rails db:create'
  - Migrate database 'rails db:migrate'
  - To add data 'rake db:seed'

* Database initialization
  - Use Faker to generate test data
  - To add data 'rake db:seed'  For example,
    20.times do
      Article.create({
        title: Faker::Book.title,
        body: Faker::Lorem.sentence
      })
    end

* How to run the test suite
  - I used Postman for testing this API. You can use any other method you want. For more details about Postman, go to https://github.com/postmanlabs/postman-app-support/
  - To view all records, change dropdown to 'get' and type http://localhost:3000/api/v1/articles on params and then click on 'Send'.  Result will display all results from the database.
  - To view a single record, change dropdown to 'get' and type http://localhost:3000/api/v1/articles/1 where '1' is the result ID and click on send and you will get one result back from the database.
  - To create a record, 'post' it through http://localhost:3000/api/v1/articles.  Change 'header' to 'content-type' and value to 'application-json'. Add json to 'body'. For example,
  {
	"title":"My Fisrt Title",
	"body":"This is the body for my first title"
  }
  - To detele a record, change it to 'delete' and type http://localhost:3000/api/v1/articles/1 where '1' is the ID for the record you want to delete.
  - To update a record, change it to 'put' and type http://localhost:3000/api/v1/articles/1 where '1' is the ID for the record you want to update. Change 'header' to 'content-type' and value to 'application-json'. Add json to 'body'. For example,
  {
	"title":"Record title will be Updated",
	"body":"This is the updated body for the record"
  }
* ...
