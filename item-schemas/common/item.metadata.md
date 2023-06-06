# ArtifactMetadata

- [1. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `ArtifactMetadata > type`](#type)
- [2. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `ArtifactMetadata > displayName`](#displayName)
- [3. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `ArtifactMetadata > description`](#description)

**Title:** ArtifactMetadata

|                           |                                                                                                                                   |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                          |
| **Additional properties** | [![Any type: allowed](https://img.shields.io/badge/Any%20type-allowed-green)](# "Additional Properties of any type are allowed.") |

**Description:** The ArtifactMetadata stored as item.metadata.json holds the Type and DisplayName of the artifact. The DisplayName is what is shown in the title bar of Power BI Desktop. There will be an ArtifactMetadata file in both the Report and Dataset folders. This file is optional.

| Property                       | Pattern | Type           | Deprecated | Definition | Title/Description |
| ------------------------------ | ------- | -------------- | ---------- | ---------- | ----------------- |
| - [type](#type )               | No      | string or null | No         | -          | Type              |
| - [displayName](#displayName ) | No      | string or null | No         | -          | DisplayName       |
| - [description](#description ) | No      | string or null | No         | -          | Description       |

## <a name="type"></a>1. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `ArtifactMetadata > type`

**Title:** Type

|          |                  |
| -------- | ---------------- |
| **Type** | `string or null` |

**Description:** The type of the artifact either "report" or "dataset".

## <a name="displayName"></a>2. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `ArtifactMetadata > displayName`

**Title:** DisplayName

|          |                  |
| -------- | ---------------- |
| **Type** | `string or null` |

**Description:** The displayname of the artifact.

## <a name="description"></a>3. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `ArtifactMetadata > description`

**Title:** Description

|          |                  |
| -------- | ---------------- |
| **Type** | `string or null` |

**Description:** The description of the artifact.

----------------------------------------------------------------------------------------------------------------------------
