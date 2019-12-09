# sys
## インスタンス
### stderr [[FileIO](../../class/io.FileIO/)]
```python
sys.stderr = FileIO()
```
### stdin [[FileIO](../../class/io.FileIO/)]
```python
sys.stdin = FileIO()
```
### stdout [[FileIO](../../class/io.FileIO/)]
```python
sys.stdout = FileIO()
```
## 関数
### exit
```python
sys.exit()
```
### print\_exception
```python
sys.print_exception()
```
## 定数
### \_\_name\_\_
```python
sys.__name__ = str('sys')
```
### argv
```python
sys.argv = list([])
```
### byteorder
```python
sys.byteorder = str('little')
```
### implementation
```python
sys.implementation = tuple((name='micropython', version=(1, 11, 0)))
```
### maxsize
```python
sys.maxsize = int(2147483647)
```
### modules
```python
sys.modules = dict({'units._button': <module 'units._button' from 'flowlib/units/_button.py'>, 'unit': <module 'unit' from 'flowlib/unit.py'>, 'modules': <module 'modules'>, 'hats._finger': <module 'hats._finger' from 'flowlib/hats/_finger.py'>, 'button': <module 'button' from 'flowlib/button.py'>, 'units._mlx90640': <module 'units._mlx90640' from 'flowlib/units/_mlx90640.py'>, 'units._pbhub': <module 'units._pbhub' from 'flowlib/units/_pbhub.py'>, 'units._relay': <module 'units._relay' from 'flowlib/units/_relay.py'>, 'units._tracker': <module 'units._tracker' from 'flowlib/units/_tracker.py'>, 'units._joystick': <module 'units._joystick' from 'flowlib/units/_joystick.py'>, 'units._weight': <module 'units._weight' from 'flowlib/units/_weight.py'>, 'microWebTemplate': <module 'microWebTemplate' from 'microWebTemplate.py'>, 'statechoose': <module 'statechoose' from 'flowlib/statechoose.py'>, 'upip': <module 'upip' from 'upip.py'>, 'usocket': <module 'usocket'>, 'hw': <module 'hw'>, 'hats._joyC': <module 'hats._joyC' from 'flowlib/hats/_joyC.py'>, 'units._light': <module 'units._light' from 'flowlib/units/_light.py'>, 'units._gps': <module 'units._gps' from 'flowlib/units/_gps.py'>, 'lib.time_ex': <module 'lib.time_ex' from 'flowlib/lib/time_ex.py'>, 'app_manage': <module 'app_manage' from 'flowlib/app_manage.py'>, 'peripheral': <module 'peripheral' from 'flowlib/peripheral.py'>, 'numbers': <module 'numbers' from 'flowlib/lib/numbers.py'>, 'upip_utarfile': <module 'upip_utarfile' from 'upip_utarfile.py'>, 'hats._servo': <module 'hats._servo' from 'flowlib/hats/_servo.py'>, 'hw.axp192': <module 'hw.axp192' from 'flowlib/hw/axp192.py'>, 'mstate': <module 'mstate' from 'flowlib/lib/mstate.py'>, 'uiflow': <module 'uiflow' from 'flowlib/uiflow.py'>, 'hats': <module 'hats'>, 'neopixel': <module 'neopixel' from 'neopixel.py'>, 'hats._pir': <module 'hats._pir' from 'flowlib/hats/_pir.py'>, 'hats._beetlec': <module 'hats._beetlec' from 'flowlib/hats/_beetlec.py'>, 'bmp280': <module 'bmp280' from 'flowlib/lib/bmp280.py'>, 'wave': <module 'wave' from 'flowlib/lib/wave.py'>, 'hats._adc': <module 'hats._adc' from 'flowlib/hats/_adc.py'>, 'dht12': <module 'dht12' from 'flowlib/lib/dht12.py'>, 'hats._yun': <module 'hats._yun' from 'flowlib/hats/_yun.py'>, 'hats._env': <module 'hats._env' from 'flowlib/hats/_env.py'>, 'hats._servos': <module 'hats._servos' from 'flowlib/hats/_servos.py'>, 'socket': <module 'usocket'>, 'network': <module 'network'>, 'utils': <module 'utils' from 'flowlib/utils.py'>, 'logging': <module 'logging' from 'logging.py'>, 'hats._joystick': <module 'hats._joystick' from 'flowlib/hats/_joystick.py'>, 'chunk': <module 'chunk' from 'flowlib/lib/chunk.py'>, 'hats._ncir': <module 'hats._ncir' from 'flowlib/hats/_ncir.py'>, 'units._dual_button': <module 'units._dual_button' from 'flowlib/units/_dual_button.py'>, 'units._ext_io': <module 'units._ext_io' from 'flowlib/units/_ext_io.py'>, 'i2c_bus': <module 'i2c_bus' from 'flowlib/i2c_bus.py'>, 'units._adc': <module 'units._adc' from 'flowlib/units/_adc.py'>, 'hats._puppy': <module 'hats._puppy' from 'flowlib/hats/_puppy.py'>, 'm5uart': <module ''>, 'units._makey': <module 'units._makey' from 'flowlib/units/_makey.py'>, 'microWebSocket': <module 'microWebSocket' from 'microWebSocket.py'>, 'units._env': <module 'units._env' from 'flowlib/units/_env.py'>, 'units._finger': <module 'units._finger' from 'flowlib/units/_finger.py'>, 'timeSchedule': <module 'timeSchedule' from 'flowlib/timeSchedule.py'>, 'units._ncir': <module 'units._ncir' from 'flowlib/units/_ncir.py'>, 'hat': <module 'hat' from 'flowlib/hat.py'>, 'hats._bugc': <module 'hats._bugc' from 'flowlib/hats/_bugc.py'>, 'hw._led': <module 'hw._led' from 'flowlib/hw/_led.py'>, 'flowSetup': <module 'flowSetup' from 'flowlib/flowSetup.py'>, 'units._rgb_multi': <module 'units._rgb_multi' from 'flowlib/units/_rgb_multi.py'>, 'units._pahub': <module 'units._pahub' from 'flowlib/units/_pahub.py'>, 'units._pir': <module 'units._pir' from 'flowlib/units/_pir.py'>, 'units._rfid': <module 'units._rfid' from 'flowlib/units/_rfid.py'>, 'units._rgb': <module 'units._rgb' from 'flowlib/units/_rgb.py'>, 'units._servo': <module 'units._servo' from 'flowlib/units/_servo.py'>, 'units._tof': <module 'units._tof' from 'flowlib/units/_tof.py'>, 'hw.bm8563': <module 'hw.bm8563' from 'flowlib/hw/bm8563.py'>, 'units': <module 'units'>, 'units._angle': <module 'units._angle' from 'flowlib/units/_angle.py'>, 'hats._dac': <module 'hats._dac' from 'flowlib/hats/_dac.py'>, 'hats._tof': <module 'hats._tof' from 'flowlib/hats/_tof.py'>, 'm5stack': <module 'm5stack' from 'flowlib/m5stack.py'>, 'hats._roverc': <module 'hats._roverc' from 'flowlib/hats/_roverc.py'>, 'hats._speaker': <module 'hats._speaker' from 'flowlib/hats/_speaker.py'>, 'units._color': <module 'units._color' from 'flowlib/units/_color.py'>, 'units._dac': <module 'units._dac' from 'flowlib/units/_dac.py'>, 'units._cardKB': <module 'units._cardKB' from 'flowlib/units/_cardKB.py'>, 'microWebSrv': <module 'microWebSrv' from 'microWebSrv.py'>, 'units._earth': <module 'units._earth' from 'flowlib/units/_earth.py'>, 'units._ir': <module 'units._ir' from 'flowlib/units/_ir.py'>, 'lib': <module 'lib'>, 'hats._cardKB': <module 'hats._cardKB' from 'flowlib/hats/_cardKB.py'>, 'hats._mlx90640': <module 'hats._mlx90640' from 'flowlib/hats/_mlx90640.py'>})
```
### path
```python
sys.path = list(['', '/lib', 'flowlib', 'flowlib/lib'])
```
### platform
```python
sys.platform = str('esp32')
```
### version
```python
sys.version = str('3.4.0')
```
### version\_info
```python
sys.version_info = tuple((3, 4, 0))
```
