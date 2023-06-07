# ReportDefinition

_The ReportDefinition stored as definition.pbir provides the overall definition of a report. It contains metadata about the overall file structure and provides core settings. It holds the DatasetReference where exactly one of either byPath or byConnection is required. The byConnection property would typically be used for LiveConnect scenarios. This file is required._

Type: `object`

<i id="">path: #</i>

**_Properties_**

 - <b id="#/properties/version">version</b> `required`
	 - ### Version
	 - _Version of the report artifact file format.  This also serves as the version number for the .pbir file format._
	 - Types: `string`, `null`
	 - <i id="/properties/version">path: #/properties/version</i>
 - <b id="#/properties/datasetReference">datasetReference</b>
	 - <i id="/properties/datasetReference">path: #/properties/datasetReference</i>
	 - &#36;ref: [#/definitions/DatasetReference](#/definitions/DatasetReference)
# definitions

**_DatasetReference_**

 - ## DatasetReference
 - _Describes the dataset bound to this report._
 - Types: `object`, `null`
 - <i id="/definitions/DatasetReference">path: #/definitions/DatasetReference</i>
 - **_Properties_**
	 - <b id="#/definitions/DatasetReference/properties/byPath">byPath</b>
		 - <i id="/definitions/DatasetReference/properties/byPath">path: #/definitions/DatasetReference/properties/byPath</i>
		 - &#36;ref: [#/definitions/ReportDatasetReferenceByPath](#/definitions/ReportDatasetReferenceByPath)
	 - <b id="#/definitions/DatasetReference/properties/byConnection">byConnection</b>
		 - <i id="/definitions/DatasetReference/properties/byConnection">path: #/definitions/DatasetReference/properties/byConnection</i>
		 - &#36;ref: [#/definitions/ReportDatasetReferenceByConnection](#/definitions/ReportDatasetReferenceByConnection)


**_ReportDatasetReferenceByConnection_**

 - ## ByConnection
 - _Provides a reference to a remote dataset using a connection string._
 - Types: `object`, `null`
 - <i id="/definitions/ReportDatasetReferenceByConnection">path: #/definitions/ReportDatasetReferenceByConnection</i>
 - **_Properties_**
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/connectionString">connectionString</b> `required`
		 - #### ConnectionString
		 - _The connection string referring to the remote dataset._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/connectionString">path: #/definitions/ReportDatasetReferenceByConnection/properties/connectionString</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/pbiServiceModelId">pbiServiceModelId</b> `required`
		 - #### PbiServiceModelId
		 - _Information used by Power BI Service._
		 - Types: `integer`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/pbiServiceModelId">path: #/definitions/ReportDatasetReferenceByConnection/properties/pbiServiceModelId</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/pbiModelVirtualServerName">pbiModelVirtualServerName</b> `required`
		 - #### PbiModelVirtualServerName
		 - _Information used by Power BI Service._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/pbiModelVirtualServerName">path: #/definitions/ReportDatasetReferenceByConnection/properties/pbiModelVirtualServerName</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/pbiModelDatabaseName">pbiModelDatabaseName</b> `required`
		 - #### PbiModelDatabaseName
		 - _Information used by Power BI Service._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/pbiModelDatabaseName">path: #/definitions/ReportDatasetReferenceByConnection/properties/pbiModelDatabaseName</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/name">name</b> `required`
		 - #### Name
		 - _The name of the connection._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/name">path: #/definitions/ReportDatasetReferenceByConnection/properties/name</i>
	 - <b id="#/definitions/ReportDatasetReferenceByConnection/properties/connectionType">connectionType</b> `required`
		 - #### ConnectionType
		 - _The type of connection, typically would be one of the following: pbiServiceLive, pbiServiceXmlaStyleLive, pbiserviceOnPremLive, analysisServicesDatabaseLive._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByConnection/properties/connectionType">path: #/definitions/ReportDatasetReferenceByConnection/properties/connectionType</i>


**_ReportDatasetReferenceByPath_**

 - ## ByPath
 - _Provides a reference to a local dataset artifact definition._
 - Types: `object`, `null`
 - <i id="/definitions/ReportDatasetReferenceByPath">path: #/definitions/ReportDatasetReferenceByPath</i>
 - **_Properties_**
	 - <b id="#/definitions/ReportDatasetReferenceByPath/properties/path">path</b> `required`
		 - #### Path
		 - _Provides a reference to a remote dataset using a connection string._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportDatasetReferenceByPath/properties/path">path: #/definitions/ReportDatasetReferenceByPath/properties/path</i>
