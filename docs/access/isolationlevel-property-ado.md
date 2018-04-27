---
title: "IsolationLevel Property (ADO)"
 
 
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
  
localization_priority: Normal
ms.assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc

---

# IsolationLevel Property (ADO)

Indicates the level of isolation for a [Connection](connection-object-ado.md) object. 
  
## Settings and Return Values

Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**. 
  
## Remarks

Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation. 
  
The **IsolationLevel** property is read/write. 
  
 **Remote Data Service Usage** When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**. 
  
Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error. 
  
