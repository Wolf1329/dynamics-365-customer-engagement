---
title: sessionId property (app profile manager) JavaScript API Reference 
description: Learn about the sessionId property of app profile manager in Copilot Service workspace.
author: gandhamm
ms.author: mgandham
ms.reviewer: mgandham
ms.date: 03/18/2025
ms.topic: reference
---

# sessionId (app profile manager)

The ID of a session.

## Syntax

`Microsoft.Apm.getSession(sessionId).focus();`

## Example

```JavaScript
const session = Microsoft.Apm.getFocusedSession();
console.log(session.sessionId);
```

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
