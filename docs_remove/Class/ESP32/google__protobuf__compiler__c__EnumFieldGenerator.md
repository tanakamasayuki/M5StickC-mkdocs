# google::protobuf::compiler::c::EnumFieldGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_enum_field_generator.html)

## メンバー

### EnumFieldGenerator()



```c
google::protobuf::compiler::c::EnumFieldGenerator::EnumFieldGenerator(const FieldDescriptor *descriptor)
```

!!! summary "引数"
	- constFieldDescriptor * `descriptor` 



### ~EnumFieldGenerator()



```c
google::protobuf::compiler::c::EnumFieldGenerator::~EnumFieldGenerator()
```



### GenerateStructMembers()



```c
void google::protobuf::compiler::c::EnumFieldGenerator::GenerateStructMembers(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDescriptorInitializer()



```c
void google::protobuf::compiler::c::EnumFieldGenerator::GenerateDescriptorInitializer(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GetDefaultValue()



```c
string google::protobuf::compiler::c::EnumFieldGenerator::GetDefaultValue(void) const
```

!!! note "戻り値"
	string



### GenerateStaticInit()



```c
void google::protobuf::compiler::c::EnumFieldGenerator::GenerateStaticInit(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



