---
title: "IDebugPort2::GetProcess | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDebugPort2::GetPortSupplier"
helpviewer_keywords: 
  - "IDebugPort2::GetPortSupplier"
ms.assetid: 3e2431b0-0e19-450d-8e1d-d7c314c8f872
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
---
# IDebugPort2::GetProcess
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDebugPort2::GetProcess](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugport2-getprocess).  
  
Gets the specified process running on a port.  
  
## Syntax  
  
```cpp#  
HRESULT GetProcess(   
   AD_PROCESS_ID    ProcessId,  
   IDebugProcess2** ppProcess  
);  
```  
  
```csharp  
int GetProcess(   
   AD_PROCESS_ID      ProcessId,  
   out IDebugProcess2 ppProcess  
);  
```  
  
#### Parameters  
 `ProcessId`  
 [in] An [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) structure that specifies the process identifier.  
  
 `ppProcess`  
 [out] Returns an [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) object representing the process.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md)

