# Using React with Ruby on Rails

From Rails 5.1, you can use the `webpacker` gem to bundle react components to your ruby-on-rails app.

## Creating new Rails app with react support

First, make sure your Rails version is above 5.1 by typing the following command

`rails --version`

If your rails version is older than 5.1, install rails 5.1 with the following command (or download the latest rails)

`gem install rails -v 5.1`

Then you can create new Rails app with React support using hte following command

`rails new react-rails-app --webpack=react`

Your react components will be in `apps/javascript` folder.

## Generate new page with react components

First, generate a new controller

`rails g controller pages home`

Change the root to newly generated page by editing `routes.rb` in the `config` folder

```rb
#config/routes.rb
Rails.application.routes.draw do
  root 'pages#home'
end
```

Edit the view of `home` to display the react component

```rb
#app/views/home.html.erb
<%= javascript_pack_tag 'hello_react' %>
```

This will display the `hello_react` component that was built during init.



## Running the server

In order to run the server to view it locally, you need to run following two commands

`rails s`
`./bin/webpack-dev-server`

If you have the `foreman` gem installed, you can create a `Procfile` on your root directory with the following content, then run `foreman start -p 3000`

```
web: bundle exec rails s
webpacker: ./bin/webpack-dev-server
```

## Running it on Heroku

In order to run the app on heroku, create a `Procfile` on your root dirctory with the following content 

```
web: bundle exec rails s
webpacker: ./bin/webpack-dev-server
```



Reference: 
[Free tutorial how to use react with webpaker and rails](https://medium.com/react-on-rails/free-tutorial-how-to-use-react-with-webpacker-and-rails-5-1-92af8e8d9d63)

[Get in Full Stack Shape with Rails 5.1 Webpacker and ReactJS](https://x-team.com/blog/get-in-full-stack-shape-with-rails-5-1-webpacker-and-reactjs/)