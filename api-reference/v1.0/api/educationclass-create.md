---
title: "Create educationClass"
description: "Create a new educationClass object."
author: "mlafleur"
localization_priority: Normal
ms.prod: "education"
doc_type: apiPageType
---

# Create a Class

Namespace: microsoft.graph

Create a new [educationClass](../resources/educationclass.md) object.

> [!INFO]
> This will also create a universal group. When you use this API to create a class, it will add special properties to the group, which will add features such as assignments and special handling within Microsoft Teams when teams are created using the group. Please note that this API only creates the universal group and does not create a team. Microsoft Teams provides a user interface for teachers to create teams for their own classes using the groups created by this API.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | Not supported.                              |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | EduRoster.ReadWrite.All                     |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
POST /education/classes
```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request body

In the request body, supply a JSON representation of the [educationClass](../resources/educationclass.md) object.

## Response

If successful, this method returns a `201 Created` response code and an [educationClass](../resources/educationclass.md) object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_"
}
-->

```http
POST https://graph.microsoft.com/v1.0/education/classes
Content-Type: application/json
Content-length: 551

{
  "@odata.type": "#microsoft.education.rostering.api.educationClass",
  "displayName": "String",
  "mailNickname": "String",
  "description": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "classCode": "String",
  "externalName": "String",
  "externalId": "String",
  "externalSource": "String",
  "externalSourceDetail": "String",
  "grade": "String",
  "term": {
    "@odata.type": "microsoft.graph.educationTerm"
  },
  "course": {
    "@odata.type": "microsoft.graph.educationCourse"
  }
}
```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.education.rostering.api.educationClass"
}
-->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.education.rostering.api.educationClass",
  "displayName": "String",
  "mailNickname": "String",
  "description": "String",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "classCode": "String",
  "externalName": "String",
  "externalId": "String",
  "externalSource": "String",
  "externalSourceDetail": "String",
  "grade": "String",
  "term": {
    "@odata.type": "microsoft.graph.educationTerm"
  },
  "course": {
    "@odata.type": "microsoft.graph.educationCourse"
  }
}
```
