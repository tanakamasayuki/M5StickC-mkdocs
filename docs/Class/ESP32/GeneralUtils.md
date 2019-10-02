# GeneralUtils

General utilities. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_general_utils.html)

## メンバー

### base64Decode()
Decode a chunk of data that is  encoded.


```c
bool GeneralUtils::base64Decode(const std::string &in, std::string *out)
```

!!! summary "引数"
	- const& `in` The string to be decoded. 
	- std::string* `out` The resulting data. 

!!! note "戻り値"
	bool



### base64Encode()
Encode a string into base 64.


```c
bool GeneralUtils::base64Encode(const std::string &in, std::string *out)
```

!!! summary "引数"
	- const& `in` 
	- std::string* `out` 

!!! note "戻り値"
	bool



### dumpInfo()
Dump general info to the log. Data includes:



```c
void GeneralUtils::dumpInfo()
```



### endsWith()
Does the string end with a specific character?


```c
bool GeneralUtils::endsWith(std::string str, char c)
```

!!! summary "引数"
	- std::string `str` The string to examine. 
	- char `c` The character to look form. 

!!! note "戻り値"
	bool True if the string ends with the given character. 



### errorToString()
Convert an ESP error code to a string.


```c
const char * GeneralUtils::errorToString(esp_err_t errCode)
```

!!! summary "引数"
	- esp_err_t `errCode` The errCode to be converted. 

!!! note "戻り値"
	constchar * A string representation of the error code. 



### wifiErrorToString()
Convert a wifi_err_reason_t code to a string.


```c
const char * GeneralUtils::wifiErrorToString(uint8_t value)
```

!!! summary "引数"
	- uint8_t `value` 

!!! note "戻り値"
	constchar * A string representation of the error code.



### hexDump()
Dump a representation of binary data to the console.


```c
void GeneralUtils::hexDump(const uint8_t *pData, uint32_t length)
```

!!! summary "引数"
	- const* `pData` Pointer to the start of data to be logged. 
	- uint32_t `length` Length of the data (in bytes) to be logged. 



### ipToString()
Convert an IP address to string.


```c
std::string GeneralUtils::ipToString(uint8_t *ip)
```

!!! summary "引数"
	- uint8_t* `ip` The 4 byte IP address. 

!!! note "戻り値"
	std::string A string representation of the IP address. 



### split()
Split a string into parts based on a delimiter.


```c
std::vector< std::string > GeneralUtils::split(std::string source, char delimiter)
```

!!! summary "引数"
	- std::string `source` The source string to split. 
	- char `delimiter` The delimiter characters. 

!!! note "戻り値"
	std::stringstd::vector<  > A vector of strings that are the split of the input. 



### toLower()
Convert a string to lower case.


```c
std::string GeneralUtils::toLower(std::string &value)
```

!!! summary "引数"
	- std::string& `value` The string to convert to lower case. 

!!! note "戻り値"
	std::string A lower case representation of the string. 



### trim()
Remove white space from a string.


```c
std::string GeneralUtils::trim(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	std::string



