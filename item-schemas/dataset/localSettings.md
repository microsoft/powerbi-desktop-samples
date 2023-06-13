# LocalSettings

_The LocalSettings stored as localSettings.json holds dataset settings that only apply to the current user/machine. This file is optional._

Type: `object`

<i id="">path: #</i>

This schema <u>does not</u> accept additional properties.

**_Properties_**

 - <b id="#/properties/version">version</b> `required`
	 - ### Version
	 - _Version of the local settings file format._
	 - Types: `string`, `null`
	 - <i id="/properties/version">path: #/properties/version</i>
	 - The value is restricted to the following: 
		 1. _"1.0"_
 - <b id="#/properties/userConsent">userConsent</b>
	 - <i id="/properties/userConsent">path: #/properties/userConsent</i>
	 - &#36;ref: [#/definitions/DatasetUserConsent](#/definitions/DatasetUserConsent)
 - <b id="#/properties/remoteArtifacts">remoteArtifacts</b>
	 - ### RemoteArtifacts
	 - _Describes the published Power BI artifacts associated with this definition._
	 - Types: `array`, `null`
	 - <i id="/properties/remoteArtifacts">path: #/properties/remoteArtifacts</i>
		 - **_Items_**
		 - <i id="/properties/remoteArtifacts/items">path: #/properties/remoteArtifacts/items</i>
		 - &#36;ref: [#/definitions/DatasetRemoteArtifact](#/definitions/DatasetRemoteArtifact)
 - <b id="#/properties/securityBindingsSignature">securityBindingsSignature</b>
	 - ### SecurityBindingsSignature
	 - _A base64 encoded signature which when absent or invalid will reset saved properties which require user review or consent._
	 - Types: `string`, `null`
	 - <i id="/properties/securityBindingsSignature">path: #/properties/securityBindingsSignature</i>
# definitions

**_DatasetRemoteArtifact_**

 - Type: `object`
 - <i id="/definitions/DatasetRemoteArtifact">path: #/definitions/DatasetRemoteArtifact</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/DatasetRemoteArtifact/properties/datasetId">datasetId</b> `required`
		 - #### DatasetId
		 - _The ID of a published dataset created from this definition._
		 - Types: `string`, `null`
		 - <i id="/definitions/DatasetRemoteArtifact/properties/datasetId">path: #/definitions/DatasetRemoteArtifact/properties/datasetId</i>


**_DatasetUserConsent_**

 - ## UserConsent
 - _Holds information about whether the user has agreed to the use of various features._
 - Types: `object`, `null`
 - <i id="/definitions/DatasetUserConsent">path: #/definitions/DatasetUserConsent</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/DatasetUserConsent/properties/compositeModel">compositeModel</b>
		 - #### CompositeModel
		 - _Whether the user has consented to the use of models with multiple direct query data sources._
		 - Type: `boolean`
		 - <i id="/definitions/DatasetUserConsent/properties/compositeModel">path: #/definitions/DatasetUserConsent/properties/compositeModel</i>
	 - <b id="#/definitions/DatasetUserConsent/properties/qnAForLiveConnect">qnAForLiveConnect</b>
		 - #### QnAForLiveConnect
		 - _Whether the user has consented to the use of Q&A for live connections to models hosted outside Power BI._
		 - Type: `boolean`
		 - <i id="/definitions/DatasetUserConsent/properties/qnAForLiveConnect">path: #/definitions/DatasetUserConsent/properties/qnAForLiveConnect</i>
	 - <b id="#/definitions/DatasetUserConsent/properties/dynamicQueryParameters">dynamicQueryParameters</b>
		 - #### DynamicQueryParameters
		 - _Whether the user has consented to the use of dynamic M query parameters in their report._
		 - Type: `boolean`
		 - <i id="/definitions/DatasetUserConsent/properties/dynamicQueryParameters">path: #/definitions/DatasetUserConsent/properties/dynamicQueryParameters</i>


