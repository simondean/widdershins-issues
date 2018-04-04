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

## getGreeting

<a id="opIdgetGreeting"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://example.com/greeting \
  -H 'Accept: application/json'

```

```http
GET http://example.com/greeting HTTP/1.1
Host: example.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'http://example.com/greeting',
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

fetch('http://example.com/greeting',
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

result = RestClient.get 'http://example.com/greeting',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://example.com/greeting', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://example.com/greeting");
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
    req, err := http.NewRequest("GET", "http://example.com/greeting", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /greeting`

Retrieves an greeting

> Example responses

```json
{
  "description": "Successfull response",
  "value": {
    "greeting": "Hello!"
  }
}
```

<h3 id="getGreeting-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Responds with a greeting|Inline|

<h3 id="getGreeting-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Description|
|---|---|---|---|
|» greeting|any|true|No description|

*oneOf*

|»» *anonymous*|string|false|No description|

*xor*

|»» *anonymous*|object|false|No description|
|»»» message1|string|true|No description|
|»»» message2|string|true|No description|

<aside class="success">
This operation does not require authentication
</aside>

