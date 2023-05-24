# ReportDefinition

- [1. Property `ReportDefinition > version`](#version)
- [2. Property `ReportDefinition > datasetReference`](#datasetReference)

**Title:** ReportDefinition

|                           |                                                                           |
| ------------------------- | ------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                  |
| **Required**              | No                                                                        |
| **Additional properties** | [[Any type: allowed]](# "Additional Properties of any type are allowed.") |

**Description:** The ReportDefinition stored as definition.pbir provides the overall definition of a report. It contains metadata about the overall file structure and provides core settings. It holds the DatasetReference where exactly one of either byPath or byConnection is required. The byConnection property would typically be used for LiveConnect scenarios. This file is required.

| Property                                 | Pattern | Type           | Deprecated | Definition                        | Title/Description                           |
| ---------------------------------------- | ------- | -------------- | ---------- | --------------------------------- | ------------------------------------------- |
| + [version](#version )                   | No      | string or null | No         | -                                 | Version                                     |
| - [datasetReference](#datasetReference ) | No      | object or null | No         | In #/definitions/DatasetReference | Describes the dataset bound to this report. |

## <a name="version"></a>1. Property `ReportDefinition > version`

**Title:** Version

|              |                  |
| ------------ | ---------------- |
| **Type**     | `string or null` |
| **Required** | Yes              |

**Description:** Version of the report artifact file format.  This also serves as the version number for the .pbir file format.

## <a name="datasetReference"></a>2. Property `ReportDefinition > datasetReference`

|                |                                |
| -------------- | ------------------------------ |
| **Type**       | `object or null`               |
| **Required**   | No                             |
| **Defined in** | #/definitions/DatasetReference |

**Description:** Describes the dataset bound to this report.

----------------------------------------------------------------------------------------------------------------------------
