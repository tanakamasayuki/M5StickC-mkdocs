# FirmataClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_firmata_class.html)

## メンバー

### FirmataClass()


The Firmata class. An instance named "Firmata" is created automatically for the user. 
```c
FirmataClass::FirmataClass()
```



### begin()


Initialize the default Serial transport at the default baud of 57600. 
```c
void FirmataClass::begin()
```



### begin()



```c
void FirmataClass::begin(long)
```

!!! summary "引数"
	- long `` 



### begin()



```c
void FirmataClass::begin(Stream &s)
```

!!! summary "引数"
	- Stream& `s` A reference to the  transport object. This can be any type of transport that implements the  interface. Some examples include Ethernet, WiFi and other UARTs on the board (Serial1, Serial2, etc). 



### printVersion()


Send the Firmata protocol version to the Firmata host application. 
```c
void FirmataClass::printVersion(void)
```



### blinkVersion()


Blink the Firmata protocol version to the onboard LEDs (if the board has an onboard LED). If VERSION_BLINK_PIN is not defined in  for a particular board, then this method does nothing. The first series of flashes indicates the firmware major version (2 flashes = 2). The second series of flashes indicates the firmware minor version (5 flashes = 5). 
```c
void FirmataClass::blinkVersion(void)
```



### printFirmwareVersion()


Sends the firmware name and version to the Firmata host application. The major and minor version numbers are the first 2 bytes in the message. The following bytes are the characters of the firmware name. 
```c
void FirmataClass::printFirmwareVersion(void)
```



### setFirmwareNameAndVersion()



```c
void FirmataClass::setFirmwareNameAndVersion(const char *name, byte major, byte minor)
```

!!! summary "引数"
	- constchar * `name` A pointer to the name char array 
	- byte `major` The major version number 
	- byte `minor` The minor version number 



### disableBlinkVersion()


Provides a means to disable the version blink sequence on the onboard LED, trimming startup time by a couple of seconds. Call this before Firmata.begin(). It only applies when using the default Serial transport. 
```c
void FirmataClass::disableBlinkVersion()
```



### available()


A wrapper for  

```c
int FirmataClass::available(void)
```

!!! note "戻り値"
	int The number of bytes remaining in the input stream buffer. 



### processInput()


Read a single int from the input stream. If the value is not = -1, pass it on to parse(byte) 
```c
void FirmataClass::processInput(void)
```



### parse()



```c
void FirmataClass::parse(unsigned char value)
```

!!! summary "引数"
	- unsigned char `value` 



### isParsingMessage()




```c
boolean FirmataClass::isParsingMessage(void)
```

!!! note "戻り値"
	boolean Returns true if the parser is actively parsing data. 



### sendAnalog()



```c
void FirmataClass::sendAnalog(byte pin, int value)
```

!!! summary "引数"
	- byte `pin` The analog pin to send the value of (limited to pins 0 - 15). 
	- int `value` The value of the analog pin (0 - 1024 for 10-bit analog, 0 - 4096 for 12-bit, etc). The maximum value is 14-bits (16384). 



### sendDigital()



```c
void FirmataClass::sendDigital(byte pin, int value)
```

!!! summary "引数"
	- byte `pin` 
	- int `value` 



### sendDigitalPort()



```c
void FirmataClass::sendDigitalPort(byte portNumber, int portData)
```

!!! summary "引数"
	- byte `portNumber` The port number to send. Note that this is not the same as a "port" on the physical microcontroller. Ports are defined in order per every 8 pins in ascending order of the Arduino digital pin numbering scheme. Port 0 = pins D0 - D7, port 1 = pins D8 - D15, etc. 
	- int `portData` The value of the port. The value of each pin in the port is represented by a bit. 



### sendString()



```c
void FirmataClass::sendString(const char *string)
```

!!! summary "引数"
	- constchar * `string` A pointer to the char string 



### sendString()



```c
void FirmataClass::sendString(byte command, const char *string)
```

!!! summary "引数"
	- byte `command` Must be STRING_DATA 
	- constchar * `string` A pointer to the char string 



### sendSysex()



```c
void FirmataClass::sendSysex(byte command, byte bytec, byte *bytev)
```

!!! summary "引数"
	- byte `command` The sysex command byte. 
	- byte `bytec` The number of data bytes in the message (excludes start, command and end bytes). 
	- byte* `bytev` A pointer to the array of data bytes to send in the message. 



### write()



```c
void FirmataClass::write(byte c)
```

!!! summary "引数"
	- byte `c` The byte to be written. 



### attach()



```c
void FirmataClass::attach(byte command, callbackFunction newFunction)
```

!!! summary "引数"
	- byte `command` The ID of the command to attach a callback function to. 
	- callbackFunction `newFunction` A reference to the callback function to attach. 



### attach()



```c
void FirmataClass::attach(byte command, systemResetCallbackFunction newFunction)
```

!!! summary "引数"
	- byte `command` Must be set to SYSTEM_RESET or it will be ignored. 
	- systemResetCallbackFunction `newFunction` A reference to the system reset callback function to attach. 



### attach()



```c
void FirmataClass::attach(byte command, stringCallbackFunction newFunction)
```

!!! summary "引数"
	- byte `command` Must be set to STRING_DATA or it will be ignored. 
	- stringCallbackFunction `newFunction` A reference to the string callback function to attach. 



### attach()



```c
void FirmataClass::attach(byte command, sysexCallbackFunction newFunction)
```

!!! summary "引数"
	- byte `command` The ID of the command to attach a callback function to. 
	- sysexCallbackFunction `newFunction` A reference to the sysex callback function to attach. 



### detach()



```c
void FirmataClass::detach(byte command)
```

!!! summary "引数"
	- byte `command` The ID of the command to detatch the callback function from. 



### getPinMode()



```c
byte FirmataClass::getPinMode(byte pin)
```

!!! summary "引数"
	- byte `pin` The pin to get the configuration of. 

!!! note "戻り値"
	byte The configuration of the specified pin. 



### setPinMode()



```c
void FirmataClass::setPinMode(byte pin, byte config)
```

!!! summary "引数"
	- byte `pin` The pin to configure. 
	- byte `config` The configuration value for the specified pin. 



### getPinState()



```c
int FirmataClass::getPinState(byte pin)
```

!!! summary "引数"
	- byte `pin` The pin to get the state of. 

!!! note "戻り値"
	int The state of the specified pin. 



### setPinState()



```c
void FirmataClass::setPinState(byte pin, int state)
```

!!! summary "引数"
	- byte `pin` The pin to set the state of 
	- int `state` Set the state of the specified pin 



### sendValueAsTwo7bitBytes()



```c
void FirmataClass::sendValueAsTwo7bitBytes(int value)
```

!!! summary "引数"
	- int `value` The 16-bit value to be split and written separately. 



### startSysex()


A helper method to write the beginning of a Sysex message transmission. 
```c
void FirmataClass::startSysex(void)
```



### endSysex()


A helper method to write the end of a Sysex message transmission. 
```c
void FirmataClass::endSysex(void)
```



