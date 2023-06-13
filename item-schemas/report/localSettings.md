# ReportLocalSettings

_The ReportLocalSettings stored as localSettings.json holds report settings that only apply for the current user/machine. This file is optional._

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
 - <b id="#/properties/remoteArtifacts">remoteArtifacts</b>
	 - ### RemoteArtifacts
	 - _Describes the published Power BI artifacts associated with this definition._
	 - Types: `array`, `null`
	 - <i id="/properties/remoteArtifacts">path: #/properties/remoteArtifacts</i>
		 - **_Items_**
		 - <i id="/properties/remoteArtifacts/items">path: #/properties/remoteArtifacts/items</i>
		 - &#36;ref: [#/definitions/ReportRemoteArtifact](#/definitions/ReportRemoteArtifact)
 - <b id="#/properties/securityBindingsSignature">securityBindingsSignature</b>
	 - ### SecurityBindingsSignature
	 - _A base64 encoded signature which when absent or invalid will reset saved properties which require user review or consent._
	 - Types: `string`, `null`
	 - <i id="/properties/securityBindingsSignature">path: #/properties/securityBindingsSignature</i>
# definitions

**_ReportRemoteArtifact_**

 - Type: `object`
 - <i id="/definitions/ReportRemoteArtifact">path: #/definitions/ReportRemoteArtifact</i>
 - This schema <u>does not</u> accept additional properties.
 - **_Properties_**
	 - <b id="#/definitions/ReportRemoteArtifact/properties/reportId">reportId</b> `required`
		 - #### ReportId
		 - _The ID of a published report created from this definition._
		 - Types: `string`, `null`
		 - <i id="/definitions/ReportRemoteArtifact/properties/reportId">path: #/definitions/ReportRemoteArtifact/properties/reportId</i>


