# google::protobuf::compiler::c::MessageFieldGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_message_field_generator.html)

## メンバー

### MessageFieldGenerator()



```c
google::protobuf::compiler::c::MessageFieldGenerator::MessageFieldGenerator(const FieldDescriptor *descriptor)
```

!!! summary "引数"
	- constFieldDescriptor * `descriptor` 



### ~MessageFieldGenerator()



```c
google::protobuf::compiler::c::MessageFieldGenerator::~MessageFieldGenerator()
```



### GenerateStructMembers()



```c
void google::protobuf::compiler::c::MessageFieldGenerator::GenerateStructMembers(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDescriptorInitializer()



```c
void google::protobuf::compiler::c::MessageFieldGenerator::GenerateDescriptorInitializer(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GetDefaultValue()



```c
string google::protobuf::compiler::c::MessageFieldGenerator::GetDefaultValue(void) const
```

!!! note "戻り値"
	string



### GenerateStaticInit()



```c
void google::protobuf::compiler::c::MessageFieldGenerator::GenerateStaticInit(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



