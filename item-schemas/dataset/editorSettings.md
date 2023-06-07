# EditorSettings

- [1. Property `EditorSettings > version`](#version)
- [2. Property `EditorSettings > showHiddenFields`](#showHiddenFields)
- [3. Property `EditorSettings > autodetectRelationships`](#autodetectRelationships)
- [4. Property `EditorSettings > parallelQueryLoading`](#parallelQueryLoading)
- [5. Property `EditorSettings > typeDetectionEnabled`](#typeDetectionEnabled)
- [6. Property `EditorSettings > relationshipImportEnabled`](#relationshipImportEnabled)
- [7. Property `EditorSettings > relationshipRefreshEnabled`](#relationshipRefreshEnabled)
- [8. Property `EditorSettings > runBackgroundAnalysis`](#runBackgroundAnalysis)

**Title:** EditorSettings

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

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

## <a name="version"></a>1. Property `EditorSettings > version`

**Title:** Version

|              |                  |
| ------------ | ---------------- |
| **Type**     | `string or null` |
| **Required** | Yes              |

**Description:** Version of the dataset editor settings file format.

## <a name="showHiddenFields"></a>2. Property `EditorSettings > showHiddenFields`

**Title:** ShowHiddenFields

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |

**Description:** Whether hidden fields should be shown in a field list.

## <a name="autodetectRelationships"></a>3. Property `EditorSettings > autodetectRelationships`

**Title:** AutodetectRelationships

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |

**Description:** Whether relationships should be automatically detected when adding tables.

## <a name="parallelQueryLoading"></a>4. Property `EditorSettings > parallelQueryLoading`

**Title:** ParallelQueryLoading

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |

**Description:** Whether multiple M queries should be run in parallel.

## <a name="typeDetectionEnabled"></a>5. Property `EditorSettings > typeDetectionEnabled`

**Title:** TypeDetectionEnabled

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |

**Description:** Whether to detect column types and headers for unstructured data sources.

## <a name="relationshipImportEnabled"></a>6. Property `EditorSettings > relationshipImportEnabled`

**Title:** RelationshipImportEnabled

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |

**Description:** Whether relationships should be imported from data sources during the first load of data.

## <a name="relationshipRefreshEnabled"></a>7. Property `EditorSettings > relationshipRefreshEnabled`

**Title:** RelationshipRefreshEnabled

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |

**Description:** Whether relationships should be updated or deleted when refreshing data.

## <a name="runBackgroundAnalysis"></a>8. Property `EditorSettings > runBackgroundAnalysis`

**Title:** RunBackgroundAnalysis

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | No        |

**Description:** Whether to load data previews for the query editor in the background.

----------------------------------------------------------------------------------------------------------------------------
