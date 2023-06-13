# ReportDefinition

_The ReportDefinition is stored as definition.pbir. It contains metadata about the overall file structure, holds core settings, and holds a reference to the dataset used by this report. This file is required._

Type: `object`

<i id="">path: #</i>

This schema <u>does not</u> accept additional properties.

**_Properties_**

 - <b id="#/properties/version">version</b> `required`
	 - ### Version
	 - _Version of the report artifact file format.  This also serves as the version number for the .pbir file format._
	 - Types: `string`, `null`
	 - <i id="/properties/version">path: #/properties/version</i>
	 - The value is restricted to the following: 
		 1. _"1.0"_
 - <b id="#/properties/datasetReference">datasetReference</b>
	 - <i id="/properties/datasetReference">path: #/properties/datasetReference</i>
	 - &#36;ref: [#/definitions/DatasetReference](#/definitions/DatasetReference)
# definitions

**_DatasetReference_**

 - ## DatasetReference
 - _The DatasetReference defines the dataset that is bound to this report. It is required to have exactly one of either the byPath or byConnection properties. The byConnection property would typically be used for LiveConnect scenarios whereas byPath would point at a local dataset._
 - Types: `object`, `null`
 - <i id="/definitions/DatasetReference">path: #/definitions/DatasetReference</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/DatasetReference/properties/byPath">byPath</b>
		 - <i id="/definitions/DatasetReference/properties/byPath">path: #/definitions/DatasetReference/properties/byPath</i>
		 - &#36;ref: [#/definitions/ReportDatasetReferenceByPath](#/definitions/ReportDatasetReferenceByPath)
	 - <b id="#/definitions/DatasetReference/properties/byConnection">byConnection</b>
		 - <i id="/definitions/DatasetReference/properties/byConnection">path: #/definitions/DatasetReference/properties/byConnection</i>
		 - &#36;ref: [#/definitions/ReportDatasetReferenceByConnection](#/definitions/ReportDatasetReferenceByConnection)


**_ReportDatasetReferenceByConnection_**

 - ## ByConnection
 - _Provides a reference to a remote dataset using a connection string. The connection string must point to a dataset hosted in the Microsoft Fabric service.  Connections to other Analysis Services semantic models must use a byPath reference to a dataset definition containing a modelReference.json file._
 - Types: `object`, `null`
 - <i id="/definitions/ReportDatasetReferenceByConnection">path: #/definitions/ReportDatasetReferenceByConnection</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/connectionString">connectionString</b> `required`
		 - #### ConnectionString
		 - _The connection string referring to the remote dataset._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/connectionString">path: #/definitions/ReportDatasetReferenceByConnection/properties/connectionString</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/pbiServiceModelId">pbiServiceModelId</b> `required`
		 - #### PbiServiceModelId
		 - _The unique identifier for the target dataset in the Microsoft Fabric service._
		 - Types: `integer`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/pbiServiceModelId">path: #/definitions/ReportDatasetReferenceByConnection/properties/pbiServiceModelId</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/pbiModelVirtualServerName">pbiModelVirtualServerName</b> `required`
		 - #### PbiModelVirtualServerName
		 - _The virtual server name for the target dataset in the Microsoft Fabric service._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/pbiModelVirtualServerName">path: #/definitions/ReportDatasetReferenceByConnection/properties/pbiModelVirtualServerName</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/pbiModelDatabaseName">pbiModelDatabaseName</b> `required`
		 - #### PbiModelDatabaseName
		 - _The database name for the target dataset in the Microsoft Fabric service._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/pbiModelDatabaseName">path: #/definitions/ReportDatasetReferenceByConnection/properties/pbiModelDatabaseName</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/name">name</b> `required`
		 - #### Name
		 - _The name of the connection. The value of this property must be 'EntityDataSource'. This property will be removed in a future release._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/name">path: #/definitions/ReportDatasetReferenceByConnection/properties/name</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/connectionType">connectionType</b> `required`
		 - #### ConnectionType
		 - _The type of connection. The value of this property must be 'pbiServiceXmlaStyleLive'. This property will be removed in a future release._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/connectionType">path: #/definitions/ReportDatasetReferenceByConnection/properties/connectionType</i>


**_ReportDatasetReferenceByPath_**

 - ## ByPath
 - _Provides a reference to a local dataset artifact definition._
 - Types: `object`, `null`
 - <i id="/definitions/ReportDatasetReferenceByPath">path: #/definitions/ReportDatasetReferenceByPath</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/ReportDatasetReferenceByPath/properties/path">path</b> `required`
		 - #### Path
		 - _A relative path from this file to the target dataset artifact folder. Uses ‘/’ as a directory separator._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByPath/properties/path">path: #/definitions/ReportDatasetReferenceByPath/properties/path</i>


