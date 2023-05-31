# ArtifactMetadata

- [1. Property `ArtifactMetadata > type`](#type)
- [2. Property `ArtifactMetadata > displayName`](#displayName)
- [3. Property `ArtifactMetadata > description`](#description)

**Title:** ArtifactMetadata

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** The ArtifactMetadata stored as item.metadata.json holds the Type and DisplayName of the artifact. The DisplayName is what is shown in the title bar of Power BI Desktop. There will be an ArtifactMetadata file in both the Report and Dataset folders. This file is optional.

| Property                       | Pattern | Type           | Deprecated | Definition | Title/Description |
| ------------------------------ | ------- | -------------- | ---------- | ---------- | ----------------- |
| - [type](#type )               | No      | string or null | No         | -          | Type              |
| - [displayName](#displayName ) | No      | string or null | No         | -          | DisplayName       |
| - [description](#description ) | No      | string or null | No         | -          | Description       |

## <a name="type"></a>1. Property `ArtifactMetadata > type`

**Title:** Type

|              |                  |
| ------------ | ---------------- |
| **Type**     | `string or null` |
| **Required** | No               |

**Description:** The type of the artifact either "report" or "dataset".

## <a name="displayName"></a>2. Property `ArtifactMetadata > displayName`

**Title:** DisplayName

|              |                  |
| ------------ | ---------------- |
| **Type**     | `string or null` |
| **Required** | No               |

**Description:** The displayname of the artifact.

## <a name="description"></a>3. Property `ArtifactMetadata > description`

**Title:** Description

|              |                  |
| ------------ | ---------------- |
| **Type**     | `string or null` |
| **Required** | No               |

**Description:** The description of the artifact.

----------------------------------------------------------------------------------------------------------------------------
