# HTTPClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_h_t_t_p_client.html)

## メンバー

### HTTPClient()


constructor 
```c
HTTPClient::HTTPClient()
```



### ~HTTPClient()


destructor 
```c
HTTPClient::~HTTPClient()
```



### begin()



```c
bool HTTPClient::begin(WiFiClient &client, String url)
```

!!! summary "引数"
	- WiFiClient& `client` & 
	- String `url` String 

!!! note "戻り値"
	bool success bool 



### begin()



```c
bool HTTPClient::begin(WiFiClient &client, String host, uint16_t port, String uri="/", bool https=false)
```

!!! summary "引数"
	- WiFiClient& `client` & 
	- String `host` String 
	- uint16_t `port` uint16_t 
	- String `uri` String 
	- bool `https` bool 

!!! note "戻り値"
	bool success bool 



### begin()



```c
bool HTTPClient::begin(String url)
```

!!! summary "引数"
	- String `url` String 

!!! note "戻り値"
	bool



### begin()



```c
bool HTTPClient::begin(String url, const char *CAcert)
```

!!! summary "引数"
	- String `url` 
	- constchar * `CAcert` 

!!! note "戻り値"
	bool



### begin()



```c
bool HTTPClient::begin(String host, uint16_t port, String uri="/")
```

!!! summary "引数"
	- String `host` 
	- uint16_t `port` 
	- String `uri` 

!!! note "戻り値"
	bool



### begin()



```c
bool HTTPClient::begin(String host, uint16_t port, String uri, const char *CAcert)
```

!!! summary "引数"
	- String `host` 
	- uint16_t `port` 
	- String `uri` 
	- constchar * `CAcert` 

!!! note "戻り値"
	bool



### begin()



```c
bool HTTPClient::begin(String host, uint16_t port, String uri, const char *CAcert, const char *cli_cert, const char *cli_key)
```

!!! summary "引数"
	- String `host` 
	- uint16_t `port` 
	- String `uri` 
	- constchar * `CAcert` 
	- constchar * `cli_cert` 
	- constchar * `cli_key` 

!!! note "戻り値"
	bool



### end()


end called after the payload is handled 
```c
void HTTPClient::end(void)
```



### connected()


connected 

```c
bool HTTPClient::connected(void)
```

!!! note "戻り値"
	bool connected status 



### setReuse()



```c
void HTTPClient::setReuse(bool reuse)
```

!!! summary "引数"
	- bool `reuse` bool 



### setUserAgent()
keep-alive


```c
void HTTPClient::setUserAgent(const String &userAgent)
```

!!! summary "引数"
	- constString & `userAgent` const char * 



### setAuthorization()



```c
void HTTPClient::setAuthorization(const char *user, const char *password)
```

!!! summary "引数"
	- constchar * `user` const char * 
	- constchar * `password` const char * 



### setAuthorization()



```c
void HTTPClient::setAuthorization(const char *auth)
```

!!! summary "引数"
	- constchar * `auth` const char *  



### setConnectTimeout()



```c
void HTTPClient::setConnectTimeout(int32_t connectTimeout)
```

!!! summary "引数"
	- int32_t `connectTimeout` int32_t 



### setTimeout()



```c
void HTTPClient::setTimeout(uint16_t timeout)
```

!!! summary "引数"
	- uint16_t `timeout` unsigned int 



### useHTTP10()



```c
void HTTPClient::useHTTP10(bool usehttp10=true)
```

!!! summary "引数"
	- bool `usehttp10` 



### GET()
request handling

send a GET request 

```c
int HTTPClient::GET()
```

!!! note "戻り値"
	int http code 



### PATCH()



```c
int HTTPClient::PATCH(uint8_t *payload, size_t size)
```

!!! summary "引数"
	- uint8_t* `payload` uint8_t * 
	- size_t `size` size_t 

!!! note "戻り値"
	int http code 



### PATCH()



```c
int HTTPClient::PATCH(String payload)
```

!!! summary "引数"
	- String `payload` 

!!! note "戻り値"
	int



### POST()



```c
int HTTPClient::POST(uint8_t *payload, size_t size)
```

