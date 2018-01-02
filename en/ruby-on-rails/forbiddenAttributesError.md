## How to handle ForbiddenAttributesError

From Rails 4, forms submitted to create model needs to have parameters specified.

This was made to prevent Models from being created with unwnted parameters.

In order to whitelist a set of parameters that are to be submitted, you can use the `permit` method.

```rb
def create
  @feed = Post.new(post_params)
  ...
end

private

def post_params
  params.permit(
    :title, :body
  )
end

## You can also specialize this method with per-user

def user_params
  params.require(:user).permit(
    :title, :body
  )
end


```

Reference: 


[strong_parameter in Rails 4.0](http://blog.willnet.in/entry/2012/10/26/005901)
[Handling ForbiddenAttributesError](http://jangajan.com/blog/2014/09/24/forbiddenattributeserror-in-rails/)