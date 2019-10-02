# asio::ssl::context



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1context.html)

## メンバー



### context()
Constructor.


```c
ASIO_DECL asio::ssl::context::context(method m)
```

!!! summary "引数"
	- method `m` 

!!! note "戻り値"
	ASIO_DECL



### ~context()
Destructor.


```c
ASIO_DECL asio::ssl::context::~context()
```

!!! note "戻り値"
	ASIO_DECL



### native_handle()
Get the underlying implementation in the native type.

This function may be used to obtain the underlying implementation of the context. This is intended to allow access to context functionality that is not otherwise provided. 
```c
ASIO_DECL native_handle_type asio::ssl::context::native_handle()
```

!!! note "戻り値"
	ASIO_DECL



### clear_options()
Clear options on the context.

This function may be used to configure the SSL options used by the context.
```c
ASIO_DECL void asio::ssl::context::clear_options(options o)
```

!!! summary "引数"
	- options `o` A bitmask of options. The available option values are defined in the  class. The specified options, if currently enabled on the context, are cleared.

!!! note "戻り値"
	ASIO_DECLvoid



### clear_options()
Clear options on the context.

This function may be used to configure the SSL options used by the context.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::clear_options(options o, asio::error_code &ec)
```

!!! summary "引数"
	- options `o` A bitmask of options. The available option values are defined in the  class. The specified options, if currently enabled on the context, are cleared.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### set_options()
Set options on the context.

This function may be used to configure the SSL options used by the context.
```c
ASIO_DECL void asio::ssl::context::set_options(options o)
```

!!! summary "引数"
	- options `o` A bitmask of options. The available option values are defined in the  class. The options are bitwise-ored with any existing value for the options.

!!! note "戻り値"
	ASIO_DECLvoid



### set_options()
Set options on the context.

This function may be used to configure the SSL options used by the context.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::set_options(options o, asio::error_code &ec)
```

!!! summary "引数"
	- options `o` A bitmask of options. The available option values are defined in the  class. The options are bitwise-ored with any existing value for the options.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### set_verify_mode()
Set the peer verification mode.

This function may be used to configure the peer verification mode used by the context.
```c
ASIO_DECL void asio::ssl::context::set_verify_mode(verify_mode v)
```

!!! summary "引数"
	- verify_mode `v` A bitmask of peer verification modes. See  for available values.

!!! note "戻り値"
	ASIO_DECLvoid



### set_verify_mode()
Set the peer verification mode.

This function may be used to configure the peer verification mode used by the context.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::set_verify_mode(verify_mode v, asio::error_code &ec)
```

!!! summary "引数"
	- verify_mode `v` A bitmask of peer verification modes. See  for available values.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### set_verify_depth()
Set the peer verification depth.

This function may be used to configure the maximum verification depth allowed by the context.
```c
ASIO_DECL void asio::ssl::context::set_verify_depth(int depth)
```

!!! summary "引数"
	- int `depth` Maximum depth for the certificate chain verification that shall be allowed.

!!! note "戻り値"
	ASIO_DECLvoid



### set_verify_depth()
Set the peer verification depth.

This function may be used to configure the maximum verification depth allowed by the context.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::set_verify_depth(int depth, asio::error_code &ec)
```

!!! summary "引数"
	- int `depth` Maximum depth for the certificate chain verification that shall be allowed.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### set_verify_callback()
Set the callback used to verify peer certificates.

This function is used to specify a callback function that will be called by the implementation when it needs to verify a peer certificate.
```c
void asio::ssl::context::set_verify_callback(VerifyCallback callback)
```

!!! summary "引数"
	- VerifyCallback `callback` The function object to be used for verifying a certificate. The function signature of the handler must be:  The return value of the callback is true if the certificate has passed verification, false otherwise.



### set_verify_callback()
Set the callback used to verify peer certificates.

This function is used to specify a callback function that will be called by the implementation when it needs to verify a peer certificate.
```c
ASIO_SYNC_OP_VOID asio::ssl::context::set_verify_callback(VerifyCallback callback, asio::error_code &ec)
```

!!! summary "引数"
	- VerifyCallback `callback` The function object to be used for verifying a certificate. The function signature of the handler must be:  The return value of the callback is true if the certificate has passed verification, false otherwise.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### load_verify_file()
Load a certification authority file for performing verification.

This function is used to load one or more trusted certification authorities from a file.
```c
ASIO_DECL void asio::ssl::context::load_verify_file(const std::string &filename)
```

!!! summary "引数"
	- const& `filename` The name of a file containing certification authority certificates in PEM format.

!!! note "戻り値"
	ASIO_DECLvoid



### load_verify_file()
Load a certification authority file for performing verification.

