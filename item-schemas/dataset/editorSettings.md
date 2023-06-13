# EditorSettings

_The EditorSettings stored as editorSettings.json holds dataset editor settings that are saved as part of the dataset definition for use across users or environments. This file is optional._

Type: `object`

<i id="">path: #</i>

This schema <u>does not</u> accept additional properties.

**_Properties_**

 - <b id="#/properties/version">version</b> `required`
	 - ### Version
	 - _Version of the dataset editor settings file format._
	 - Types: `string`, `null`
	 - <i id="/properties/version">path: #/properties/version</i>
	 - The value is restricted to the following: 
		 1. _"1.0"_
 - <b id="#/properties/showHiddenFields">showHiddenFields</b>
	 - ### ShowHiddenFields
	 - _Whether hidden fields should be shown in a field list._
	 - Type: `boolean`
	 - <i id="/properties/showHiddenFields">path: #/properties/showHiddenFields</i>
 - <b id="#/properties/autodetectRelationships">autodetectRelationships</b>
	 - ### AutodetectRelationships
	 - _Whether relationships should be automatically detected when adding tables._
	 - Type: `boolean`
	 - <i id="/properties/autodetectRelationships">path: #/properties/autodetectRelationships</i>
 - <b id="#/properties/parallelQueryLoading">parallelQueryLoading</b>
	 - ### ParallelQueryLoading
	 - _Whether multiple M queries should be run in parallel._
	 - Type: `boolean`
	 - <i id="/properties/parallelQueryLoading">path: #/properties/parallelQueryLoading</i>
 - <b id="#/properties/typeDetectionEnabled">typeDetectionEnabled</b>
	 - ### TypeDetectionEnabled
	 - _Whether to detect column types and headers for unstructured data sources._
	 - Type: `boolean`
	 - <i id="/properties/typeDetectionEnabled">path: #/properties/typeDetectionEnabled</i>
 - <b id="#/properties/relationshipImportEnabled">relationshipImportEnabled</b>
	 - ### RelationshipImportEnabled
	 - _Whether relationships should be imported from data sources during the first load of data._
	 - Type: `boolean`
	 - <i id="/properties/relationshipImportEnabled">path: #/properties/relationshipImportEnabled</i>
 - <b id="#/properties/relationshipRefreshEnabled">relationshipRefreshEnabled</b>
	 - ### RelationshipRefreshEnabled
	 - _Whether relationships should be updated or deleted when refreshing data._
	 - Type: `boolean`
	 - <i id="/properties/relationshipRefreshEnabled">path: #/properties/relationshipRefreshEnabled</i>
 - <b id="#/properties/runBackgroundAnalysis">runBackgroundAnalysis</b>
	 - ### RunBackgroundAnalysis
	 - _Whether to load data previews for the query editor in the background._
	 - Type: `boolean`
	 - <i id="/properties/runBackgroundAnalysis">path: #/properties/runBackgroundAnalysis</i>
