# google::protobuf::compiler::c::PrimitiveFieldGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_primitive_field_generator.html)

## メンバー

### PrimitiveFieldGenerator()



```c
google::protobuf::compiler::c::PrimitiveFieldGenerator::PrimitiveFieldGenerator(const FieldDescriptor *descriptor)
```

!!! summary "引数"
	- constFieldDescriptor * `descriptor` 



### ~PrimitiveFieldGenerator()



```c
google::protobuf::compiler::c::PrimitiveFieldGenerator::~PrimitiveFieldGenerator()
```



### GenerateStructMembers()



```c
void google::protobuf::compiler::c::PrimitiveFieldGenerator::GenerateStructMembers(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDescriptorInitializer()



```c
void google::protobuf::compiler::c::PrimitiveFieldGenerator::GenerateDescriptorInitializer(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GetDefaultValue()



```c
string google::protobuf::compiler::c::PrimitiveFieldGenerator::GetDefaultValue(void) const
```

!!! note "戻り値"
	string



### GenerateStaticInit()



```c
void google::protobuf::compiler::c::PrimitiveFieldGenerator::GenerateStaticInit(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



