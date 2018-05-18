---
title: UpdateSubresources (stack-allocating) function
description: Updates subresources with a stack-allocating implementation.
ms.assetid: '2F30FDF1-4450-473E-AEA8-C5FF54260BCE'
keywords: ["UpdateSubresources function"]
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
---

# UpdateSubresources (stack-allocating) function

Updates subresources with a stack-allocating implementation.

## Syntax


```C++
UINT64 inline UpdateSubresources(
  _In_�ID3D12GraphicsCommandList *pCmdList,
  _In_�ID3D12Resource �����������*pDestinationResource,
  _In_�ID3D12Resource �����������*pIntermediate,
  �����UINT64 �������������������IntermediateOffset,
  _In_�UINT ���������������������FirstSubresource,
  _In_�UINT ���������������������NumSubresources,
  _In_�D3D12_SUBRESOURCE_DATA ���*pSrcData
);
```



## Parameters

<dl> <dt>

*pCmdList* \[in\]
</dt> <dd>

Type: **[**ID3D12GraphicsCommandList**](id3d12graphicscommandlist.md)\***

The command list, as a pointer to an [**ID3D12GraphicsCommandList**](id3d12graphicscommandlist.md).

</dd> <dt>

*pDestinationResource* \[in\]
</dt> <dd>

Type: **[**ID3D12Resource**](id3d12resource.md)\***

The destination resource, as a pointer to an [**ID3D12Resource**](id3d12resource.md).

</dd> <dt>

*pIntermediate* \[in\]
</dt> <dd>

Type: **[**ID3D12Resource**](id3d12resource.md)\***

The intermediate resource, as a pointer to an [**ID3D12Resource**](id3d12resource.md).

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Type: **[**UINT64**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

The offset, in bytes, to the intermediate resource.

</dd> <dt>

*FirstSubresource* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

The index of the first subresource in the resource. Valid values range from 0 to *MaxSubresources*.

</dd> <dt>

*NumSubresources* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

The number of subresources in the resource. Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).

</dd> <dt>

*pSrcData* \[in\]
</dt> <dd>

Type: **[**D3D12\_SUBRESOURCE\_DATA**](d3d12-subresource-data.md)\***

Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](d3d12-subresource-data.md) structures containing descriptions of the subresource data used for the update.

</dd> </dl>

## Return value

Type: **[**UINT64**](https://msdn.microsoft.com/library/windows/desktop/aa383751)**

The size, in bytes, of the buffer.

## Remarks

The declaration of this function begins with: `template <UINT MaxSubresources>`

## Requirements



|                    |                                                                                      |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Library<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## See also

<dl> <dt>

[Helper Functions for D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Subresources](subresources.md)
</dt> </dl>

�

�




