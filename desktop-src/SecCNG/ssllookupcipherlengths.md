---
Description: 'Returns an NCRYPT\_SSL\_CIPHER\_LENGTHS structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.'
ms.assetid: '44d0d803-16d7-4bdf-9638-afbdaf9e1802'
title: SslLookupCipherLengths function
---

# SslLookupCipherLengths function

The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](seccngprov-ncrypt_ssl_cipher_lengths) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.

## Syntax


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_��NCRYPT_PROV_HANDLE �������hSslProvider,
  _In_��DWORD ��������������������dwProtocol,
  _In_��DWORD ��������������������dwCipherSuite,
  _In_��DWORD ��������������������dwKeyType,
  _Out_�NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_��DWORD ��������������������cbCipherLengths,
  _In_��DWORD ��������������������dwFlags
);
```



## Parameters

<dl> <dt>

*hSslProvider* \[in\]
</dt> <dd>

The handle of the [*Secure Sockets Layer protocol*](https://msdn.microsoft.com/library/windows/desktop/ms721625#-security-secure-sockets-layer-protocol-gly) (SSL) protocol provider instance.

</dd> <dt>

*dwProtocol* \[in\]
</dt> <dd>

One of the [**CNG SSL Provider Protocol Identifier**](seccngprov-cng_ssl_provider_protocol_identifiers) values.

</dd> <dt>

*dwCipherSuite* \[in\]
</dt> <dd>

One of the [**CNG SSL Provider Cipher Suite Identifier**](seccngprov-cng_ssl_provider_cipher_suite_identifiers) values.

</dd> <dt>

*dwKeyType* \[in\]
</dt> <dd>

One of the [**CNG SSL Provider Key Type Identifier**](seccngprov-cng_ssl_provider_key_type_identifiers) values. For key types that are not [*elliptic curve cryptography*](https://msdn.microsoft.com/library/windows/desktop/ms721575#-security-elliptic-curve-cryptography-gly) (ECC), set this parameter to zero.

</dd> <dt>

*pCipherLengths* \[out\]
</dt> <dd>

A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](seccngprov-ncrypt_ssl_cipher_lengths) structure.

</dd> <dt>

*cbCipherLengths* \[in\]
</dt> <dd>

The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.

</dd> <dt>

*dwFlags* \[in\]
</dt> <dd>

This parameter is reserved for future use and must be set to zero.

</dd> </dl>

## Return value

If the function succeeds, it returns zero.

If the function fails, it returns a nonzero error value.

Possible return codes include, but are not limited to, the following.



| Return code/value                                                                                                                                                       | Description                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | The *hSslProvider* parameter contains a pointer that is not valid.<br/>                                                      |
| <dl> <dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.<br/> |
| <dl> <dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | The *dwFlags* parameter must be set to zero.<br/>                                                                            |



�

## Remarks

The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](https://msdn.microsoft.com/library/windows/desktop/ms721627#-security-transport-layer-security-protocol-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.

## Requirements



|                                     |                                                                                          |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�7 \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows Server�2008�R2 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



�

�



