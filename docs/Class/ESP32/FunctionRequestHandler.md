# FunctionRequestHandler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_function_request_handler.html)

## メンバー

### FunctionRequestHandler()



```c
FunctionRequestHandler::FunctionRequestHandler(WebServer::THandlerFunction fn, WebServer::THandlerFunction ufn, const String &uri, HTTPMethod method)
```

!!! summary "引数"
	- WebServer::THandlerFunction `fn` 
	- WebServer::THandlerFunction `ufn` 
	- constString & `uri` 
	- HTTPMethod `method` 



### canHandle()



```c
bool FunctionRequestHandler::canHandle(HTTPMethod requestMethod, String requestUri) override
```

!!! summary "引数"
	- HTTPMethod `requestMethod` 
	- String `requestUri` 

!!! note "戻り値"
	bool



### canUpload()



```c
bool FunctionRequestHandler::canUpload(String requestUri) override
```

!!! summary "引数"
	- String `requestUri` 

!!! note "戻り値"
	bool



### handle()



```c
bool FunctionRequestHandler::handle(WebServer &server, HTTPMethod requestMethod, String requestUri) override
```

!!! summary "引数"
	- WebServer& `server` 
	- HTTPMethod `requestMethod` 
	- String `requestUri` 

!!! note "戻り値"
	bool



### upload()



```c
void FunctionRequestHandler::upload(WebServer &server, String requestUri, HTTPUpload &upload) override
```

!!! summary "引数"
	- WebServer& `server` 
	- String `requestUri` 
	- HTTPUpload& `upload` 



