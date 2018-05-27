---
title: Example API v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="Example-API">Example API v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

This is an example API

Base URLs:

* <a href="http://example.com">http://example.com</a>

<h1 id="Example-API-Endpoints">Endpoints</h1>

## getCars

<a id="opIdgetCars"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://example.com/cars \
  -H 'Accept: application/json'

```

```http
GET http://example.com/cars HTTP/1.1
Host: example.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'http://example.com/cars',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('http://example.com/cars',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'http://example.com/cars',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://example.com/cars', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://example.com/cars");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://example.com/cars", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /cars`

Retrieves all cars

> Example responses

```json
{
  "vehicles": [
    {
      "id": "",
      "wheels": [
        {
          "width": 235,
          "aspectRatio": 35,
          "diameter": 19
        },
        {
          "width": 235,
          "aspectRatio": 35,
          "diameter": 19
        },
        {
          "width": 305,
          "aspectRatio": 30,
          "diameter": 19
        },
        {
          "width": 305,
          "aspectRatio": 30,
          "diameter": 19
        }
      ],
      "doors": [
        {
          "electricWindow": true
        },
        {
          "electricWindow": true
        }
      ],
      "engine": {
        "fuel": "petrol",
        "capacity": 3.8
      }
    }
  ]
}
```

<h3 id="getCars-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Responds with the details of all cars|Inline|

<h3 id="getCars-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Description|
|---|---|---|---|
|» vehicles|[object]|true|No description|
|»» id|string|true|Example description|
|»» wheels|[object]|true|No description|
|»»» width|integer|true|Example description|
|»»» aspectRatio|integer|true|Example description|
|»»» diameter|integer|true|Example description|
|»» doors|[object]|true|No description|
|»»» electricWindow|boolean|true|Example description|
|»» engine|object|true|Example description|
|»»» fuel|string|true|Example description|
|»»» capacity|number|true|Example description|

<aside class="success">
This operation does not require authentication
</aside>

