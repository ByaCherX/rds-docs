---
description: "Learn more about: COleStreamFile Class"
title: "COleStreamFile Class"
ms.date: "11/04/2016"
f1_keywords: ["COleStreamFile", "AFXOLE/COleStreamFile", "AFXOLE/COleStreamFile::COleStreamFile", "AFXOLE/COleStreamFile::Attach", "AFXOLE/COleStreamFile::CreateMemoryStream", "AFXOLE/COleStreamFile::CreateStream", "AFXOLE/COleStreamFile::Detach", "AFXOLE/COleStreamFile::GetStream", "AFXOLE/COleStreamFile::OpenStream"]
helpviewer_keywords: ["COleStreamFile [MFC], COleStreamFile", "COleStreamFile [MFC], Attach", "COleStreamFile [MFC], CreateMemoryStream", "COleStreamFile [MFC], CreateStream", "COleStreamFile [MFC], Detach", "COleStreamFile [MFC], GetStream", "COleStreamFile [MFC], OpenStream"]
ms.assetid: e4f93698-e17c-4a18-a7c0-4b4df8eb4d93
---
# COleStreamFile Class

Represents a stream of data (`IStream`) in a compound file as part of OLE Structured Storage.

## Syntax

```
class COleStreamFile : public CFile
```

## Members

### Public Constructors

