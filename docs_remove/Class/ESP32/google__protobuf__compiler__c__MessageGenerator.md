# google::protobuf::compiler::c::MessageGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_message_generator.html)

## メンバー

### MessageGenerator()



```c
google::protobuf::compiler::c::MessageGenerator::MessageGenerator(const Descriptor *descriptor, const string &dllexport_decl)
```

!!! summary "引数"
	- constDescriptor * `descriptor` 
	- const& `dllexport_decl` 



### ~MessageGenerator()



```c
google::protobuf::compiler::c::MessageGenerator::~MessageGenerator()
```



### GenerateStructTypedef()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateStructTypedef(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDescriptorDeclarations()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateDescriptorDeclarations(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateClosureTypedef()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateClosureTypedef(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateEnumDefinitions()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateEnumDefinitions(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateStructDefinition()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateStructDefinition(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateStructStaticInitMacro()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateStructStaticInitMacro(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateHelperFunctionDeclarations()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateHelperFunctionDeclarations(io::Printer *printer, bool is_submessage)
```

!!! summary "引数"
	- io::Printer * `printer` 
	- bool `is_submessage` 



### GenerateMessageDescriptor()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateMessageDescriptor(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateHelperFunctionDefinitions()



```c
void google::protobuf::compiler::c::MessageGenerator::GenerateHelperFunctionDefinitions(io::Printer *printer, bool is_submessage)
```

!!! summary "引数"
	- io::Printer * `printer` 
	- bool `is_submessage` 



