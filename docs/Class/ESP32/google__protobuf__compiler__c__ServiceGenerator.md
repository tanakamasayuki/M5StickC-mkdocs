# google::protobuf::compiler::c::ServiceGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_service_generator.html)

## メンバー

###  descriptor_

```c
const ServiceDescriptor* google::protobuf::compiler::c::ServiceGenerator::descriptor_
```


###  vars_

```c
std::map<string, string> google::protobuf::compiler::c::ServiceGenerator::vars_
```


### ServiceGenerator()



```c
google::protobuf::compiler::c::ServiceGenerator::ServiceGenerator(const ServiceDescriptor *descriptor, const string &dllexport_decl)
```

!!! summary "引数"
	- constServiceDescriptor * `descriptor` 
	- const& `dllexport_decl` 



### ~ServiceGenerator()



```c
google::protobuf::compiler::c::ServiceGenerator::~ServiceGenerator()
```



### GenerateMainHFile()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateMainHFile(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateVfuncs()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateVfuncs(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateInitMacros()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateInitMacros(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateDescriptorDeclarations()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateDescriptorDeclarations(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateCallersDeclarations()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateCallersDeclarations(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateCFile()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateCFile(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateServiceDescriptor()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateServiceDescriptor(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateInit()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateInit(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateCallersImplementations()



```c
void google::protobuf::compiler::c::ServiceGenerator::GenerateCallersImplementations(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GOOGLE_DISALLOW_EVIL_CONSTRUCTORS()



```c
google::protobuf::compiler::c::ServiceGenerator::GOOGLE_DISALLOW_EVIL_CONSTRUCTORS(ServiceGenerator)
```

!!! summary "引数"
	- ServiceGenerator `` 



