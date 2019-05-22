# omniauth-aloha

[OmniAuth](https://github.com/intridea/omniauth) Strategy for Aloha.

Note: This is a fork of the [original](https://github.com/richardvanhook/omniauth-aloha) project with modification to function as a specific strategy for Salesforce.com Aloha.

## Basic Usage

```ruby
require "sinatra"
require "omniauth"
require "omniauth-aloha"

class MyApplication < Sinatra::Base
  use Rack::Session
  use OmniAuth::Builder do
    provider :aloha, ENV['ALOHA_KEY'], ENV['ALOHA_SECRET']
  end
end
```

## Including other sites

```ruby
use OmniAuth::Builder do
    provider :aloha, 
             ENV['ALOHA_KEY'], 
             ENV['ALOHA_SECRET']
end
```

## Resources

* [Article: Digging Deeper into OAuth 2.0 on Force.com](http://wiki.developerforce.com/index.php/Digging_Deeper_into_OAuth_2.0_on_Force.com)
