# WebServer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_web_server.html)

## メンバー



### WebServer()



```c
WebServer::WebServer(IPAddress addr, int port=80)
```

!!! summary "引数"
	- IPAddress `addr` 
	- int `port` 



### WebServer()



```c
WebServer::WebServer(int port=80)
```

!!! summary "引数"
	- int `port` 



### ~WebServer()



```c
WebServer::~WebServer()
```



### begin()



```c
void WebServer::begin()
```



### begin()



```c
void WebServer::begin(uint16_t port)
```

!!! summary "引数"
	- uint16_t `port` 



### handleClient()



```c
void WebServer::handleClient()
```



### close()



```c
void WebServer::close()
```



### stop()



```c
void WebServer::stop()
```



### authenticate()



```c
bool WebServer::authenticate(const char *username, const char *password)
```

!!! summary "引数"
	- constchar * `username` 
	- constchar * `password` 

!!! note "戻り値"
	bool



### requestAuthentication()



```c
void WebServer::requestAuthentication(HTTPAuthMethod mode=BASIC_AUTH, const char *realm=NULL, const String &authFailMsg=String(""))
```

!!! summary "引数"
	- HTTPAuthMethod `mode` 
	- constchar * `realm` 
	- constString & `authFailMsg` 



### on()



```c
void WebServer::on(const String &uri, THandlerFunction handler)
```

!!! summary "引数"
	- constString & `uri` 
	- THandlerFunction `handler` 



### on()



```c
void WebServer::on(const String &uri, HTTPMethod method, THandlerFunction fn)
```

!!! summary "引数"
	- constString & `uri` 
	- HTTPMethod `method` 
	- THandlerFunction `fn` 



### on()



```c
void WebServer::on(const String &uri, HTTPMethod method, THandlerFunction fn, THandlerFunction ufn)
```

!!! summary "引数"
	- constString & `uri` 
	- HTTPMethod `method` 
	- THandlerFunction `fn` 
	- THandlerFunction `ufn` 



### addHandler()



```c
void WebServer::addHandler(RequestHandler *handler)
```

!!! summary "引数"
	- RequestHandler* `handler` 



### serveStatic()



```c
void WebServer::serveStatic(const char *uri, fs::FS &fs, const char *path, const char *cache_header=NULL)
```

!!! summary "引数"
	- constchar * `uri` 
	- fs::FS& `fs` 
	- constchar * `path` 
	- constchar * `cache_header` 



### onNotFound()



```c
void WebServer::onNotFound(THandlerFunction fn)
```

!!! summary "引数"
	- THandlerFunction `fn` 



### onFileUpload()



```c
void WebServer::onFileUpload(THandlerFunction fn)
```

!!! summary "引数"
	- THandlerFunction `fn` 



### uri()



```c
String WebServer::uri()
```

!!! note "戻り値"
	String



### method()



```c
HTTPMethod WebServer::method()
```

!!! note "戻り値"
	HTTPMethod



### client()



```c
virtual WiFiClient WebServer::client()
```

!!! note "戻り値"
	WiFiClient



### upload()



```c
HTTPUpload& WebServer::upload()
```

!!! note "戻り値"
	HTTPUpload&



### pathArg()



```c
String WebServer::pathArg(unsigned int i)
```

!!! summary "引数"
	- unsigned int `i` 

!!! note "戻り値"
	String



### arg()



```c
String WebServer::arg(String name)
```

!!! summary "引数"
	- String `name` 

!!! note "戻り値"
	String



### arg()



```c
String WebServer::arg(int i)
```

!!! summary "引数"
	- int `i` 

!!! note "戻り値"
	String



### argName()



```c
String WebServer::argName(int i)
```

!!! summary "引数"
	- int `i` 

!!! note "戻り値"
	String



### args()



```c
int WebServer::args()
```

!!! note "戻り値"
	int



### hasArg()



```c
bool WebServer::hasArg(String name)
```

!!! summary "引数"
	- String `name` 

!!! note "戻り値"
	bool



### collectHeaders()



```c
void WebServer::collectHeaders(const char *headerKeys[], const size_t headerKeysCount)
```

!!! summary "引数"
	- constchar * `headerKeys` 
	- constsize_t `headerKeysCount` 



### header()



```c
String WebServer::header(String name)
```

!!! summary "引数"
	- String `name` 

!!! note "戻り値"
	String



### header()



```c
String WebServer::header(int i)
```

!!! summary "引数"
	- int `i` 

!!! note "戻り値"
	String



### headerName()



```c
String WebServer::headerName(int i)
```

!!! summary "引数"
	- int `i` 

!!! note "戻り値"
	String



### headers()



```c
int WebServer::headers()
```

!!! note "戻り値"
	int



### hasHeader()



```c
bool WebServer::hasHeader(String name)
```

!!! summary "引数"
	- String `name` 

!!! note "戻り値"
	bool



### hostHeader()



```c
String WebServer::hostHeader()
```

!!! note "戻り値"
	String



### send()



```c
void WebServer::send(int code, const char *content_type=NULL, const String &content=String(""))
```

!!! summary "引数"
	- int `code` 
	- constchar * `content_type` 
	- constString & `content` 



### send()



```c
void WebServer::send(int code, char *content_type, const String &content)
```

!!! summary "引数"
	- int `code` 
	- char * `content_type` 
	- constString & `content` 



### send()



```c
void WebServer::send(int code, const String &content_type, const String &content)
```

!!! summary "引数"
	- int `code` 
	- constString & `content_type` 
	- constString & `content` 



### send_P()



```c
void WebServer::send_P(int code, PGM_P content_type, PGM_P content)
```

!!! summary "引数"
	- int `code` 
	- PGM_P `content_type` 
	- PGM_P `content` 



### send_P()



```c
void WebServer::send_P(int code, PGM_P content_type, PGM_P content, size_t contentLength)
```

!!! summary "引数"
	- int `code` 
	- PGM_P `content_type` 
	- PGM_P `content` 
	- size_t `contentLength` 



### setContentLength()



```c
void WebServer::setContentLength(const size_t contentLength)
```

!!! summary "引数"
	- constsize_t `contentLength` 



### sendHeader()



```c
void WebServer::sendHeader(const String &name, const String &value, bool first=false)
```

!!! summary "引数"
	- constString & `name` 
	- constString & `value` 
	- bool `first` 



### sendContent()



```c
void WebServer::sendContent(const String &content)
```

!!! summary "引数"
	- constString & `content` 



### sendContent_P()



```c
void WebServer::sendContent_P(PGM_P content)
```

!!! summary "引数"
	- PGM_P `content` 



### sendContent_P()



```c
void WebServer::sendContent_P(PGM_P content, size_t size)
```

!!! summary "引数"
	- PGM_P `content` 
	- size_t `size` 



### streamFile()



```c
size_t WebServer::streamFile(T &file, const String &contentType)
```

!!! summary "引数"
	- T& `file` 
	- constString & `contentType` 

!!! note "戻り値"
	size_t



### urlDecode()



```c
String WebServer::urlDecode(const String &text)
```

!!! summary "引数"
	- constString & `text` 

!!! note "戻り値"
	String



