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

## getOneOf

<a id="opIdgetOneOf"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://example.com/one-of \
  -H 'Accept: application/json'

```

```http
GET http://example.com/one-of HTTP/1.1
Host: example.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'http://example.com/one-of',
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

fetch('http://example.com/one-of',
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

result = RestClient.get 'http://example.com/one-of',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://example.com/one-of', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://example.com/one-of");
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
    req, err := http.NewRequest("GET", "http://example.com/one-of", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /one-of`

Retrieves an greeting

> Example responses

```json
{
  "greeting": "Hello!"
}
```

<h3 id="getOneOf-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Responds with a greeting|Inline|

<h3 id="getOneOf-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Description|
|---|---|---|---|
|» greeting|any|true|No description|

*oneOf*

|Name|Type|Required|Description|
|---|---|---|---|
|»» *anonymous*|string|false|No description|

*xor*

|Name|Type|Required|Description|
|---|---|---|---|
|»» *anonymous*|object|false|No description|
|»»» message1|string|true|No description|
|»»» message2|string|true|No description|

<aside class="success">
This operation does not require authentication
</aside>

## getAnyOf

<a id="opIdgetAnyOf"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://example.com/any-of \
  -H 'Accept: application/json'

```

```http
GET http://example.com/any-of HTTP/1.1
Host: example.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'http://example.com/any-of',
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

fetch('http://example.com/any-of',
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

result = RestClient.get 'http://example.com/any-of',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://example.com/any-of', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://example.com/any-of");
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
    req, err := http.NewRequest("GET", "http://example.com/any-of", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /any-of`

Retrieves an greeting

> Example responses

```json
{
  "greeting": "Hello!"
}
```

<h3 id="getAnyOf-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Responds with a greeting|Inline|

<h3 id="getAnyOf-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Description|
|---|---|---|---|
|» greeting|any|true|No description|

*anyOf*

|Name|Type|Required|Description|
|---|---|---|---|
|»» *anonymous*|string|false|No description|

*or*

|Name|Type|Required|Description|
|---|---|---|---|
|»» *anonymous*|object|false|No description|
|»»» message1|string|true|No description|
|»»» message2|string|true|No description|

<aside class="success">
This operation does not require authentication
</aside>

## getAllOf

<a id="opIdgetAllOf"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://example.com/all-of \
  -H 'Accept: application/json'

```

```http
GET http://example.com/all-of HTTP/1.1
Host: example.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'http://example.com/all-of',
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

fetch('http://example.com/all-of',
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

result = RestClient.get 'http://example.com/all-of',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://example.com/all-of', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://example.com/all-of");
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
    req, err := http.NewRequest("GET", "http://example.com/all-of", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /all-of`

Retrieves an greeting

> Example responses

```json
{
  "greeting": "Hello!"
}
```

<h3 id="getAllOf-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Responds with a greeting|Inline|

<h3 id="getAllOf-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Description|
|---|---|---|---|
|» greeting|any|true|No description|

*allOf*

|Name|Type|Required|Description|
|---|---|---|---|
|»» *anonymous*|string|false|No description|

*and*

|Name|Type|Required|Description|
|---|---|---|---|
|»» *anonymous*|object|false|No description|
|»»» message1|string|true|No description|
|»»» message2|string|true|No description|

<aside class="success">
This operation does not require authentication
</aside>

