---
title: "educationSchool: delta"
description: "Get newly created or updated schools without having to perform a full read of the entire school collection."
author: "mlafleur"
localization_priority: Normal
ms.prod: "education"
doc_type: apiPageType
---

# Schools Delta Query

Namespace: microsoft.graph

Get newly created or updated schools without having to perform a full read of the entire school collection. See [Use delta query](/graph/delta-query-overview) for details.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | EduRoster.ReadBasic                         |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | EduRoster.Read.All, EduRoster.ReadWrite.All |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /education/schools/delta
```

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [educationSchool](../resources/educationschool.md) collection in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "educationschool_delta"
}
-->

```http
GET https://graph.microsoft.com/v1.0/education/schools/delta
```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.educationSchool)"
}
-->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.educationSchool",
      "id": "String (identifier)",
      "displayName": "String",
      "description": "String",
      "externalSource": "String",
      "externalSourceDetail": "String",
      "principalEmail": "String",
      "principalName": "String",
      "externalPrincipalId": "String",
      "lowestGrade": "String",
      "highestGrade": "String",
      "schoolNumber": "String",
      "externalId": "String",
      "phone": "String",
      "fax": "String",
      "createdBy": {
        "@odata.type": "microsoft.graph.identitySet"
      },
      "address": {
        "@odata.type": "microsoft.graph.physicalAddress"
      }
    }
  ]
}
```
