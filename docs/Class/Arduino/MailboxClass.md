# MailboxClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_mailbox_class.html)

## メンバー

### MailboxClass()



```c
MailboxClass::MailboxClass(BridgeClass &b=Bridge)
```

!!! summary "引数"
	- BridgeClass& `b` 



### begin()



```c
void MailboxClass::begin()
```



### end()



```c
void MailboxClass::end()
```



### readMessage()



```c
unsigned int MailboxClass::readMessage(uint8_t *buffer, unsigned int size)
```

!!! summary "引数"
	- uint8_t * `buffer` 
	- unsigned int `size` 

!!! note "戻り値"
	unsigned int



### readMessage()



```c
void MailboxClass::readMessage(String &str, unsigned int maxLength=128)
```

!!! summary "引数"
	- String & `str` 
	- unsigned int `maxLength` 



### writeMessage()



```c
void MailboxClass::writeMessage(const uint8_t *buffer, unsigned int size)
```

!!! summary "引数"
	- constuint8_t * `buffer` 
	- unsigned int `size` 



### writeMessage()



```c
void MailboxClass::writeMessage(const String &str)
```

!!! summary "引数"
	- constString & `str` 



### writeJSON()



```c
void MailboxClass::writeJSON(const String &str)
```

!!! summary "引数"
	- constString & `str` 



### messageAvailable()



```c
unsigned int MailboxClass::messageAvailable()
```

!!! note "戻り値"
	unsigned int



