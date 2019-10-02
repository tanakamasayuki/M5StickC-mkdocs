# BLEUtils

A set of general BLE utilities. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_utils.html)

## メンバー

### addressTypeToString()
Convert an esp_ble_addr_type_t to a string representation.


```c
const char * BLEUtils::addressTypeToString(esp_ble_addr_type_t type)
```

!!! summary "引数"
	- esp_ble_addr_type_t `type` 

!!! note "戻り値"
	constchar *



### adFlagsToString()
Convert the BLE Advertising Data flags to a string.


```c
std::string BLEUtils::adFlagsToString(uint8_t adFlags)
```

!!! summary "引数"
	- uint8_t `adFlags` The flags to convert 

!!! note "戻り値"
	std::string std::string A string representation of the advertising flags. 



### advTypeToString()
Given an advertising type, return a string representation of the type.



```c
const char * BLEUtils::advTypeToString(uint8_t advType)
```

!!! summary "引数"
	- uint8_t `advType` 

!!! note "戻り値"
	constchar *



### buildHexData()
Create a hex representation of data.


```c
char * BLEUtils::buildHexData(uint8_t *target, uint8_t *source, uint8_t length)
```

!!! summary "引数"
	- uint8_t* `target` Where to write the hex string. If this is null, we malloc storage. 
	- uint8_t* `source` The start of the binary data. 
	- uint8_t `length` The length of the data to convert. 

!!! note "戻り値"
	char * A pointer to the formatted buffer. 



### buildPrintData()
Build a printable string of memory range. Create a string representation of a piece of memory. Only printable characters will be included while those that are not printable will be replaced with '.'.


```c
std::string BLEUtils::buildPrintData(uint8_t *source, size_t length)
```

!!! summary "引数"
	- uint8_t* `source` Start of memory. 
	- size_t `length` Length of memory. 

!!! note "戻り値"
	std::string A string representation of a piece of memory. 



### characteristicPropertiesToString()
Convert characteristic properties into a string representation.


```c
std::string BLEUtils::characteristicPropertiesToString(esp_gatt_char_prop_t prop)
```

!!! summary "引数"
	- esp_gatt_char_prop_t `prop` Characteristic properties. 

!!! note "戻り値"
	std::string A string representation of characteristic properties. 



### devTypeToString()
Convert a BLE device type to a string.


```c
const char * BLEUtils::devTypeToString(esp_bt_dev_type_t type)
```

!!! summary "引数"
	- esp_bt_dev_type_t `type` The device type. 

!!! note "戻り値"
	constchar *



### buildGattId()



```c
esp_gatt_id_t BLEUtils::buildGattId(esp_bt_uuid_t uuid, uint8_t inst_id=0)
```

!!! summary "引数"
	- esp_bt_uuid_t `uuid` 
	- uint8_t `inst_id` 

!!! note "戻り値"
	esp_gatt_id_t



### buildGattSrvcId()



```c
esp_gatt_srvc_id_t BLEUtils::buildGattSrvcId(esp_gatt_id_t gattId, bool is_primary=true)
```

!!! summary "引数"
	- esp_gatt_id_t `gattId` 
	- bool `is_primary` 

!!! note "戻り値"
	esp_gatt_srvc_id_t



### dumpGapEvent()
Dump the GAP event to the log.


```c
void BLEUtils::dumpGapEvent(esp_gap_ble_cb_event_t event, esp_ble_gap_cb_param_t *param)
```

!!! summary "引数"
	- esp_gap_ble_cb_event_t `event` 
	- esp_ble_gap_cb_param_t* `param` 



### dumpGattClientEvent()
Decode and dump a GATT client event


```c
void BLEUtils::dumpGattClientEvent(esp_gattc_cb_event_t event, esp_gatt_if_t gattc_if, esp_ble_gattc_cb_param_t *evtParam)
```

!!! summary "引数"
	- esp_gattc_cb_event_t `event` The type of event received. 
	- esp_gatt_if_t `gattc_if` 
	- esp_ble_gattc_cb_param_t* `evtParam` The data associated with the event. 



### dumpGattServerEvent()
Dump the details of a GATT server event. A GATT  event is a callback received from the BLE subsystem when we are acting as a BLE server. The callback indicates the type of event in the  field. The  is a union of structures where we can use the  to indicate which of the structures has been populated and hence is valid.


```c
void BLEUtils::dumpGattServerEvent(esp_gatts_cb_event_t event, esp_gatt_if_t gatts_if, esp_ble_gatts_cb_param_t *evtParam)
```

!!! summary "引数"
	- esp_gatts_cb_event_t `event` The event type that was posted. 
	- esp_gatt_if_t `gatts_if` 
	- esp_ble_gatts_cb_param_t* `evtParam` A union of structures only one of which is populated. 



