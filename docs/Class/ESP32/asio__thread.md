# asio::thread

A simple abstraction for starting threads. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1thread.html)

## メンバー

### thread()
Start a new thread that executes the supplied function.

This constructor creates a new thread that will execute the given function or function object.
```c
asio::thread::thread(Function f)
```

!!! summary "引数"
	- Function `f` The function or function object to be run in the thread. The function signature must be: 



### ~thread()
Destructor.


```c
asio::thread::~thread()
```



### join()
Wait for the thread to exit.

If this function is not called before the thread object is destroyed, the thread itself will continue to run until completion. You will, however, no longer have the ability to wait for it to exit. 
```c
void asio::thread::join()
```



