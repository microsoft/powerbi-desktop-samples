# ArtifactConfig

- [1. ![Required](https://img.shields.io/badge/Required-blue) Property `ArtifactConfig > version`](#version)
- [2. ![Required](https://img.shields.io/badge/Required-blue) Property `ArtifactConfig > logicalId`](#logicalId)

**Title:** ArtifactConfig

|                           |                                                                                                                                   |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                          |
| **Additional properties** | [![Any type: allowed](https://img.shields.io/badge/Any%20type-allowed-green)](# "Additional Properties of any type are allowed.") |

**Description:** The ArtifactConfig stored as item.config.json holds the LogicalId of the artifact and identifies this directory as an artifact. This file can be present in both the Report and Dataset folders with different LogicalIds. This file is optional.

| Property                   | Pattern | Type           | Deprecated | Definition | Title/Description |
| -------------------------- | ------- | -------------- | ---------- | ---------- | ----------------- |
| + [version](#version )     | No      | string or null | No         | -          | Version           |
| + [logicalId](#logicalId ) | No      | string         | No         | -          | LogicalId         |

## <a name="version"></a>1. ![Required](https://img.shields.io/badge/Required-blue) Property `ArtifactConfig > version`

**Title:** Version

|          |                  |
| -------- | ---------------- |
| **Type** | `string or null` |

**Description:** The verion of this artifact. The current latest version is 1.0

## <a name="logicalId"></a>2. ![Required](https://img.shields.io/badge/Required-blue) Property `ArtifactConfig > logicalId`

**Title:** LogicalId

|          |          |
| -------- | -------- |
| **Type** | `string` |

**Description:** The logicalId of the artifact is a workspace-unique immutable identifier representing a logical artifact and its source control representation. There is a different logicalId in the Report and Dataset folder.

----------------------------------------------------------------------------------------------------------------------------
