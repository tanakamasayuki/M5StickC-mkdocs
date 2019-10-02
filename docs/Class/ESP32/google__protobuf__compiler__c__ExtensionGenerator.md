# google::protobuf::compiler::c::ExtensionGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_extension_generator.html)

## メンバー

### ExtensionGenerator()



```c
google::protobuf::compiler::c::ExtensionGenerator::ExtensionGenerator(const FieldDescriptor *descriptor, const string &dllexport_decl)
```

!!! summary "引数"
	- constFieldDescriptor * `descriptor` 
	- const& `dllexport_decl` 



### ~ExtensionGenerator()



```c
google::protobuf::compiler::c::ExtensionGenerator::~ExtensionGenerator()
```



### GenerateDeclaration()



```c
void google::protobuf::compiler::c::ExtensionGenerator::GenerateDeclaration(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDefinition()



```c
void google::protobuf::compiler::c::ExtensionGenerator::GenerateDefinition(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



