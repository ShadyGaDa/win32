---
title: IMimeMessageTree GetMessageSource method
description: Gets the message source for the message.
ms.assetid: '32416f96-13c9-4fca-9beb-d2b82fc07f6d'
keywords: ["GetMessageSource method Windows Mail (formerly Outlook Express)", "GetMessageSource method Windows Mail (formerly Outlook Express) , IMimeMessageTree interface", "IMimeMessageTree interface Windows Mail (formerly Outlook Express) , GetMessageSource method"]
topic_type:
- apiref
api_name:
- IMimeMessageTree.GetMessageSource
api_location:
- Inetcomm.dll
api_type:
- COM
---

# IMimeMessageTree::GetMessageSource method

Gets the message source for the message.

## Syntax


```C++
HRESULT GetMessageSource(
  [out]�IStream **ppStream,
  [in]��DWORD ��dwFlags
);
```



## Parameters

<dl> <dt>

*ppStream* \[out\]
</dt> <dd>

Type: **[IStream](http://msdn.microsoft.com/library/stg/stg/istream.asp)\*\***

Receives the address to a pointer to an [IStream](http://msdn.microsoft.com/library/stg/stg/istream.asp) object. The client is responsible for releasing this object.

> [!Note]  
> The client should not write to this stream.

�

</dd> <dt>

*dwFlags* \[in\]
</dt> <dd>

Type: **DWORD**

Specifies how an [**IMimeMessageTree**](oe-imimemessagetree.md) object should be committed.



| Value                                                                                                                                                                                                                                                                | Meaning                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMMIT_ONLYIFDIRTY"></span><span id="commit_onlyifdirty"></span><dl> <dt>**COMMIT\_ONLYIFDIRTY**</dt> <dt>0x00000001</dt> </dl>                         | Indicates that if the message object is dirty, the message should internally commit all changes so that the method being called reflects the committed state of the message. <br/>                                                                                                                                        |
| <span id="COMMIT_REUSESTORAGE"></span><span id="commit_reusestorage"></span><dl> <dt>**COMMIT\_REUSESTORAGE**</dt> <dt>0x00000002</dt> </dl>                      | Indicates that if the message object needs to commit itself, it should reuse its current storage object. For example, if a message object is loaded from a client provided [IStream](http://msdn.microsoft.com/library/stg/stg/istream.asp), the message object saves itself back into that original IStream. <br/> |
| <span id="COMMIT_SMIMETRANSFERENCODE"></span><span id="commit_smimetransferencode"></span><dl> <dt>**COMMIT\_SMIMETRANSFERENCODE**</dt> <dt>0x00000004</dt> </dl> | Indicates secure messaging.<br/>                                                                                                                                                                                                                                                                                          |



�

</dd> </dl>

## Return value

Type: **HRESULT**

Returns one of the following values.



| Return code                                                                                       | Description                                                                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl>              | Indicates success.<br/>                                                                |
| <dl> <dt>**E\_FAIL**</dt> </dl>            | Indicates that an unknown error has occurred.<br/>                                     |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl>      | Indicates that *ppStream* is **NULL**. <br/>                                           |
| <dl> <dt>**MIME\_E\_NO\_DATA**</dt> </dl>  | Indicates that the message has no data to save. <br/>                                  |
| <dl> <dt>**E\_OUTOFMEMORY**</dt> </dl>     | Indicates that an attempt to allocate memory failed.<br/>                              |
| <dl> <dt>**STG\_E\_MEDIUMFULL**</dt> </dl> | Indicates that not enough disk space or memory is available to save the message. <br/> |



�

## Remarks

This method creates an [IStream](http://msdn.microsoft.com/library/stg/stg/istream.asp) object that can be used to read the MIME or [RFC 822](http://www.ietf.org/rfc/rfc822.txt) message source. It is faster than calling [IMimeMessageTree::Save](http://msdn.microsoft.com/library/com/htm/cmi_n2p_47z9.asp) because if the message object is not dirty, MimeOLE returns a pointer to an internal IStream object and does not have to write the message.

## Requirements



|                                     |                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�XP \[desktop apps only\]<br/>                                                                    |
| Minimum supported server<br/> | Windows Server�2003 \[desktop apps only\]<br/>                                                           |
| Product<br/>                  | Outlook Express 6.0<br/>                                                                                 |
| Header<br/>                   | <dl> <dt>Mimeole.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Mimeole.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Inetcomm.dll (version 6.0 or later)</dt> </dl> |



�

�




