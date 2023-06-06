This folder contains the authoritative JSON schema files for validating item metadata files. These schemas conform to the [Draft 7 specification](https://json-schema.org/specification-links.html#draft-7) of the [JSON schema spec](https://json-schema.org/specification.html).

The schemas can be used in external application development or as a direct reference "$schema" when editing the metadata files in a text editor like Visual Studio Code. 

To learn more, see [Editing JSON with Visual Studio Code](https://code.visualstudio.com/docs/languages/json).

# Report schemas

Within the [Report schemas folder](./report/README.md), you will find JSON schemas for the Report metadata files.

# Dataset schemas

Within the [Dataset schemas folder](./dataset/README.md), you will find JSON schemas for the Dataset metadata files.

# Common schemas

Within the [Common schemas folder](./common/README.md), you will find JSON schemas for metadata files common to all items.

# How to use JSON Schemas using Visual Studio Code

You can use Visual Studio Code as a code editor to author the metadata files and map the JSON schemas to the files being authored. This will permit validation, syntax highlighting, auto completion and tooltip documentation.

When authoring the document, only valid properties show up:

![Alt text](_images/vscode-schemas-context.png)

If a wrong property or type is specified an warning is emited:

![Alt text](_images/vscode-schemas-wrongproperty.png)

When you hover over properties, additional context is provided:

![Alt text](_images/vscode-schemas-context.png)

You can directly reference the schema by adding the "$schema" property to the edited file:

```json
{
  "$schema": "https://raw.githubusercontent.com/microsoft/powerbi-desktop-samples/main/item-schemas/report/definition.pbir-1.0.json",
  "version": "1.0",
  "datasetReference": {
    "byPath": {
      "path": "../Sales.Dataset"
    },
    "byConnection": null
  }
}

```

Or by mapping the metadata files to your VS Code user settings:

```json
{
    "json.schemas": [
        {
            "fileMatch": [
                "/*.Report/*.pbir"
            ],
            "url": "https://raw.githubusercontent.com/microsoft/powerbi-desktop-samples/main/item-schemas/report/definition.pbir-1.0.json"
        }
        ,
        {
            "fileMatch": [
                "/*.Dataset/*.pbidataset"
            ],
            "url": "https://raw.githubusercontent.com/microsoft/powerbi-desktop-samples/main/item-schemas/dataset/definition.pbidataset-1.0.json"
        }
        ,
        {
            "fileMatch": [
                "/*.Dataset/.pbi/editorSettings.json"
            ],
            "url": "https://raw.githubusercontent.com/microsoft/powerbi-desktop-samples/main/item-schemas/dataset/editorSettings-1.0.json"
        }
    ]
}

```