---
title: "educationOrganization resource type"
description: "Abstract entity used to model the commonality between different organization types within the education sector."
author: "mlafleur"
localization_priority: Normal
ms.prod: "education"
doc_type: resourcePageType
---

# Education Organization resource type

Namespace: microsoft.graph

Abstract entity used to model the commonality between different organization types within the education sector.

## Properties

| Property             | Type                    | Description                                                                                                         |
| :------------------- | :---------------------- | :------------------------------------------------------------------------------------------------------------------ |
| description          | String                  | Organization description.                                                                                           |
| displayName          | String                  | Organization display name.                                                                                          |
| externalSource       | educationExternalSource | Source where this organization was created from. Possible values are: `sis`, `manual`, `unknownFutureValue`, `lms`. |
| externalSourceDetail | String                  | The name of the external source this resources was generated from.                                                  |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.educationOrganization",
  "openType": false
}
-->

```json
{
  "@odata.type": "#microsoft.graph.educationOrganization",
  "displayName": "String",
  "description": "String",
  "externalSource": "String",
  "externalSourceDetail": "String"
}
```
