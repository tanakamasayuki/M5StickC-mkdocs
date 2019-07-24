# StaticRequestHandler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_static_request_handler.html)

## メンバー

### StaticRequestHandler()



```c
StaticRequestHandler::StaticRequestHandler(FS &fs, const char *path, const char *uri, const char *cache_header)
```

!!! summary "引数"
	- FS & `fs` 
	- constchar * `path` 
	- constchar * `uri` 
	- constchar * `cache_header` 



### canHandle()



```c
bool StaticRequestHandler::canHandle(HTTPMethod requestMethod, String requestUri) override
```

!!! summary "引数"
	- HTTPMethod `requestMethod` 
	- String `requestUri` 

!!! note "戻り値"
	bool



### handle()



```c
bool StaticRequestHandler::handle(WebServer &server, HTTPMethod requestMethod, String requestUri) override
```

!!! summary "引数"
	- WebServer& `server` 
	- HTTPMethod `requestMethod` 
	- String `requestUri` 

!!! note "戻り値"
	bool



### getContentType()



```c
static String StaticRequestHandler::getContentType(const String &path)
```

!!! summary "引数"
	- constString & `path` 

!!! note "戻り値"
	String



