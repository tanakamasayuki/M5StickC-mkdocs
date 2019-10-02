# firmata::FirmataParser



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/classfirmata_1_1_firmata_parser.html)

## メンバー













### FirmataParser()



```c
FirmataParser::FirmataParser(uint8_t *dataBuffer=(uint8_t *) NULL, size_t dataBufferSize=0)
```

!!! summary "引数"
	- uint8_t * `dataBuffer` A pointer to an external buffer used to store parsed data 
	- size_t `dataBufferSize` The size of the external buffer 



### parse()



```c
void FirmataParser::parse(uint8_t value)
```

!!! summary "引数"
	- uint8_t `value` 



### isParsingMessage()




```c
bool FirmataParser::isParsingMessage(void) const
```

!!! note "戻り値"
	bool Returns true if the parser is actively parsing data. 



### setDataBufferOfSize()



```c
int FirmataParser::setDataBufferOfSize(uint8_t *dataBuffer, size_t dataBufferSize)
```

!!! summary "引数"
	- uint8_t * `dataBuffer` A pointer to an external buffer used to store parsed data 
	- size_t `dataBufferSize` The size of the external buffer 

!!! note "戻り値"
	int



### attach()



```c
void FirmataParser::attach(uint8_t command, callbackFunction newFunction, void *context=NULL)
```

!!! summary "引数"
	- uint8_t `command` The ID of the command to attach a callback function to. 
	- callbackFunction `newFunction` A reference to the callback function to attach. 
	- void * `context` An optional context to be provided to the callback function (NULL by default). 



### attach()



```c
void FirmataParser::attach(dataBufferOverflowCallbackFunction newFunction, void *context=NULL)
```

!!! summary "引数"
	- dataBufferOverflowCallbackFunction `newFunction` A reference to the buffer overflow callback function to attach. 
	- void * `context` An optional context to be provided to the callback function (NULL by default). 



### attach()



```c
void FirmataParser::attach(uint8_t command, stringCallbackFunction newFunction, void *context=NULL)
```

!!! summary "引数"
	- uint8_t `command` Must be set to STRING_DATA or it will be ignored. 
	- stringCallbackFunction `newFunction` A reference to the string callback function to attach. 
	- void * `context` An optional context to be provided to the callback function (NULL by default). 



### attach()



```c
void FirmataParser::attach(uint8_t command, sysexCallbackFunction newFunction, void *context=NULL)
```

!!! summary "引数"
	- uint8_t `command` The ID of the command to attach a callback function to. 
	- sysexCallbackFunction `newFunction` A reference to the sysex callback function to attach. 
	- void * `context` An optional context to be provided to the callback function (NULL by default). 



### attach()



```c
void FirmataParser::attach(uint8_t command, systemCallbackFunction newFunction, void *context=NULL)
```

!!! summary "引数"
	- uint8_t `command` The ID of the command to attach a callback function to. 
	- systemCallbackFunction `newFunction` A reference to the callback function to attach. 
	- void * `context` An optional context to be provided to the callback function (NULL by default). 



### attach()



```c
void FirmataParser::attach(uint8_t command, versionCallbackFunction newFunction, void *context=NULL)
```

!!! summary "引数"
	- uint8_t `command` The ID of the command to attach a callback function to. 
	- versionCallbackFunction `newFunction` A reference to the callback function to attach. 
	- void * `context` An optional context to be provided to the callback function (NULL by default). 



### detach()



```c
void FirmataParser::detach(uint8_t command)
```

!!! summary "引数"
	- uint8_t `command` The ID of the command to detatch the callback function from. 



### detach()



```c
void FirmataParser::detach(dataBufferOverflowCallbackFunction)
```

!!! summary "引数"
	- dataBufferOverflowCallbackFunction `` 



