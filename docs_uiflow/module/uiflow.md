# uiflow

## モジュール

### [axp192](../axp192/)
```python
uiflow.axp192
```

### [binascii](../binascii/)
```python
uiflow.binascii
```

### [bm8563](../bm8563/)
```python
uiflow.bm8563
```

### [display](../display/)
```python
uiflow.display
```

### [gc](../gc/)
```python
uiflow.gc
```

### [m5base](../m5base/)
```python
uiflow.m5base
```

### [machine](../machine/)
```python
uiflow.machine
```

### [os](../os/)
```python
uiflow.os
```

### [time](../time/)
```python
uiflow.time
```

### [timeSchedule](../timeSchedule/)
```python
uiflow.timeSchedule
```

### [time\_ex](../time_ex/)
```python
uiflow.time_ex
```
## クラス定義
### [Btn](../../class/uiflow.Btn/)
```python
uiflow.Btn
```
### [BtnChild](../../class/uiflow.BtnChild/)
```python
uiflow.BtnChild
```
### [flowExit](../../class/uiflow.flowExit/)
```python
uiflow.flowExit
```
## インスタンス
### M5Led [[M5Led](../../class/hw._led.M5Led/)]
```python
uiflow.M5Led = M5Led()
```
### axp [[Axp192](../../class/axp192.Axp192/)]
```python
uiflow.axp = Axp192()
```
### btn [[Btn](../../class/uiflow.Btn/)]
```python
uiflow.btn = Btn()
```
### btnA [[BtnChild](../../class/uiflow.BtnChild/)]
```python
uiflow.btnA = BtnChild()
```
### btnB [[BtnChild](../../class/uiflow.BtnChild/)]
```python
uiflow.btnB = BtnChild()
```
### lcd [[TFT](../../class/display.TFT/)]
```python
uiflow.lcd = TFT()
```
### rtc [[Bm8563](../../class/bm8563.Bm8563/)]
```python
uiflow.rtc = Bm8563()
```
### timEx [[TimerEx](../../class/time_ex.TimerEx/)]
```python
uiflow.timEx = TimerEx()
```
### timerSch [[timeSch](../../class/timeSchedule.timeSch/)]
```python
uiflow.timerSch = timeSch()
```
## 関数
### cfgRead
```python
uiflow.cfgRead()
```
### cfgWrite
```python
uiflow.cfgWrite()
```
### const
```python
uiflow.const()
```
### core\_start
```python
uiflow.core_start()
```
### flowDeinit
```python
uiflow.flowDeinit()
```
### getP2PData
```python
uiflow.getP2PData()
```
### loopExit
```python
uiflow.loopExit()
```
### loopSetIdle
```python
uiflow.loopSetIdle()
```
### loopState
```python
uiflow.loopState()
```
### modeSet
```python
uiflow.modeSet()
```
### reboot
```python
uiflow.reboot()
```
### remoteInit
```python
uiflow.remoteInit()
```
### resetDefault
```python
uiflow.resetDefault()
```
### sendP2PData
```python
uiflow.sendP2PData()
```
### setP2PData
```python
uiflow.setP2PData()
```
### start
```python
uiflow.start()
```
### startBeep
```python
uiflow.startBeep()
```
### wait
```python
uiflow.wait()
```
### wait\_ms
```python
uiflow.wait_ms()
```
## 定数
### \_\_file\_\_
```python
uiflow.__file__ = str('flowlib/uiflow.py')
```
### \_\_name\_\_
```python
uiflow.__name__ = str('uiflow')
```
### \_exitState
```python
uiflow._exitState = bool(False)
```
### \_is\_remote
```python
uiflow._is_remote = bool(False)
```
### \_nextP2PTime
```python
uiflow._nextP2PTime = int(0)
```
### \_p2pData
```python
uiflow._p2pData = NoneType(>>>)
```
### apikey
```python
uiflow.apikey = str('C8E567C6')
```
### config\_normal
```python
uiflow.config_normal = str('{\n    "start": "flow",\n    "mode": "internet",\n    "server": "Flow.m5stack.com", \n    "wifi": {\n        "ssid": "",\n        "password": ""\n    }\n}\n')
```
### node\_id
```python
uiflow.node_id = str('d8a01d515dbc')
```
