# W5100Class



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_w5100_class.html)

## メンバー

###  SSIZE

```c
const uint16_t W5100Class::SSIZE
```


###  SMASK

```c
const uint16_t W5100Class::SMASK
```


### init()



```c
uint8_t W5100Class::init(void)
```

!!! note "戻り値"
	uint8_t



### execCmdSn()



```c
void W5100Class::execCmdSn(SOCKET s, SockCMD _cmd)
```

!!! summary "引数"
	- SOCKET `s` 
	- SockCMD `_cmd` 



### write()



```c
uint16_t W5100Class::write(uint16_t addr, const uint8_t *buf, uint16_t len)
```

!!! summary "引数"
	- uint16_t `addr` 
	- constuint8_t * `buf` 
	- uint16_t `len` 

!!! note "戻り値"
	uint16_t



### write()



```c
static uint8_t W5100Class::write(uint16_t addr, uint8_t data)
```

!!! summary "引数"
	- uint16_t `addr` 
	- uint8_t `data` 

!!! note "戻り値"
	uint8_t



### read()



```c
uint16_t W5100Class::read(uint16_t addr, uint8_t *buf, uint16_t len)
```

!!! summary "引数"
	- uint16_t `addr` 
	- uint8_t * `buf` 
	- uint16_t `len` 

!!! note "戻り値"
	uint16_t



### read()



```c
static uint8_t W5100Class::read(uint16_t addr)
```

!!! summary "引数"
	- uint16_t `addr` 

!!! note "戻り値"
	uint8_t



### getLinkStatus()



```c
W5100Linkstatus W5100Class::getLinkStatus()
```

!!! note "戻り値"
	W5100Linkstatus



### getChip()



```c
static uint8_t W5100Class::getChip(void)
```

!!! note "戻り値"
	uint8_t



### SBASE()



```c
static uint16_t W5100Class::SBASE(uint8_t socknum)
```

!!! summary "引数"
	- uint8_t `socknum` 

!!! note "戻り値"
	uint16_t



### RBASE()



```c
static uint16_t W5100Class::RBASE(uint8_t socknum)
```

!!! summary "引数"
	- uint8_t `socknum` 

!!! note "戻り値"
	uint16_t



### hasOffsetAddressMapping()



```c
static bool W5100Class::hasOffsetAddressMapping(void)
```

!!! note "戻り値"
	bool



### setSS()



```c
static void W5100Class::setSS(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 



### setGatewayIp()



```c
void W5100Class::setGatewayIp(const uint8_t *addr)
```

!!! summary "引数"
	- constuint8_t * `addr` 



### getGatewayIp()



```c
void W5100Class::getGatewayIp(uint8_t *addr)
```

!!! summary "引数"
	- uint8_t * `addr` 



### setSubnetMask()



```c
void W5100Class::setSubnetMask(const uint8_t *addr)
```

!!! summary "引数"
	- constuint8_t * `addr` 



### getSubnetMask()



```c
void W5100Class::getSubnetMask(uint8_t *addr)
```

!!! summary "引数"
	- uint8_t * `addr` 



### setMACAddress()



```c
void W5100Class::setMACAddress(const uint8_t *addr)
```

!!! summary "引数"
	- constuint8_t * `addr` 



### getMACAddress()



```c
void W5100Class::getMACAddress(uint8_t *addr)
```

!!! summary "引数"
	- uint8_t * `addr` 



### setIPAddress()



```c
void W5100Class::setIPAddress(const uint8_t *addr)
```

!!! summary "引数"
	- constuint8_t * `addr` 



### getIPAddress()



```c
void W5100Class::getIPAddress(uint8_t *addr)
```

!!! summary "引数"
	- uint8_t * `addr` 



### setRetransmissionTime()



```c
void W5100Class::setRetransmissionTime(uint16_t timeout)
```

!!! summary "引数"
	- uint16_t `timeout` 



### setRetransmissionCount()



```c
void W5100Class::setRetransmissionCount(uint8_t retry)
```

!!! summary "引数"
	- uint8_t `retry` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(MR, 0x0000)
```

!!! summary "引数"
	- 0x0000 `` 



### __GP_REGISTER_N()



```c
W5100Class::__GP_REGISTER_N(GAR, 0x0001, 4)
```

!!! summary "引数"
	- 4 `` 



### __GP_REGISTER_N()



```c
W5100Class::__GP_REGISTER_N(SUBR, 0x0005, 4)
```

!!! summary "引数"
	- 4 `` 



### __GP_REGISTER_N()



