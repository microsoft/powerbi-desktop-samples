# DatasetDefinition

_The DatasetDefinition stored as definition.pbidataset holds information about the overall dataset definition. This file is required._

Type: `object`

<i id="">path: #</i>

This schema <u>does not</u> accept additional properties.

**_Properties_**

 - <b id="#/properties/version">version</b> `required`
	 - ### Version
	 - _Version of the dataset item file format. This also serves as the version number for the .pbidataset file format._
	 - Types: `string`, `null`
	 - <i id="/properties/version">path: #/properties/version</i>
	 - The value is restricted to the following: 
		 1. _"1.0"_
 - <b id="#/properties/settings">settings</b>
	 - <i id="/properties/settings">path: #/properties/settings</i>
	 - &#36;ref: [#/definitions/DatasetSettings](#/definitions/DatasetSettings)
# definitions

**_DatasetSettings_**

 - ## Settings
 - _Settings for this dataset that do not impact the behavior of the data model itself. Instead, these settings control the behavior of other Power BI features associated with the dataset._
 - Types: `object`, `null`
 - <i id="/definitions/DatasetSettings">path: #/definitions/DatasetSettings</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/DatasetSettings/properties/qnaEnabled">qnaEnabled</b>
		 - #### QnaEnabled
		 - _Whether Q&A is enabled for this dataset._
		 - Type: `boolean`
		 - <i id="/definitions/DatasetSettings/properties/qnaEnabled">path: #/definitions/DatasetSettings/properties/qnaEnabled</i>
	 - <b id="#/definitions/DatasetSettings/properties/qnaLsdlSharingPermissions">qnaLsdlSharingPermissions</b>
		 - #### QnaLsdlSharingPermissions
		 - _Describes how the linguistic schema (LSDL) can be shared with other users within the same tenant. Allowed values are 0 (LSDL can be shared with users with read permission) and 1 (LSDL can be shared with all users)._
		 - Type: `integer`
		 - <i id="/definitions/DatasetSettings/properties/qnaLsdlSharingPermissions">path: #/definitions/DatasetSettings/properties/qnaLsdlSharingPermissions</i>
		 - The value is restricted to the following: 
			 1. `0`
			 2. `1`


