# ItemMetadata

_The ItemMetadata stored as item.metadata.json holds the Type and DisplayName of the item. The DisplayName is what is shown in the title bar of Power BI Desktop. There is an ItemMetadata file in both the Report and Dataset folders. This file is optional._

Type: `object`

<i id="">path: #</i>

This schema <u>does not</u> accept additional properties.

**_Properties_**

 - <b id="#/properties/type">type</b>
	 - ### Type
	 - _The type of the item either "report" or "dataset"._
	 - Types: `string`, `null`
	 - <i id="/properties/type">path: #/properties/type</i>
 - <b id="#/properties/displayName">displayName</b>
	 - ### DisplayName
	 - _The display name of the item._
	 - Types: `string`, `null`
	 - <i id="/properties/displayName">path: #/properties/displayName</i>
 - <b id="#/properties/description">description</b>
	 - ### Description
	 - _The description of the item._
	 - Types: `string`, `null`
	 - <i id="/properties/description">path: #/properties/description</i>
