
### Usage examples for [ipapi.co](https://ipapi.co/) - IP location API

##### Example 1 : Using OpenURI 
```ruby
require 'open-uri'
require 'json'

loc = open('https://ipapi.co/8.8.8.8/json/').read
JSON.parse(loc)
```


##### Example 2 : Using Net::HTTP (ruby version >= 2.0.0)
```ruby
require 'net/http'
require 'json'

loc = Net::HTTP.get(URI('https://ipapi.co/8.8.8.8/json/'))
JSON.parse(loc)
```

##### Example 3 : Using Net::HTTP (ruby version < 2.0.0)
```ruby
require 'net/http'
require 'json'

uri   = URI('https://ipapi.co/8.8.8.8/json/')
https = Net::HTTP.new(uri.host, uri.port)
https.use_ssl = true
loc = https.get(uri.request_uri)
JSON.parse(loc.body)
```

### Output
```json
{
    "ip": "8.8.8.8",
    "city": "Mountain View",
    "region": "California",
    "region_code": "CA",
    "country": "US",
    "country_name": "United States",
    "postal": "94035",
    "latitude": 37.386,
    "longitude": -122.0838,
    "timezone": "America/Los_Angeles",
    "asn": "AS15169",
    "org": "Google Inc."
}
```