### eventTypeToString()
Convert a BLE event type to a string.


```c
const char * BLEUtils::eventTypeToString(esp_ble_evt_type_t eventType)
```

!!! summary "引数"
	- esp_ble_evt_type_t `eventType` The event type. 

!!! note "戻り値"
	constchar * The event type as a string. 



### findByAddress()



```c
static BLEClient* BLEUtils::findByAddress(BLEAddress address)
```

!!! summary "引数"
	- BLEAddress `address` 

!!! note "戻り値"
	BLEClient*



### findByConnId()



```c
static BLEClient* BLEUtils::findByConnId(uint16_t conn_id)
```

!!! summary "引数"
	- uint16_t `conn_id` 

!!! note "戻り値"
	BLEClient*



### gapEventToString()
Convert a BT GAP event type to a string representation.


```c
const char * BLEUtils::gapEventToString(uint32_t eventType)
```

!!! summary "引数"
	- uint32_t `eventType` The type of event. 

!!! note "戻り値"
	constchar * A string representation of the event type. 



### gattCharacteristicUUIDToString()



```c
std::string BLEUtils::gattCharacteristicUUIDToString(uint32_t characteristicUUID)
```

!!! summary "引数"
	- uint32_t `characteristicUUID` 

!!! note "戻り値"
	std::string



### gattClientEventTypeToString()



```c
std::string BLEUtils::gattClientEventTypeToString(esp_gattc_cb_event_t eventType)
```

!!! summary "引数"
	- esp_gattc_cb_event_t `eventType` 

!!! note "戻り値"
	std::string



### gattCloseReasonToString()
Convert a close/disconnect reason to a string.


```c
std::string BLEUtils::gattCloseReasonToString(esp_gatt_conn_reason_t reason)
```

!!! summary "引数"
	- esp_gatt_conn_reason_t `reason` The close reason. 

!!! note "戻り値"
	std::string A string representation of the reason. 



### gattcServiceElementToString()
Return a string representation of an .



```c
std::string BLEUtils::gattcServiceElementToString(esp_gattc_service_elem_t *pGATTCServiceElement)
```

!!! summary "引数"
	- esp_gattc_service_elem_t* `pGATTCServiceElement` 

!!! note "戻り値"
	std::string A string representation of an . 



### gattDescriptorUUIDToString()
Given the UUID for a BLE defined descriptor, return its string representation.


```c
std::string BLEUtils::gattDescriptorUUIDToString(uint32_t descriptorUUID)
```

!!! summary "引数"
	- uint32_t `descriptorUUID` UUID of the descriptor to be returned as a string. 

!!! note "戻り値"
	std::string The string representation of a descriptor UUID. 



### gattServerEventTypeToString()
Return a string representation of a GATT server event code.


```c
std::string BLEUtils::gattServerEventTypeToString(esp_gatts_cb_event_t eventType)
```

!!! summary "引数"
	- esp_gatts_cb_event_t `eventType` A GATT server event code. 

!!! note "戻り値"
	std::string A string representation of the GATT server event code. 



### gattServiceIdToString()
Convert an esp_gatt_srvc_id_t to a string.


```c
std::string BLEUtils::gattServiceIdToString(esp_gatt_srvc_id_t srvcId)
```

!!! summary "引数"
	- esp_gatt_srvc_id_t `srvcId` 

!!! note "戻り値"
	std::string



### gattServiceToString()



```c
std::string BLEUtils::gattServiceToString(uint32_t serviceId)
```

!!! summary "引数"
	- uint32_t `serviceId` 

!!! note "戻り値"
	std::string



### gattStatusToString()
Convert a GATT status to a string.


```c
std::string BLEUtils::gattStatusToString(esp_gatt_status_t status)
```

!!! summary "引数"
	- esp_gatt_status_t `status` The status to convert. 

!!! note "戻り値"
	std::string A string representation of the status. 



### getMember()



```c
std::string BLEUtils::getMember(uint32_t memberId)
```

!!! summary "引数"
	- uint32_t `memberId` 

!!! note "戻り値"
	std::string



### registerByAddress()



```c
static void BLEUtils::registerByAddress(BLEAddress address, BLEClient *pDevice)
```

!!! summary "引数"
	- BLEAddress `address` 
	- BLEClient* `pDevice` 



### registerByConnId()



```c
static void BLEUtils::registerByConnId(uint16_t conn_id, BLEClient *pDevice)
```

!!! summary "引数"
	- uint16_t `conn_id` 
	- BLEClient* `pDevice` 



### searchEventTypeToString()
convert a GAP search event to a string.


```c
const char * BLEUtils::searchEventTypeToString(esp_gap_search_evt_t searchEvt)
```

!!! summary "引数"
	- esp_gap_search_evt_t `searchEvt` 

!!! note "戻り値"
	constchar * The search event type as a string. 



