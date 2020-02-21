# asio::ip::basic_resolver_iterator

An iterator over the entries produced by a resolver. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1basic__resolver__iterator.html)

## メンバー











### basic_resolver_iterator()
Default constructor creates an end iterator.


```c
asio::ip::basic_resolver_iterator< InternetProtocol >::basic_resolver_iterator()
```



### basic_resolver_iterator()
Copy constructor.


```c
asio::ip::basic_resolver_iterator< InternetProtocol >::basic_resolver_iterator(const basic_resolver_iterator &other)
```

!!! summary "引数"
	- const& `other` 



### operator=()
Assignment operator.


```c
basic_resolver_iterator& asio::ip::basic_resolver_iterator< InternetProtocol >::operator=(const basic_resolver_iterator &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	basic_resolver_iterator&



### operator *()
Dereference an iterator.


```c
const basic_resolver_entry<InternetProtocol>& asio::ip::basic_resolver_iterator< InternetProtocol >::operator *() const
```

!!! note "戻り値"
	const< InternetProtocol > &



### operator->()
Dereference an iterator.


```c
const basic_resolver_entry<InternetProtocol>* asio::ip::basic_resolver_iterator< InternetProtocol >::operator->() const
```

!!! note "戻り値"
	const< InternetProtocol > *



### operator++()
Increment operator (prefix).


```c
basic_resolver_iterator& asio::ip::basic_resolver_iterator< InternetProtocol >::operator++()
```

!!! note "戻り値"
	basic_resolver_iterator&



### operator++()
Increment operator (postfix).


```c
basic_resolver_iterator asio::ip::basic_resolver_iterator< InternetProtocol >::operator++(int)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	basic_resolver_iterator







