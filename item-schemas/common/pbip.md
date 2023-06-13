# ItemShortcut

_The ItemShortcut is a file that ends in a .pbip extension. It is the default shortcut for opening up pbip based items and holds a link to the report path as well as other settings. This file is optional._

Type: `object`

<i id="">path: #</i>

This schema <u>does not</u> accept additional properties.

**_Properties_**

 - <b id="#/properties/version">version</b> `required`
	 - ### Version
	 - _The version of the item shortcut file format._
	 - Type: `string`
	 - <i id="/properties/version">path: #/properties/version</i>
	 - The value is restricted to the following: 
		 1. _"1.0"_
 - <b id="#/properties/artifacts">artifacts</b> `required`
	 - ### Artifacts
	 - _The items referenced by this shortcut file._
	 - Type: `array`
	 - <i id="/properties/artifacts">path: #/properties/artifacts</i>
		 - **_Items_**
		 - <i id="/properties/artifacts/items">path: #/properties/artifacts/items</i>
		 - &#36;ref: [#/definitions/ArtifactShortcutContainer](#/definitions/ArtifactShortcutContainer)
 - <b id="#/properties/settings">settings</b>
	 - <i id="/properties/settings">path: #/properties/settings</i>
	 - &#36;ref: [#/definitions/ArtifactShortcutSettings](#/definitions/ArtifactShortcutSettings)
# definitions

**_ArtifactShortcutContainer_**

 - Type: `object`
 - <i id="/definitions/ArtifactShortcutContainer">path: #/definitions/ArtifactShortcutContainer</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/ArtifactShortcutContainer/properties/report">report</b> `required`
		 - <i id="/definitions/ArtifactShortcutContainer/properties/report">path: #/definitions/ArtifactShortcutContainer/properties/report</i>
		 - &#36;ref: [#/definitions/ArtifactShortcutReportReference](#/definitions/ArtifactShortcutReportReference)


**_ArtifactShortcutReportReference_**

 - ## Report
 - _Describes a reference to a report item._
 - Type: `object`
 - <i id="/definitions/ArtifactShortcutReportReference">path: #/definitions/ArtifactShortcutReportReference</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/ArtifactShortcutReportReference/properties/path">path</b> `required`
		 - #### Path
		 - _The path to the report item. This must be a relative path and ‘/’ must be used as the directory separator._
		 - Type: `string`
		 - <i id="/definitions/ArtifactShortcutReportReference/properties/path">path: #/definitions/ArtifactShortcutReportReference/properties/path</i>


**_ArtifactShortcutSettings_**

 - ## Settings
 - _Holds settings applied when opening this item shortcut._
 - Types: `object`, `null`
 - <i id="/definitions/ArtifactShortcutSettings">path: #/definitions/ArtifactShortcutSettings</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/ArtifactShortcutSettings/properties/enableAutoRecovery">enableAutoRecovery</b>
		 - #### EnableAutoRecovery
		 - _Whether Power BI Desktop should periodically save a copy of the open report and dataset to guard against the program closing unexpectedly._
		 - Type: `boolean`
		 - <i id="/definitions/ArtifactShortcutSettings/properties/enableAutoRecovery">path: #/definitions/ArtifactShortcutSettings/properties/enableAutoRecovery</i>


