# HttpClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_http_client.html)

## メンバー

### HttpClient()



```c
HttpClient::HttpClient()
```



### get()



```c
unsigned int HttpClient::get(String &url)
```

!!! summary "引数"
	- String & `url` 

!!! note "戻り値"
	unsigned int



### get()



```c
unsigned int HttpClient::get(const char *url)
```

!!! summary "引数"
	- constchar * `url` 

!!! note "戻り値"
	unsigned int



### getAsynchronously()



```c
void HttpClient::getAsynchronously(String &url)
```

!!! summary "引数"
	- String & `url` 



### getAsynchronously()



```c
void HttpClient::getAsynchronously(const char *url)
```

!!! summary "引数"
	- constchar * `url` 



### post()



```c
unsigned int HttpClient::post(String &url, String &data)
```

!!! summary "引数"
	- String & `url` 
	- String & `data` 

!!! note "戻り値"
	unsigned int



### post()



```c
unsigned int HttpClient::post(const char *url, const char *data)
```

!!! summary "引数"
	- constchar * `url` 
	- constchar * `data` 

!!! note "戻り値"
	unsigned int



### postAsynchronously()



```c
void HttpClient::postAsynchronously(String &url, String &data)
```

!!! summary "引数"
	- String & `url` 
	- String & `data` 



### postAsynchronously()



```c
void HttpClient::postAsynchronously(const char *url, const char *data)
```

!!! summary "引数"
	- constchar * `url` 
	- constchar * `data` 



### patch()



```c
unsigned int HttpClient::patch(String &url, String &data)
```

!!! summary "引数"
	- String & `url` 
	- String & `data` 

!!! note "戻り値"
	unsigned int



### patch()



```c
unsigned int HttpClient::patch(const char *url, const char *data)
```

!!! summary "引数"
	- constchar * `url` 
	- constchar * `data` 

!!! note "戻り値"
	unsigned int



### patchAsynchronously()



```c
void HttpClient::patchAsynchronously(String &url, String &data)
```

!!! summary "引数"
	- String & `url` 
	- String & `data` 



### patchAsynchronously()



```c
void HttpClient::patchAsynchronously(const char *url, const char *data)
```

!!! summary "引数"
	- constchar * `url` 
	- constchar * `data` 



### put()



```c
unsigned int HttpClient::put(String &url, String &data)
```

!!! summary "引数"
	- String & `url` 
	- String & `data` 

!!! note "戻り値"
	unsigned int



### put()



```c
unsigned int HttpClient::put(const char *url, const char *data)
```

!!! summary "引数"
	- constchar * `url` 
	- constchar * `data` 

!!! note "戻り値"
	unsigned int



### putAsynchronously()



```c
void HttpClient::putAsynchronously(String &url, String &data)
```

!!! summary "引数"
	- String & `url` 
	- String & `data` 



### putAsynchronously()



```c
void HttpClient::putAsynchronously(const char *url, const char *data)
```

!!! summary "引数"
	- constchar * `url` 
	- constchar * `data` 



### setHeader()



```c
void HttpClient::setHeader(String &header)
```

!!! summary "引数"
	- String & `header` 



### setHeader()



```c
void HttpClient::setHeader(const char *header)
```

!!! summary "引数"
	- constchar * `header` 



### ready()



```c
boolean HttpClient::ready()
```

!!! note "戻り値"
	boolean



### getResult()



```c
unsigned int HttpClient::getResult()
```

!!! note "戻り値"
	unsigned int



### noCheckSSL()



```c
void HttpClient::noCheckSSL()
```



### checkSSL()



```c
void HttpClient::checkSSL()
```