!!! summary "引数"
	- uint8_t* `payload` uint8_t * 
	- size_t `size` size_t 

!!! note "戻り値"
	int http code 



### POST()



```c
int HTTPClient::POST(String payload)
```

!!! summary "引数"
	- String `payload` 

!!! note "戻り値"
	int



### PUT()



```c
int HTTPClient::PUT(uint8_t *payload, size_t size)
```

!!! summary "引数"
	- uint8_t* `payload` uint8_t * 
	- size_t `size` size_t 

!!! note "戻り値"
	int http code 



### PUT()



```c
int HTTPClient::PUT(String payload)
```

!!! summary "引数"
	- String `payload` 

!!! note "戻り値"
	int



### sendRequest()



```c
int HTTPClient::sendRequest(const char *type, String payload)
```

!!! summary "引数"
	- constchar * `type` const char * "GET", "POST", .... 
	- String `payload` String data for the message body 

!!! note "戻り値"
	int 



### sendRequest()



```c
int HTTPClient::sendRequest(const char *type, uint8_t *payload=NULL, size_t size=0)
```

!!! summary "引数"
	- constchar * `type` const char * "GET", "POST", .... 
	- uint8_t* `payload` uint8_t * data for the message body if null not send 
	- size_t `size` size_t size for the message body if 0 not send 

!!! note "戻り値"
	int -1 if no info or > 0 when Content-Length is set by server 



### sendRequest()



```c
int HTTPClient::sendRequest(const char *type, Stream *stream, size_t size=0)
```

!!! summary "引数"
	- constchar * `type` const char * "GET", "POST", .... 
	- Stream* `stream`  * data stream for the message body 
	- size_t `size` size_t size for the message body if 0 not Content-Length is send 

!!! note "戻り値"
	int -1 if no info or > 0 when Content-Length is set by server 



### addHeader()



```c
void HTTPClient::addHeader(const String &name, const String &value, bool first=false, bool replace=true)
```

!!! summary "引数"
	- constString & `name` 
	- constString & `value` 
	- bool `first` 
	- bool `replace` 



### collectHeaders()
Response handling


```c
void HTTPClient::collectHeaders(const char *headerKeys[], const size_t headerKeysCount)
```

!!! summary "引数"
	- constchar * `headerKeys` 
	- constsize_t `headerKeysCount` 



### header()



```c
String HTTPClient::header(const char *name)
```

!!! summary "引数"
	- constchar * `name` 

!!! note "戻り値"
	String



### header()



```c
String HTTPClient::header(size_t i)
```

!!! summary "引数"
	- size_t `i` 

!!! note "戻り値"
	String



### headerName()



```c
String HTTPClient::headerName(size_t i)
```

!!! summary "引数"
	- size_t `i` 

!!! note "戻り値"
	String



### headers()



```c
int HTTPClient::headers()
```

!!! note "戻り値"
	int



### hasHeader()



```c
bool HTTPClient::hasHeader(const char *name)
```

!!! summary "引数"
	- constchar * `name` 

!!! note "戻り値"
	bool



### getSize()


size of message body / payload 

```c
int HTTPClient::getSize(void)
```

!!! note "戻り値"
	int -1 if no info or > 0 when Content-Length is set by server 



### getStream()


returns the stream of the tcp connection 

```c
WiFiClient & HTTPClient::getStream(void)
```

!!! note "戻り値"
	WiFiClient&  



### getStreamPtr()


returns a pointer to the stream of the tcp connection 

```c
WiFiClient * HTTPClient::getStreamPtr(void)
```

!!! note "戻り値"
	WiFiClient* WiFiClient* 



### writeToStream()



```c
int HTTPClient::writeToStream(Stream *stream)
```

!!! summary "引数"
	- Stream* `stream`  * 

!!! note "戻り値"
	int bytes written ( negative values are error codes ) 



### getString()


return all payload as String (may need lot of ram or trigger out of memory!) 

```c
String HTTPClient::getString(void)
```

!!! note "戻り値"
	String String 



### errorToString()



```c
String HTTPClient::errorToString(int error)
```

!!! summary "引数"
	- int `error` int 

!!! note "戻り値"
	String String 



