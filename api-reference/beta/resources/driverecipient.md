---
author: JeremyKelley
description: "The DriveRecipient resource represents a person, group, or other recipient to share with using the invite action."
ms.date: 09/10/2017
title: DriveRecipient
ms.localizationpriority: medium
ms.prod: "sharepoint"
doc_type: resourcePageType
---
# DriveRecipient resource

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **DriveRecipient** resource represents a person, group, or other recipient to share with using the [invite](../api/driveitem-invite.md) action.

## JSON representation

<!-- { 
  "blockType": "resource", 
  "@odata.type": "microsoft.graph.driveRecipient", 
  "optionalProperties": ["alias", "objectId", "email"] } -->
```json
{
  "email": "string",
  "alias": "string",
  "objectId": "string",
}
```

## Properties
The recipients resource has these properties.

| Property name | Type   | Description                                                                                             |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------|
| email         | String | The email address for the recipient, if the recipient has an associated email address.                  |
| alias         | String | The alias of the domain object, for cases where an email address is unavailable (e.g. security groups). |
| objectId      | String | The unique identifier for the recipient in the directory.                                               |

## Remarks

When using [invite](../api/driveitem-invite.md) to add permissions, the DriveRecipient can specify **email**, **alias**, or **objectId**.
Only one of these values is required.

<!--
{
  "type": "#page.annotation",
  "description": "Recipients resource defines a single recipient for the sharing invitation and permissions collection.",
  "keywords": "sharing,share,permissions,action.invite,invite,email",
  "section": "documentation",
  "tocPath": "Resources/Recipients",
  "suppressions": []
}
-->


