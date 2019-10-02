# RequestHandler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_request_handler.html)

## メンバー

### ~RequestHandler()



```c
virtual RequestHandler::~RequestHandler()
```



### canHandle()



```c
virtual bool RequestHandler::canHandle(HTTPMethod method, String uri)
```

!!! summary "引数"
	- HTTPMethod `method` 
	- String `uri` 

!!! note "戻り値"
	bool



### canUpload()



```c
virtual bool RequestHandler::canUpload(String uri)
```

!!! summary "引数"
	- String `uri` 

!!! note "戻り値"
	bool



### handle()



```c
virtual bool RequestHandler::handle(WebServer &server, HTTPMethod requestMethod, String requestUri)
```

!!! summary "引数"
	- WebServer& `server` 
	- HTTPMethod `requestMethod` 
	- String `requestUri` 

!!! note "戻り値"
	bool



### upload()



```c
virtual void RequestHandler::upload(WebServer &server, String requestUri, HTTPUpload &upload)
```

!!! summary "引数"
	- WebServer& `server` 
	- String `requestUri` 
	- HTTPUpload& `upload` 



### next()



```c
RequestHandler* RequestHandler::next()
```

!!! note "戻り値"
	RequestHandler*



### next()



```c
void RequestHandler::next(RequestHandler *r)
```

!!! summary "引数"
	- RequestHandler* `r` 



### pathArg()



```c
const String& RequestHandler::pathArg(unsigned int i)
```

!!! summary "引数"
	- unsigned int `i` 

!!! note "戻り値"
	constString &



