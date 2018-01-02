# Creating new rails app page and making it the root of the page

Rails page can be created by generating a new controller.

## Generate new controller

By entering the command below, a Top controller with index page will be created.

`rails generate controller top index`

## Setting the generated controller as the root directory

In order to change the root directory of the rails app, modify the `/config/routes.rb` file

```rb
Rails.application.routes.draw do
  root 'top#index'
end
```

## Test the result

Now, if you run server by running `rails server`, and open `localhost:3000`, the new generated page should be displayed instead of the default rails page.