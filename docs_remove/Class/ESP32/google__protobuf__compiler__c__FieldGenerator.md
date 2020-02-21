# google::protobuf::compiler::c::FieldGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_field_generator.html)

## メンバー

### FieldGenerator()



```c
google::protobuf::compiler::c::FieldGenerator::FieldGenerator(const FieldDescriptor *descriptor)
```

!!! summary "引数"
	- constFieldDescriptor * `descriptor` 



### ~FieldGenerator()



```c
virtual google::protobuf::compiler::c::FieldGenerator::~FieldGenerator()
```



### GenerateStructMembers()



```c
virtual void google::protobuf::compiler::c::FieldGenerator::GenerateStructMembers(io::Printer *printer) const =0
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDescriptorInitializer()



```c
virtual void google::protobuf::compiler::c::FieldGenerator::GenerateDescriptorInitializer(io::Printer *printer) const =0
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDefaultValueDeclarations()



```c
virtual void google::protobuf::compiler::c::FieldGenerator::GenerateDefaultValueDeclarations(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDefaultValueImplementations()



```c
virtual void google::protobuf::compiler::c::FieldGenerator::GenerateDefaultValueImplementations(io::Printer *printer) const
```

!!! summary "引数"
	- io::Printer * `printer` 



### GetDefaultValue()



```c
virtual string google::protobuf::compiler::c::FieldGenerator::GetDefaultValue() const =0
```

!!! note "戻り値"
	string



### GenerateStaticInit()



```c
virtual void google::protobuf::compiler::c::FieldGenerator::GenerateStaticInit(io::Printer *printer) const =0
```

!!! summary "引数"
	- io::Printer * `printer` 



