# google::protobuf::compiler::c::EnumGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_enum_generator.html)

## メンバー

### EnumGenerator()



```c
google::protobuf::compiler::c::EnumGenerator::EnumGenerator(const EnumDescriptor *descriptor, const string &dllexport_decl)
```

!!! summary "引数"
	- constEnumDescriptor * `descriptor` 
	- const& `dllexport_decl` 



### ~EnumGenerator()



```c
google::protobuf::compiler::c::EnumGenerator::~EnumGenerator()
```



### GenerateDefinition()



```c
void google::protobuf::compiler::c::EnumGenerator::GenerateDefinition(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDescriptorDeclarations()



```c
void google::protobuf::compiler::c::EnumGenerator::GenerateDescriptorDeclarations(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateEnumDescriptor()



```c
void google::protobuf::compiler::c::EnumGenerator::GenerateEnumDescriptor(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateValueInitializer()



```c
void google::protobuf::compiler::c::EnumGenerator::GenerateValueInitializer(io::Printer *printer, int index)
```

!!! summary "引数"
	- io::Printer * `printer` 
	- int `index` 



