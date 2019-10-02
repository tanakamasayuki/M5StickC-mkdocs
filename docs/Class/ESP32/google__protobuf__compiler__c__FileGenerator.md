# google::protobuf::compiler::c::FileGenerator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classgoogle_1_1protobuf_1_1compiler_1_1c_1_1_file_generator.html)

## メンバー

### FileGenerator()



```c
google::protobuf::compiler::c::FileGenerator::FileGenerator(const FileDescriptor *file, const string &dllexport_decl)
```

!!! summary "引数"
	- constFileDescriptor * `file` 
	- const& `dllexport_decl` 



### ~FileGenerator()



```c
google::protobuf::compiler::c::FileGenerator::~FileGenerator()
```



### GenerateHeader()



```c
void google::protobuf::compiler::c::FileGenerator::GenerateHeader(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



### GenerateSource()



```c
void google::protobuf::compiler::c::FileGenerator::GenerateSource(io::Printer *printer)
```

!!! summary "引数"
	- io::Printer * `printer` 



