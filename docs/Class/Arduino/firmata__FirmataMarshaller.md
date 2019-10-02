# firmata::FirmataMarshaller



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/classfirmata_1_1_firmata_marshaller.html)

## メンバー

### FirmataMarshaller()


The  class. 
```c
FirmataMarshaller::FirmataMarshaller()
```



### begin()



```c
void FirmataMarshaller::begin(Stream &s)
```

!!! summary "引数"
	- Stream& `s` A reference to the  transport object. This can be any type of transport that implements the  interface. Some examples include Ethernet, WiFi and other UARTs on the board (Serial1, Serial2, etc). 



### end()


Closes the  stream by setting its stream reference to  
```c
void FirmataMarshaller::end()
```



### queryFirmwareVersion()


Query the target's firmware name and version 
```c
void FirmataMarshaller::queryFirmwareVersion(void) const
```



### queryVersion()


Query the target's Firmata protocol version 
```c
void FirmataMarshaller::queryVersion(void) const
```



### reportAnalogDisable()



```c
void FirmataMarshaller::reportAnalogDisable(uint8_t pin) const
```

!!! summary "引数"
	- uint8_t `pin` The analog pin for which to request the value (limited to pins 0 - 15). 



### reportAnalogEnable()



```c
void FirmataMarshaller::reportAnalogEnable(uint8_t pin) const
```

!!! summary "引数"
	- uint8_t `pin` The analog pin for which to request the value (limited to pins 0 - 15). 



### reportDigitalPortDisable()



```c
void FirmataMarshaller::reportDigitalPortDisable(uint8_t portNumber) const
```

!!! summary "引数"
	- uint8_t `portNumber` The port number for which to request the value. Note that this is not the same as a "port" on the physical microcontroller. Ports are defined in order per every 8 pins in ascending order of the Arduino digital pin numbering scheme. Port 0 = pins D0 - D7, port 1 = pins D8 - D15, etc. 



### reportDigitalPortEnable()



```c
void FirmataMarshaller::reportDigitalPortEnable(uint8_t portNumber) const
```

!!! summary "引数"
	- uint8_t `portNumber` The port number for which to request the value. Note that this is not the same as a "port" on the physical microcontroller. Ports are defined in order per every 8 pins in ascending order of the Arduino digital pin numbering scheme. Port 0 = pins D0 - D7, port 1 = pins D8 - D15, etc. 



### sendAnalog()



```c
void FirmataMarshaller::sendAnalog(uint8_t pin, uint16_t value) const
```

!!! summary "引数"
	- uint8_t `pin` The analog pin to which the value is sent. 
	- uint16_t `value` The value of the analog pin (0 - 1024 for 10-bit analog, 0 - 4096 for 12-bit, etc). 



### sendAnalogMappingQuery()


Send an analog mapping query to the Firmata host application. The resulting sysex message will have an ANALOG_MAPPING_RESPONSE command byte, followed by a list of pins [0-n]; where each pin will specify its corresponding analog pin number or 0x7F (127) if not applicable. 
```c
void FirmataMarshaller::sendAnalogMappingQuery(void) const
```



### sendCapabilityQuery()


Send a capability query to the Firmata host application. The resulting sysex message will have a CAPABILITY_RESPONSE command byte, followed by a list of byte tuples (mode and mode resolution) for each pin; where each pin list is terminated by 0x7F (127). 
```c
void FirmataMarshaller::sendCapabilityQuery(void) const
```



### sendDigital()



```c
void FirmataMarshaller::sendDigital(uint8_t pin, uint8_t value) const
```

!!! summary "引数"
	- uint8_t `pin` The digital pin to send the value of. 
	- uint8_t `value` The value of the pin. 



### sendDigitalPort()



```c
void FirmataMarshaller::sendDigitalPort(uint8_t portNumber, uint16_t portData) const
```

!!! summary "引数"
	- uint8_t `portNumber` The port number to send. Note that this is not the same as a "port" on the physical microcontroller. Ports are defined in order per every 8 pins in ascending order of the Arduino digital pin numbering scheme. Port 0 = pins D0 - D7, port 1 = pins D8 - D15, etc. 
	- uint16_t `portData` The value of the port. The value of each pin in the port is represented by a bit. 



### sendFirmwareVersion()



```c
void FirmataMarshaller::sendFirmwareVersion(uint8_t major, uint8_t minor, size_t bytec, uint8_t *bytev) const
```

!!! summary "引数"
	- uint8_t `major` The major verison number 
	- uint8_t `minor` The minor version number 
	- size_t `bytec` The length of the firmware name 
	- uint8_t * `bytev` The firmware name array 



### sendVersion()



```c
void FirmataMarshaller::sendVersion(uint8_t major, uint8_t minor) const
```

!!! summary "引数"
	- uint8_t `major` The major verison number 
	- uint8_t `minor` The minor version number 



### sendPinMode()



```c
void FirmataMarshaller::sendPinMode(uint8_t pin, uint8_t config) const
```

!!! summary "引数"
	- uint8_t `pin` The pin to configure. 
	- uint8_t `config` The configuration value for the specified pin. 



### sendPinStateQuery()



```c
void FirmataMarshaller::sendPinStateQuery(uint8_t pin) const
```

!!! summary "引数"
	- uint8_t `pin` The pin to query 



### sendString()



```c
void FirmataMarshaller::sendString(const char *string) const
```

!!! summary "引数"
	- constchar * `string` A pointer to the char string 



### sendSysex()



```c
void FirmataMarshaller::sendSysex(uint8_t command, size_t bytec, uint8_t *bytev) const
```

!!! summary "引数"
	- uint8_t `command` The sysex command byte. 
	- size_t `bytec` The number of data bytes in the message (excludes start, command and end bytes). 
	- uint8_t * `bytev` A pointer to the array of data bytes to send in the message. 



### setSamplingInterval()



```c
void FirmataMarshaller::setSamplingInterval(uint16_t interval_ms) const
```

!!! summary "引数"
	- uint16_t `interval_ms` The interval (in milliseconds) at which to sample 



### systemReset()


Perform a software reset on the target. For example, StandardFirmata.ino will initialize everything to a known state and reset the parsing buffer. 
```c
void FirmataMarshaller::systemReset(void) const
```



