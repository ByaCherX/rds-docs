---
description: "Learn more about: Provider Wizard-Generated Files"
title: "Provider Wizard-Generated Files"
ms.date: "05/09/2019"
helpviewer_keywords: ["OLE DB providers, wizard-generated files"]
ms.assetid: 6e1ac94b-eb90-4abf-82b3-06944b947ebc
---
# Provider Wizard-Generated Files

::: moniker range="msvc-160"

The ATL OLE DB Provider wizard is not available in Visual Studio 2019 and later.

::: moniker-end

::: moniker range="<=msvc-150"

The **ATL OLE DB Provider Wizard** generates the following files. The following topics use the short name *Custom*, but the exact file names depend on the choice you made when creating the provider.

|File name|Description|
|---------------|-----------------|
|*Custom*RS.cpp|Contains the command helper `Execute` method and the provider column map.|
|*Custom*DS.h|Implements the data source object. This header file contains the property map for data source properties.|
|*Custom*RS.h|Implements the command and rowset objects. This header file contains the property map for rowset and command properties.|
|*Custom*Sess.h|Implements the session object. This header file contains the property map for session properties.|
|*Custom*.rgs|Contains the registered objects generated by the **OLE DB Provider Wizard**.|

::: moniker-end

## See also

[Creating an OLE DB Provider](../../data/oledb/creating-an-ole-db-provider.md)<br/>