This function is used to load the certificates for one or more trusted certification authorities from a file.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::load_verify_file(const std::string &filename, asio::error_code &ec)
```

!!! summary "引数"
	- const& `filename` The name of a file containing certification authority certificates in PEM format.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### add_certificate_authority()
Add certification authority for performing verification.

This function is used to add one trusted certification authority from a memory buffer.
```c
ASIO_DECL void asio::ssl::context::add_certificate_authority(const const_buffer &ca)
```

!!! summary "引数"
	- const& `ca` The buffer containing the certification authority certificate. The certificate must use the PEM format.

!!! note "戻り値"
	ASIO_DECLvoid



### add_certificate_authority()
Add certification authority for performing verification.

This function is used to add one trusted certification authority from a memory buffer.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::add_certificate_authority(const const_buffer &ca, asio::error_code &ec)
```

!!! summary "引数"
	- const& `ca` The buffer containing the certification authority certificate. The certificate must use the PEM format.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### set_default_verify_paths()


Configures the context to use the default directories for finding certification authority certificates. This function specifies that the context should use the default, system-dependent directories for locating certification authority certificates.
```c
ASIO_DECL void asio::ssl::context::set_default_verify_paths()
```

!!! note "戻り値"
	ASIO_DECLvoid



### set_default_verify_paths()


