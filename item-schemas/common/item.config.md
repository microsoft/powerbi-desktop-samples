# ItemConfig

_The ItemConfig stored as item.config.json holds the LogicalId of the item and identifies this directory as a Fabric item. There is an ItemConfig file in both the Report and Dataset folders. This file is optional._

Type: `object`

<i id="">path: #</i>

This schema <u>does not</u> accept additional properties.

**_Properties_**

 - <b id="#/properties/version">version</b> `required`
	 - ### Version
	 - _The verion of this item. The current latest version is 1.0_
	 - Types: `string`, `null`
	 - <i id="/properties/version">path: #/properties/version</i>
	 - The value is restricted to the following: 
		 1. _"1.0"_
 - <b id="#/properties/logicalId">logicalId</b> `required`
	 - ### LogicalId
	 - _The logicalId of the item is a workspace-unique immutable identifier representing a logical item and its source control representation. There is a different logicalId in the Report and Dataset folder._
	 - Type: `string`
	 - <i id="/properties/logicalId">path: #/properties/logicalId</i>
