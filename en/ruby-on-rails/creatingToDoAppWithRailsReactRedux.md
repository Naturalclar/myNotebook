# Creating a ToDo app with React, Redux, and Rails

## First, build a new Rails app

`rails new react-rails-todo webpacker=react`
`cd react-rails-todo`

## Install dependencies from Redux

`yarn add redux react-redux redux-thunk`

## Create New Controller for ToDo List, and set it as Route

`rails g controller todo index`

```rb
#./config/routes.rb
Rails.application.routes.draw do
  root 'todo#index'
end
```

## Edit View for Todo List

```rb
#./app/views/todo/index.html.erb
<div id="root"></div>
```

## Edit application.html.erb to include webpacker

```rb
#./app/views/layout/applications.html.erb
...
  <head>
    ...
    <%= javascript_pack_tag 'hello_react' %>
  </head>
...
```


## Run Server

`rails s`
`./bin/webpack-dev-server`

## Access Server

Open your browser, and access `localhost:3000`