|Name|Description|
|----------|-----------------|
|[COleStreamFile::COleStreamFile](#colestreamfile)|Constructs a `COleStreamFile` object.|

### Public Methods

|Name|Description|
|----------|-----------------|
|[COleStreamFile::Attach](#attach)|Associates a stream with the object.|
|[COleStreamFile::CreateMemoryStream](#creatememorystream)|Creates a stream from global memory and associates it with the object.|
|[COleStreamFile::CreateStream](#createstream)|Creates a stream and associates it with the object.|
|[COleStreamFile::Detach](#detach)|Disassociates the stream from the object.|
|[COleStreamFile::GetStream](#getstream)|Returns the current stream.|
|[COleStreamFile::OpenStream](#openstream)|Safely opens a stream and associates it with the object.|

## Remarks

An `IStorage` object must exist before the stream can be opened or created unless it is a memory stream.

`COleStreamFile` objects are manipulated exactly like [CFile](../../mfc/reference/cfile-class.md) objects.

For more information about manipulating streams and storages, see the article [Containers: Compound Files](../../mfc/containers-compound-files.md)..

For more information, see [IStream](/windows/win32/api/objidl/nn-objidl-istream) and [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) in the Windows SDK.

## Inheritance Hierarchy

[CObject](../../mfc/reference/cobject-class.md)

[CFile](../../mfc/reference/cfile-class.md)

`COleStreamFile`

## Requirements

**Header:** afxole.h

## <a name="attach"></a> COleStreamFile::Attach

Associates the supplied OLE stream with the `COleStreamFile` object.

```cpp
void Attach(LPSTREAM lpStream);
```

### Parameters

*lpStream*<br/>
Points to the OLE stream (`IStream`) to be associated with the object. Cannot be NULL.

### Remarks

The object must not already be associated with an OLE stream.

For more information, see [IStream](/windows/win32/api/objidl/nn-objidl-istream) in the Windows SDK.

## <a name="colestreamfile"></a> COleStreamFile::COleStreamFile

Creates a `COleStreamFile` object.

```
COleStreamFile(LPSTREAM lpStream = NULL);
```

### Parameters

*lpStream*<br/>
Pointer to the OLE stream to be associated with the object.

### Remarks

If *lpStream* is NULL, the object is not associated with an OLE stream, otherwise, the object is associated with the supplied OLE stream.

For more information, see [IStream](/windows/win32/api/objidl/nn-objidl-istream) in the Windows SDK.

## <a name="creatememorystream"></a> COleStreamFile::CreateMemoryStream

Safely creates a new stream out of global, shared memory where a failure is a normal, expected condition.

```
BOOL CreateMemoryStream(CFileException* pError = NULL);
```

### Parameters

*pError*<br/>
Points to a [CFileException](../../mfc/reference/cfileexception-class.md) object or NULL that indicates the completion status of the create operation. Supply this parameter if you want to monitor possible exceptions generated by attempting to create the stream.

### Return Value

Nonzero if the stream is created successfully; otherwise 0.

### Remarks

The memory is allocated by the OLE subsystem.

For more information, see [CreateStreamOnHGlobal](/windows/win32/api/combaseapi/nf-combaseapi-createstreamonhglobal) in the Windows SDK.

## <a name="createstream"></a> COleStreamFile::CreateStream

Safely creates a new stream in the supplied storage object where a failure is a normal, expected condition.

```
BOOL CreateStream(
    LPSTORAGE lpStorage,
    LPCTSTR lpszStreamName,
    DWORD nOpenFlags = modeReadWrite|shareExclusive|modeCreate,
    CFileException* pError = NULL);
```

### Parameters

*lpStorage*<br/>
Points to the OLE storage object that contains the stream to be created. Cannot be NULL.

*lpszStreamName*<br/>
Name of the stream to be created. Cannot be NULL.

*nOpenFlags*<br/>
Access mode to use when opening the stream. Exclusive, read/write, and create modes are used by default. For a complete list of the available modes, see [CFile::CFile](../../mfc/reference/cfile-class.md#cfile).

*pError*<br/>
Points to a [CFileException](../../mfc/reference/cfileexception-class.md) object or NULL. Supply this parameter if you want to monitor possible exceptions generated by attempting to create the stream.

### Return Value

Nonzero if the stream is created successfully; otherwise 0.

### Remarks

A file exception will be thrown if the open fails and *pError* is not NULL.

For more information, see [IStorage::CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) in the Windows SDK.

## <a name="detach"></a> COleStreamFile::Detach

Disassociates the stream from the object without closing the stream.

```
LPSTREAM Detach();
```

### Return Value

A pointer to the stream (`IStream`) that was associated with the object.

### Remarks

The stream must be closed in some other fashion before the program terminates.

For more information, see [IStream](/windows/win32/api/objidl/nn-objidl-istream) in the Windows SDK.

## <a name="getstream"></a> COleStreamFile::GetStream

Call this function to return a pointer to current stream.

```
IStream* GetStream() const;
```

### Return Value

A pointer to the current stream interface ( [IStream](/windows/win32/api/objidl/nn-objidl-istream)).

## <a name="openstream"></a> COleStreamFile::OpenStream

Opens an existing stream.

```
BOOL OpenStream(
    LPSTORAGE lpStorage,
    LPCTSTR lpszStreamName,
    DWORD nOpenFlags = modeReadWrite|shareExclusive,
    CFileException* pError = NULL);
```

### Parameters

*lpStorage*<br/>
Points to the OLE storage object that contains the stream to be opened. Cannot be NULL.

*lpszStreamName*<br/>
Name of the stream to be opened. Cannot be NULL.

*nOpenFlags*<br/>
Access mode to use when opening the stream. Exclusive and read/write modes are used by default. For the complete list of the available modes, see [CFile::CFile](../../mfc/reference/cfile-class.md#cfile).

*pError*<br/>
Points to a [CFileException](../../mfc/reference/cfileexception-class.md) object or NULL. Supply this parameter if you want to monitor possible exceptions generated by attempting to open the stream.

### Return Value

Nonzero if the stream is opened successfully; otherwise 0.

### Remarks

A file exception will be thrown if the open fails and *pError* is not NULL.

For more information, see [IStorage::OpenStream](/windows/win32/api/objidl/nf-objidl-istorage-openstream) in the Windows SDK.

## See also

[CFile Class](../../mfc/reference/cfile-class.md)<br/>
[Hierarchy Chart](../../mfc/hierarchy-chart.md)