Configures the context to use the default directories for finding certification authority certificates. This function specifies that the context should use the default, system-dependent directories for locating certification authority certificates.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::set_default_verify_paths(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### add_verify_path()


Add a directory containing certificate authority files to be used for performing verification. This function is used to specify the name of a directory containing certification authority certificates. Each file in the directory must contain a single certificate. The files must be named using the subject name's hash and an extension of ".0".
```c
ASIO_DECL void asio::ssl::context::add_verify_path(const std::string &path)
```

!!! summary "引数"
	- const& `path` The name of a directory containing the certificates.

!!! note "戻り値"
	ASIO_DECLvoid



### add_verify_path()


Add a directory containing certificate authority files to be used for performing verification. This function is used to specify the name of a directory containing certification authority certificates. Each file in the directory must contain a single certificate. The files must be named using the subject name's hash and an extension of ".0".
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::add_verify_path(const std::string &path, asio::error_code &ec)
```

!!! summary "引数"
	- const& `path` The name of a directory containing the certificates.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_certificate()
Use a certificate from a memory buffer.

This function is used to load a certificate into the context from a buffer.
```c
ASIO_DECL void asio::ssl::context::use_certificate(const const_buffer &certificate, file_format format)
```

!!! summary "引数"
	- const& `certificate` The buffer containing the certificate.
	- file_format `format` The certificate format (ASN.1 or PEM).

!!! note "戻り値"
	ASIO_DECLvoid



### use_certificate()
Use a certificate from a memory buffer.

This function is used to load a certificate into the context from a buffer.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_certificate(const const_buffer &certificate, file_format format, asio::error_code &ec)
```

!!! summary "引数"
	- const& `certificate` The buffer containing the certificate.
	- file_format `format` The certificate format (ASN.1 or PEM).
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_certificate_file()
Use a certificate from a file.

This function is used to load a certificate into the context from a file.
```c
ASIO_DECL void asio::ssl::context::use_certificate_file(const std::string &filename, file_format format)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the certificate.
	- file_format `format` The file format (ASN.1 or PEM).

!!! note "戻り値"
	ASIO_DECLvoid



### use_certificate_file()
Use a certificate from a file.

This function is used to load a certificate into the context from a file.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_certificate_file(const std::string &filename, file_format format, asio::error_code &ec)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the certificate.
	- file_format `format` The file format (ASN.1 or PEM).
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_certificate_chain()
Use a certificate chain from a memory buffer.

This function is used to load a certificate chain into the context from a buffer.
```c
ASIO_DECL void asio::ssl::context::use_certificate_chain(const const_buffer &chain)
```

!!! summary "引数"
	- const& `chain` The buffer containing the certificate chain. The certificate chain must use the PEM format.

!!! note "戻り値"
	ASIO_DECLvoid



### use_certificate_chain()
Use a certificate chain from a memory buffer.

This function is used to load a certificate chain into the context from a buffer.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_certificate_chain(const const_buffer &chain, asio::error_code &ec)
```

!!! summary "引数"
	- const& `chain` The buffer containing the certificate chain. The certificate chain must use the PEM format.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_certificate_chain_file()
Use a certificate chain from a file.

This function is used to load a certificate chain into the context from a file.
```c
ASIO_DECL void asio::ssl::context::use_certificate_chain_file(const std::string &filename)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the certificate. The file must use the PEM format.

!!! note "戻り値"
	ASIO_DECLvoid



### use_certificate_chain_file()
Use a certificate chain from a file.

This function is used to load a certificate chain into the context from a file.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_certificate_chain_file(const std::string &filename, asio::error_code &ec)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the certificate. The file must use the PEM format.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_private_key()
Use a private key from a memory buffer.

This function is used to load a private key into the context from a buffer.
```c
ASIO_DECL void asio::ssl::context::use_private_key(const const_buffer &private_key, file_format format)
```

!!! summary "引数"
	- const& `private_key` The buffer containing the private key.
	- file_format `format` The private key format (ASN.1 or PEM).

!!! note "戻り値"
	ASIO_DECLvoid



### use_private_key()
Use a private key from a memory buffer.

This function is used to load a private key into the context from a buffer.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_private_key(const const_buffer &private_key, file_format format, asio::error_code &ec)
```

!!! summary "引数"
	- const& `private_key` The buffer containing the private key.
	- file_format `format` The private key format (ASN.1 or PEM).
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_private_key_file()
Use a private key from a file.

This function is used to load a private key into the context from a file.
```c
ASIO_DECL void asio::ssl::context::use_private_key_file(const std::string &filename, file_format format)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the private key.
	- file_format `format` The file format (ASN.1 or PEM).

!!! note "戻り値"
	ASIO_DECLvoid



### use_private_key_file()
Use a private key from a file.

This function is used to load a private key into the context from a file.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_private_key_file(const std::string &filename, file_format format, asio::error_code &ec)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the private key.
	- file_format `format` The file format (ASN.1 or PEM).
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_rsa_private_key()
Use an RSA private key from a memory buffer.

This function is used to load an RSA private key into the context from a buffer.
```c
ASIO_DECL void asio::ssl::context::use_rsa_private_key(const const_buffer &private_key, file_format format)
```

!!! summary "引数"
	- const& `private_key` The buffer containing the RSA private key.
	- file_format `format` The private key format (ASN.1 or PEM).

!!! note "戻り値"
	ASIO_DECLvoid



### use_rsa_private_key()
Use an RSA private key from a memory buffer.

This function is used to load an RSA private key into the context from a buffer.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_rsa_private_key(const const_buffer &private_key, file_format format, asio::error_code &ec)
```

!!! summary "引数"
	- const& `private_key` The buffer containing the RSA private key.
	- file_format `format` The private key format (ASN.1 or PEM).
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_rsa_private_key_file()
Use an RSA private key from a file.

This function is used to load an RSA private key into the context from a file.
```c
ASIO_DECL void asio::ssl::context::use_rsa_private_key_file(const std::string &filename, file_format format)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the RSA private key.
	- file_format `format` The file format (ASN.1 or PEM).

!!! note "戻り値"
	ASIO_DECLvoid



### use_rsa_private_key_file()
Use an RSA private key from a file.

This function is used to load an RSA private key into the context from a file.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_rsa_private_key_file(const std::string &filename, file_format format, asio::error_code &ec)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the RSA private key.
	- file_format `format` The file format (ASN.1 or PEM).
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_tmp_dh()


Use the specified memory buffer to obtain the temporary Diffie-Hellman parameters. This function is used to load Diffie-Hellman parameters into the context from a buffer.
```c
ASIO_DECL void asio::ssl::context::use_tmp_dh(const const_buffer &dh)
```

!!! summary "引数"
	- const& `dh` The memory buffer containing the Diffie-Hellman parameters. The buffer must use the PEM format.

!!! note "戻り値"
	ASIO_DECLvoid



### use_tmp_dh()


Use the specified memory buffer to obtain the temporary Diffie-Hellman parameters. This function is used to load Diffie-Hellman parameters into the context from a buffer.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_tmp_dh(const const_buffer &dh, asio::error_code &ec)
```

!!! summary "引数"
	- const& `dh` The memory buffer containing the Diffie-Hellman parameters. The buffer must use the PEM format.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### use_tmp_dh_file()
Use the specified file to obtain the temporary Diffie-Hellman parameters.

This function is used to load Diffie-Hellman parameters into the context from a file.
```c
ASIO_DECL void asio::ssl::context::use_tmp_dh_file(const std::string &filename)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the Diffie-Hellman parameters. The file must use the PEM format.

!!! note "戻り値"
	ASIO_DECLvoid



### use_tmp_dh_file()
Use the specified file to obtain the temporary Diffie-Hellman parameters.

This function is used to load Diffie-Hellman parameters into the context from a file.
```c
ASIO_DECL ASIO_SYNC_OP_VOID asio::ssl::context::use_tmp_dh_file(const std::string &filename, asio::error_code &ec)
```

!!! summary "引数"
	- const& `filename` The name of the file containing the Diffie-Hellman parameters. The file must use the PEM format.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### set_password_callback()
Set the password callback.

This function is used to specify a callback function to obtain password information about an encrypted key in PEM format.
```c
void asio::ssl::context::set_password_callback(PasswordCallback callback)
```

!!! summary "引数"
	- PasswordCallback `callback` The function object to be used for obtaining the password. The function signature of the handler must be:  The return value of the callback is a string containing the password.



### set_password_callback()
Set the password callback.

This function is used to specify a callback function to obtain password information about an encrypted key in PEM format.
```c
ASIO_SYNC_OP_VOID asio::ssl::context::set_password_callback(PasswordCallback callback, asio::error_code &ec)
```

!!! summary "引数"
	- PasswordCallback `callback` The function object to be used for obtaining the password. The function signature of the handler must be:  The return value of the callback is a string containing the password.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



