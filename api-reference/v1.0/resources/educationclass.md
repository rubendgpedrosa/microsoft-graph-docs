---
title: "educationClass resource type"
description: "Represents a class within a school. The **educationClass** resource corresponds to the Microsoft 365 group and shares the same ID. Students are regular members of the class, and teachers are owners and have appropriate rights. For Office experiences to work correctly, teachers must be members of both the teachers and members collections.  "
localization_priority: Normal
author: "mlafleur"
ms.prod: "education"
doc_type: resourcePageType
---

# Class resource type

Namespace: microsoft.graph

Represents a class within a school. The **educationClass** resource corresponds to the Microsoft 365 group and shares the same ID. Students are regular members of the class, and teachers are owners and have appropriate rights. For Office experiences to work correctly, teachers must be members of both the teachers and members collections.

## Methods

| Method                                                   | Return type                                                 | Description                                                                                          |
| :------------------------------------------------------- | :---------------------------------------------------------- | :--------------------------------------------------------------------------------------------------- |
| [List educationClasses](../api/educationclass-list.md)   | [educationClass](../resources/educationclass.md) collection | Get a list of the [educationClass](../resources/educationclass.md) objects and their properties.     |
| [Create educationClass](../api/educationclass-create.md) | [educationClass](../resources/educationclass.md)            | Create a new [educationClass](../resources/educationclass.md) object.                                |
| [Get educationClass](../api/educationclass-get.md)       | [educationClass](../resources/educationclass.md)            | Read the properties and relationships of an [educationClass](../resources/educationclass.md) object. |
| [Update educationClass](../api/educationclass-update.md) | [educationClass](../resources/educationclass.md)            | Update the properties of an [educationClass](../resources/educationclass.md) object.                 |
| [Delete educationClass](../api/educationclass-delete.md) | None                                                        | Deletes an [educationClass](../resources/educationclass.md) object.                                  |
| [delta](../api/educationclass-delta.md)                  | [educationClass](../resources/educationclass.md) collection | **TODO: Add Description**                                                                            |
| [List members](../api/educationclass-list-members.md)    | [educationUser](../resources/educationuser.md) collection   | Get the educationUser resources from the members navigation property.                                |
| [Add member](../api/educationclass-post-members.md)      | [educationUser](../resources/educationuser.md)              | Add members by posting to the members collection.                                                    |
| [List teachers](../api/educationclass-list-teachers.md)  | [educationUser](../resources/educationuser.md) collection   | Get the educationUser resources from the teachers navigation property.                               |
| [Add teacher](../api/educationclass-post-teachers.md)    | [educationUser](../resources/educationuser.md)              | Add teachers by posting to the teachers collection.                                                  |

## Properties

| Property             | Type                                               | Description                                                                                    |
| :------------------- | :------------------------------------------------- | :--------------------------------------------------------------------------------------------- |
| classCode            | String                                             | Class code used by the school to identify the class.                                           |
| course               | [educationCourse](../resources/educationcourse.md) | Course information for the class                                                               |
| createdBy            | [identitySet](../resources/identityset.md)         | Entity who created the class                                                                   |
| description          | String                                             | Description of the class.                                                                      |
| displayName          | String                                             | Name of the class.                                                                             |
| externalId           | String                                             | ID of the class from the syncing system.                                                       |
| externalName         | String                                             | Name of the class in the syncing system.                                                       |
| externalSource       | educationExternalSource                            | How this class was created. Possible values are: `sis`, `manual`, `unknownFutureValue`, `lms`. |
| externalSourceDetail | String                                             | The name of the external source this resources was generated from.                             |
| grade                | String                                             | Grade level of the class.                                                                      |
| mailNickname         | String                                             | Mail name for sending email to all members, if this is enabled.                                |
| term                 | [educationTerm](../resources/educationterm.md)     | Term for this class.                                                                           |

## Relationships

| Relationship | Type                                                          | Description                                               |
| :----------- | :------------------------------------------------------------ | :-------------------------------------------------------- |
| members      | [educationUser](../resources/educationuser.md) collection     | All users in the class. Nullable.                         |
| schools      | [educationSchool](../resources/educationschool.md) collection | All schools that this class is associated with. Nullable. |
| teachers     | [educationUser](../resources/educationuser.md) collection     | All teachers in the class. Nullable.                      |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.educationClass",
  "openType": false
}
-->

```json
{
  "@odata.type": "#microsoft.graph.educationClass",
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
