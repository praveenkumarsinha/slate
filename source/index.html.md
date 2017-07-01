---
title: DrawingView API(v 0.1) Reference

language_tabs:
  - shell
  - ruby
  - javascript

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - users
  - errors

search: true
---

# Introduction

Welcome to the DrawingView API(v 0.1)! These API end points will serve core functionality from creating user to adding/uploading drawings and then data capturing using annotations like punch and drawing tools.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

These API end points are also used to cater request from official DrawingView iPad/iPhone and Android apps.

# Authentication

> To authorize, use this code:

```ruby
require "net/http" 
require "uri" 
url = URI.parse("api_endpoint_here") 
req = Net::HTTP::Get.new(url.path) 
req.add_field("Authorization", 'Bearer 7b77b0c2-870b-4bfd-a285-1f561087d503') 
res = Net::HTTP.new(url.host, url.port).start do |http| 
http.request(req) 
end 
puts res.body
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: 7b77b0c2-870b-4bfd-a285-1f561087d503"
```

```javascript
$.ajax({
    url: 'api_endpoint_here',
    headers: {
        'Authorization':'Bearer 7b77b0c2-870b-4bfd-a285-1f561087d503',
        'Content-Type':'application/json'
    }
  });
```

> Make sure to replace `7b77b0c2-870b-4bfd-a285-1f561087d503` with your API key.

DrawingView uses API key to allow access to the API, which can be grabbed by calling users's sign-up api or log-in api discussed below.

DrawingView expects for the API key to be included in all API requests to the server in a header that looks like the following, unless mentioned otherwise:

`Authorization: Bearer 7b77b0c2-870b-4bfd-a285-1f561087d503`

<aside class="notice">
You must replace <code>7b77b0c2-870b-4bfd-a285-1f561087d503</code> with user's personal API key.
</aside>
