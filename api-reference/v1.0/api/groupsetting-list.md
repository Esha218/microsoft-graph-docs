---
title: "List group settings"
description: "Retrieve a list of group setting objects."
author: "Jordanndahl"
ms.localizationpriority: medium
ms.prod: "groups"
doc_type: apiPageType
---

# List group settings

Namespace: microsoft.graph

Retrieve a list of group setting objects.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).


|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Directory.Read.All, Directory.ReadWrite.All |

## HTTP request
<!-- { "blockType": "ignored" } -->

List tenant-wide or group settings.

```http
GET /groupSettings
GET groups/{id}/settings
```
## Optional query parameters
This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.

>**Note:** $filter is not supported.

## Request headers
| Name | Description |
|:----------|:----------|
| Authorization  | Bearer {token}. Required. |

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and collection of [groupSetting](../resources/groupsetting.md) objects in the response body.
## Example

### Request


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_groupsettings"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/v1.0/groupSettings
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-groupsettings-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-groupsettings-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-groupsettings-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-groupsettings-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

Note: The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSetting",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groupSettings",
  "value": [
    {
      "id": "f0b2d6f5-097d-4177-91af-a24e530b53cc",
      "displayName": "Group.Unified",
      "templateId": "62375ab9-6b52-47ed-826b-58e47e0e304b",
      "values": [
        {
          "name": "EnableMIPLabels",
          "value": "true"
        },
        {
          "name": "CustomBlockedWordsList",
          "value": ""
        },
        {
          "name": "EnableMSStandardBlockedWords",
          "value": "true"
        },
        {
          "name": "ClassificationDescriptions",
          "value": ""
        },
        {
          "name": "DefaultClassification",
          "value": ""
        },
        {
          "name": "PrefixSuffixNamingRequirement",
          "value": "[Contoso-][GroupName]"
        },
        {
          "name": "AllowGuestsToBeGroupOwner",
          "value": "false"
        },
        {
          "name": "AllowGuestsToAccessGroups",
          "value": "true"
        },
        {
          "name": "GuestUsageGuidelinesUrl",
          "value": "https://privacy.contoso.com/privacystatement"
        },
        {
          "name": "GroupCreationAllowedGroupId",
          "value": ""
        },
        {
          "name": "AllowToAddGuests",
          "value": "true"
        },
        {
          "name": "UsageGuidelinesUrl",
          "value": ""
        },
        {
          "name": "ClassificationList",
          "value": ""
        },
        {
          "name": "EnableGroupCreation",
          "value": "true"
        }
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groupSettings",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

