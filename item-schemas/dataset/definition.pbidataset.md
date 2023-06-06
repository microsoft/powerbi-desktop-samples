# DatasetDefinition

- [1. ![Required](https://img.shields.io/badge/Required-blue) Property `DatasetDefinition > version`](#version)
- [2. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `DatasetDefinition > settings`](#settings)

**Title:** DatasetDefinition

|                           |                                                                                                                                   |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                          |
| **Additional properties** | [![Any type: allowed](https://img.shields.io/badge/Any%20type-allowed-green)](# "Additional Properties of any type are allowed.") |

**Description:** The DatasetDefinition stored as definition.pbidataset holds information about the overall dataset definition. This file is required.

| Property                 | Pattern | Type           | Deprecated | Definition                       | Title/Description                                                                                                                                                                        |
| ------------------------ | ------- | -------------- | ---------- | -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| + [version](#version )   | No      | string or null | No         | -                                | Version                                                                                                                                                                                  |
| - [settings](#settings ) | No      | object or null | No         | In #/definitions/DatasetSettings | Settings for this dataset that do not impact the behavior of the data model itself. Instead, these settings control the behavior of other Power BI features associated with the dataset. |

## <a name="version"></a>1. ![Required](https://img.shields.io/badge/Required-blue) Property `DatasetDefinition > version`

**Title:** Version

|          |                  |
| -------- | ---------------- |
| **Type** | `string or null` |

**Description:** Version of the dataset artifact file format. This also serves as the version number for the .pbidataset file format.

## <a name="settings"></a>2. ![Optional](https://img.shields.io/badge/Optional-yellow) Property `DatasetDefinition > settings`

|                |                               |
| -------------- | ----------------------------- |
| **Type**       | `object or null`              |
| **Defined in** | #/definitions/DatasetSettings |

**Description:** Settings for this dataset that do not impact the behavior of the data model itself. Instead, these settings control the behavior of other Power BI features associated with the dataset.

----------------------------------------------------------------------------------------------------------------------------
