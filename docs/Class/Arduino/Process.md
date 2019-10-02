# Process



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_process.html)

## メンバー

### Process()



```c
Process::Process(BridgeClass &_b=Bridge)
```

!!! summary "引数"
	- BridgeClass& `_b` 



### ~Process()



```c
Process::~Process()
```



### begin()



```c
void Process::begin(const String &command)
```

!!! summary "引数"
	- constString & `command` 



### addParameter()



```c
void Process::addParameter(const String &param)
```

!!! summary "引数"
	- constString & `param` 



### run()



```c
unsigned int Process::run()
```

!!! note "戻り値"
	unsigned int



### runAsynchronously()



```c
void Process::runAsynchronously()
```



### running()



```c
boolean Process::running()
```

!!! note "戻り値"
	boolean



### exitValue()



```c
unsigned int Process::exitValue()
```

!!! note "戻り値"
	unsigned int



### close()



```c
void Process::close()
```



### runShellCommand()



```c
unsigned int Process::runShellCommand(const String &command)
```

!!! summary "引数"
	- constString & `command` 

!!! note "戻り値"
	unsigned int



### runShellCommandAsynchronously()



```c
void Process::runShellCommandAsynchronously(const String &command)
```

!!! summary "引数"
	- constString & `command` 



### operator bool()



```c
Process::operator bool()
```



### available()



```c
int Process::available()
```

!!! note "戻り値"
	int



### read()



```c
int Process::read()
```

!!! note "戻り値"
	int



### peek()



```c
int Process::peek()
```

!!! note "戻り値"
	int



### write()



```c
size_t Process::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### flush()



```c
void Process::flush()
```



