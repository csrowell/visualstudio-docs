---
title: "How to: Set a Thread Name in Managed Code | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "Thread.Name property"
  - "threading [Visual Studio], names"
  - "thread names"
  - "debugging [Visual Studio], threads"
ms.assetid: c0c4d74a-0314-4b71-81c9-b0b019347ab8
caps.latest.revision: 31
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# How to: Set a Thread Name in Managed Code
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [How to: Set a Thread Name in Managed Code](https://docs.microsoft.com/visualstudio/debugger/how-to-set-a-thread-name-in-managed-code).  
  
Thread naming is possible in any edition of Visual Studio. Thread naming is useful for keeping track of threads in the **Threads** window. Because the **Threads** window is not available in the Visual Studio Express editions, thread naming has little utility in Express editions.  
  
 To set a thread name in managed code, use the <xref:System.Threading.Thread.Name%2A> property.  
  
## Example  
  
```  
Public Class Needle  
    ' This method will be called when the thread is started.  
    Sub Baz()  
        Console.WriteLine("Needle Baz is running on another thread")  
    End Sub  
End Class  
  
Sub Main()  
    Console.WriteLine("Thread Simple Sample")  
    Dim oNeedle As New Needle()  
   ' Create a Thread object.   
    Dim oThread As New System.Threading.Thread(AddressOf oNeedle.Baz)  
    ' Set the Thread name to "MainThread".  
    oThread.Name = "MainThread"  
    ' Starting the thread invokes the ThreadStart delegate  
    oThread.Start()  
End Sub  
```  
  
## See Also  
 [Debug Multithreaded Applications](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [How to: Set a Thread Name in Native Code](../debugger/how-to-set-a-thread-name-in-native-code.md)



