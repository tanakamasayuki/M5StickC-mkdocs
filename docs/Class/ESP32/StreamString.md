# StreamString



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_stream_string.html)

## メンバー

### write()


You should have received a copy of the GNU Lesser General Public License along with this library; if not, write to the Free Software Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301 USA 
```c
size_t StreamString::write(const uint8_t *buffer, size_t size) override
```

!!! summary "引数"
	- const* `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### write()



```c
size_t StreamString::write(uint8_t data) override
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



### available()



```c
int StreamString::available() override
```

!!! note "戻り値"
	int



### read()



```c
int StreamString::read() override
```

!!! note "戻り値"
	int



### peek()



```c
int StreamString::peek() override
```

!!! note "戻り値"
	int



### flush()



```c
void StreamString::flush() override
```



