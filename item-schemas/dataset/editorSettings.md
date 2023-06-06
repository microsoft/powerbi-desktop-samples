# EditorSettings

- [1. ![Required](https://img.shields.io/badge/Required-blue) Property `EditorSettings > version`](#version)
- [2. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > showHiddenFields`](#showHiddenFields)
- [3. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > autodetectRelationships`](#autodetectRelationships)
- [4. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > parallelQueryLoading`](#parallelQueryLoading)
- [5. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > typeDetectionEnabled`](#typeDetectionEnabled)
- [6. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > relationshipImportEnabled`](#relationshipImportEnabled)
- [7. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > relationshipRefreshEnabled`](#relationshipRefreshEnabled)
- [8. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > runBackgroundAnalysis`](#runBackgroundAnalysis)

**Title:** EditorSettings

|                           |                                                                                                                                   |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                          |
| **Additional properties** | [![Any type: allowed](https://img.shields.io/badge/Any%20type-allowed-green)](# "Additional Properties of any type are allowed.") |

**Description:** The EditorSettings stored as editorSettings.json holds dataset editor settings that are saved as part of the dataset definition for use across users or environments. This file is optional.

| Property                                                     | Pattern | Type           | Deprecated | Definition | Title/Description          |
| ------------------------------------------------------------ | ------- | -------------- | ---------- | ---------- | -------------------------- |
| + [version](#version )                                       | No      | string or null | No         | -          | Version                    |
| - [showHiddenFields](#showHiddenFields )                     | No      | boolean        | No         | -          | ShowHiddenFields           |
| - [autodetectRelationships](#autodetectRelationships )       | No      | boolean        | No         | -          | AutodetectRelationships    |
| - [parallelQueryLoading](#parallelQueryLoading )             | No      | boolean        | No         | -          | ParallelQueryLoading       |
| - [typeDetectionEnabled](#typeDetectionEnabled )             | No      | boolean        | No         | -          | TypeDetectionEnabled       |
| - [relationshipImportEnabled](#relationshipImportEnabled )   | No      | boolean        | No         | -          | RelationshipImportEnabled  |
| - [relationshipRefreshEnabled](#relationshipRefreshEnabled ) | No      | boolean        | No         | -          | RelationshipRefreshEnabled |
| - [runBackgroundAnalysis](#runBackgroundAnalysis )           | No      | boolean        | No         | -          | RunBackgroundAnalysis      |

## <a name="version"></a>1. ![Required](https://img.shields.io/badge/Required-blue) Property `EditorSettings > version`

**Title:** Version

|          |                  |
| -------- | ---------------- |
| **Type** | `string or null` |

**Description:** Version of the dataset editor settings file format.

## <a name="showHiddenFields"></a>2. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > showHiddenFields`

**Title:** ShowHiddenFields

|          |           |
| -------- | --------- |
| **Type** | `boolean` |

**Description:** Whether hidden fields should be shown in a field list.

## <a name="autodetectRelationships"></a>3. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > autodetectRelationships`

**Title:** AutodetectRelationships

|          |           |
| -------- | --------- |
| **Type** | `boolean` |

**Description:** Whether relationships should be automatically detected when adding tables.

## <a name="parallelQueryLoading"></a>4. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > parallelQueryLoading`

**Title:** ParallelQueryLoading

|          |           |
| -------- | --------- |
| **Type** | `boolean` |

**Description:** Whether multiple M queries should be run in parallel.

## <a name="typeDetectionEnabled"></a>5. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > typeDetectionEnabled`

**Title:** TypeDetectionEnabled

|          |           |
| -------- | --------- |
| **Type** | `boolean` |

**Description:** Whether to detect column types and headers for unstructured data sources.

## <a name="relationshipImportEnabled"></a>6. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > relationshipImportEnabled`

**Title:** RelationshipImportEnabled

|          |           |
| -------- | --------- |
| **Type** | `boolean` |

**Description:** Whether relationships should be imported from data sources during the first load of data.

## <a name="relationshipRefreshEnabled"></a>7. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > relationshipRefreshEnabled`

**Title:** RelationshipRefreshEnabled

|          |           |
| -------- | --------- |
| **Type** | `boolean` |

**Description:** Whether relationships should be updated or deleted when refreshing data.

## <a name="runBackgroundAnalysis"></a>8. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `EditorSettings > runBackgroundAnalysis`

**Title:** RunBackgroundAnalysis

|          |           |
| -------- | --------- |
| **Type** | `boolean` |

**Description:** Whether to load data previews for the query editor in the background.

----------------------------------------------------------------------------------------------------------------------------