```c
W5100Class::__GP_REGISTER_N(SHAR, 0x0009, 6)
```

!!! summary "引数"
	- 6 `` 



### __GP_REGISTER_N()



```c
W5100Class::__GP_REGISTER_N(SIPR, 0x000F, 4)
```

!!! summary "引数"
	- 4 `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(IR, 0x0015)
```

!!! summary "引数"
	- 0x0015 `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(IMR, 0x0016)
```

!!! summary "引数"
	- 0x0016 `` 



### __GP_REGISTER16()



```c
W5100Class::__GP_REGISTER16(RTR, 0x0017)
```

!!! summary "引数"
	- 0x0017 `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(RCR, 0x0019)
```

!!! summary "引数"
	- 0x0019 `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(RMSR, 0x001A)
```

!!! summary "引数"
	- 0x001A `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(TMSR, 0x001B)
```

!!! summary "引数"
	- 0x001B `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(PATR, 0x001C)
```

!!! summary "引数"
	- 0x001C `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(PTIMER, 0x0028)
```

!!! summary "引数"
	- 0x0028 `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(PMAGIC, 0x0029)
```

!!! summary "引数"
	- 0x0029 `` 



### __GP_REGISTER_N()



```c
W5100Class::__GP_REGISTER_N(UIPR, 0x002A, 4)
```

!!! summary "引数"
	- 4 `` 



### __GP_REGISTER16()



```c
W5100Class::__GP_REGISTER16(UPORT, 0x002E)
```

!!! summary "引数"
	- 0x002E `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(VERSIONR_W5200, 0x001F)
```

!!! summary "引数"
	- 0x001F `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(VERSIONR_W5500, 0x0039)
```

!!! summary "引数"
	- 0x0039 `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(PSTATUS_W5200, 0x0035)
```

!!! summary "引数"
	- 0x0035 `` 



### __GP_REGISTER8()



```c
W5100Class::__GP_REGISTER8(PHYCFGR_W5500, 0x002E)
```

!!! summary "引数"
	- 0x002E `` 



### __SOCKET_REGISTER8()



```c
W5100Class::__SOCKET_REGISTER8(SnMR, 0x0000) __SOCKET_REGISTER8(SnCR
```

!!! summary "引数"
	- 0x0000 `` 



### __SOCKET_REGISTER8()



```c
W5100Class::__SOCKET_REGISTER8(SnIR, 0x0002) __SOCKET_REGISTER8(SnSR
```

!!! summary "引数"
	- 0x0002 `` 



### __SOCKET_REGISTER16()



```c
W5100Class::__SOCKET_REGISTER16(SnPORT, 0x0004) __SOCKET_REGISTER_N(SnDHAR
```

!!! summary "引数"
	- 0x0004 `` 



### __SOCKET_REGISTER_N()



```c
W5100Class::__SOCKET_REGISTER_N(SnDIPR, 0x000C, 4) __SOCKET_REGISTER16(SnDPORT
```

!!! summary "引数"
	- 4 `` 



### __SOCKET_REGISTER16()



```c
W5100Class::__SOCKET_REGISTER16(SnMSSR, 0x0012) __SOCKET_REGISTER8(SnPROTO
```

!!! summary "引数"
	- 0x0012 `` 



### __SOCKET_REGISTER8()



```c
W5100Class::__SOCKET_REGISTER8(SnTOS, 0x0015) __SOCKET_REGISTER8(SnTTL
```

!!! summary "引数"
	- 0x0015 `` 



### __SOCKET_REGISTER8()



```c
W5100Class::__SOCKET_REGISTER8(SnRX_SIZE, 0x001E) __SOCKET_REGISTER8(SnTX_SIZE
```

!!! summary "引数"
	- 0x001E `` 



### __SOCKET_REGISTER16()



```c
W5100Class::__SOCKET_REGISTER16(SnTX_FSR, 0x0020) __SOCKET_REGISTER16(SnTX_RD
```

!!! summary "引数"
	- 0x0020 `` 



### __SOCKET_REGISTER16()



```c
W5100Class::__SOCKET_REGISTER16(SnTX_WR, 0x0024) __SOCKET_REGISTER16(SnRX_RSR
```

!!! summary "引数"
	- 0x0024 `` 



### __SOCKET_REGISTER16()



```c
W5100Class::__SOCKET_REGISTER16(SnRX_RD, 0x0028) __SOCKET_REGISTER16(SnRX_WR
```

!!! summary "引数"
	- 0x0028 `` 



