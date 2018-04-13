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

Example API

Base URLs:

* <a href="http://example.com">http://example.com</a>

<h1 id="Example-API-Endpoints">Endpoints</h1>

## getGreeting

<a id="opIdgetGreeting"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://example.com/greeting \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://example.com/greeting HTTP/1.1
Host: example.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'http://example.com/greeting',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "greeting": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('http://example.com/greeting',
{
  method: 'POST',
  body: inputBody,
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://example.com/greeting',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://example.com/greeting', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://example.com/greeting");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
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
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://example.com/greeting", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /greeting`

Creates an greeting

> Body parameter

```json
{
  "greeting": "string"
}
```

<h3 id="getGreeting-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|Contains the greeting to create|
|» greeting|body|string|true|No description|

> Example responses

```json
{
  "greeting": "Response!"
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
|» greeting|string|true|No description|

<aside class="success">
This operation does not require authentication
</aside>

