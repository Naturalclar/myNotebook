# Using React with Ruby on Rails

From Rails 5.1, you can use the `webpacker` gem to bundle react components to your ruby-on-rails app.

## Creating new Rails app with react support

First, make sure your Rails version is above 5.1 by typing the following command

`rails --version`

If your rails version is older than 5.1, install rails 5.1 with the following command (or download the latest rails)

`gem install rails -v 5.1`

Then you can create new Rails app with React support using hte following command

`rails new react-rails-app --webpack=react`

Reference: 
[Free tutorial how to use react with webpaker and rails](https://medium.com/react-on-rails/free-tutorial-how-to-use-react-with-webpacker-and-rails-5-1-92af8e8d9d63)