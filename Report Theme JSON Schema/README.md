# Report theme JSON schema

This folder contains the authoritative JSON schema files for validating report themes in [Power BI Desktop](https://powerbi.microsoft.com/desktop/).  These schemas conform to the [Draft 7 specification](https://json-schema.org/specification-links.html#draft-7) of the [JSON schema spec](https://json-schema.org/specification.html).

Each file is tagged with the monthly release version of Desktop.  Inside the file, the `description` field describes the "exploration version" that the schema is valid for; this is generally matched with the release version of Power BI Desktop.

As part of our on-going effort to provide complete specification of our file format, subsequent versions of this schema will feature mostly additive changes as new formatting settings are added.

| Power BI Desktop version | Date     |  Exploration version | Schema name                                                    |
|--------------------------|----------|----------------------|----------------------------------------------------------------|
| 2.136.x.x                | Sep 2024 | 5.58                 | [reportThemeSchema-2.136.json](./reportThemeSchema-2.136.json) |
| 2.132.x.x                | Aug 2024 | 5.57                 | [reportThemeSchema-2.132.json](./reportThemeSchema-2.132.json) |
| 2.131.x.x                | Jul 2024 | 5.56                 | [reportThemeSchema-2.131.json](./reportThemeSchema-2.131.json) |
| 2.130.x.x                | Jun 2024 | 5.55                 | [reportThemeSchema-2.130.json](./reportThemeSchema-2.130.json) |
| 2.129.x.x                | May 2024 | 5.54                 | [reportThemeSchema-2.129.json](./reportThemeSchema-2.129.json) |
| 2.128.x.x                | Apr 2024 | 5.53                 | [reportThemeSchema-2.128.json](./reportThemeSchema-2.128.json) |
| 2.127.x.x                | Mar 2024 | 5.52                 | [reportThemeSchema-2.127.json](./reportThemeSchema-2.127.json) |
| 2.126.x.x                | Feb 2024 | 5.51                 | [reportThemeSchema-2.126.json](./reportThemeSchema-2.126.json) |
| 2.124.x.x                | Dec 2023 | 5.50                 | [reportThemeSchema-2.124.json](./reportThemeSchema-2.124.json) |
| 2.123.x.x                | Nov 2023 | 5.49                 | [reportThemeSchema-2.123.json](./reportThemeSchema-2.123.json) |
| 2.122.x.x                | Oct 2023 | 5.48                 | [reportThemeSchema-2.122.json](./reportThemeSchema-2.122.json) |
| 2.121.x.x                | Sep 2023 | 5.48                 | [reportThemeSchema-2.121.json](./reportThemeSchema-2.121.json) |
| 2.120.x.x                | Aug 2023 | 5.47                 | [reportThemeSchema-2.120.json](./reportThemeSchema-2.120.json) |
| 2.119.x.x                | Jul 2023 | 5.46                 | [reportThemeSchema-2.119.json](./reportThemeSchema-2.119.json) |
| 2.118.x.x                | Jun 2023 | 5.45                 | [reportThemeSchema-2.118.json](./reportThemeSchema-2.118.json) |
| 2.117.x.x                | May 2023 | 5.44                 | [reportThemeSchema-2.117.json](./reportThemeSchema-2.117.json) |
| 2.116.x.x                | Apr 2023 | 5.43                 | [reportThemeSchema-2.116.json](./reportThemeSchema-2.116.json) |
| 2.115.x.x                | Mar 2023 | 5.42                 | [reportThemeSchema-2.115.json](./reportThemeSchema-2.115.json) |
| 2.114.x.x                | Feb 2023 | 5.41                 | [reportThemeSchema-2.114.json](./reportThemeSchema-2.114.json) |

## Using the JSON schema

We anticipate two primary use cases for this schema.  One is for report theme authors, and the other is for report theme ISVs.  As always, you can find the [general documentation for report themes on the Microsoft docs site](https://learn.microsoft.com/power-bi/create-reports/desktop-report-themes).

Each formatting option under the `visualStyles` top-level property is tagged with the `title` and `description` that generally matches the English (en-US) translation text of the formatting property as it shows in the Formatting pane within Power BI Desktop.

### As a report theme author

If you are building custom report themes, you can use this schema to identify what formatting property defaults can be specified within your custom theme.

While [the Microsoft docs site](https://learn.microsoft.com/power-bi/create-reports/desktop-report-themes#report-theme-json-file-format) contains information about semantic colors, icons, and text styles, it does not specify all per-visual formatting settings.  As a general rule, all formatting that is controlled within the format pane within Power BI Desktop can also be specified with a different default by a custom theme.  The JSON schema helps to identify what these properties are called, their valid values, and how they should be specified.

Various IDEs can support in-line validation of JSON file authoring.  Here, we'll use the example of Visual Studio Code's [support for JSON schemas](https://code.visualstudio.com/docs/languages/json#_json-schemas-and-settings).

Download the appropriate schema file to your workstation, then create a blank JSON file alongside the downloaded file.  You can reference the schema from within your custom theme using the `"$schema"` property, like so:

![Specifying a "$schema" top-level property in a JSON file, referencing a local reporThemeSchema.json file](images/schema-spec.png)

You can also directly reference the "raw" HTML link of the schema in the repository, though note that you need an active internet connection and allow Visual Studio Code access to the remote resource.

Once you link up the schema, you can use autocomplete to understand the structure and available formatting options available.  Trigger autocomplete explicitly by using the key combination <kbd>Ctrl</kbd> + <kbd>Space</kbd>.  The description pop-up will show the formatting item's display name and description as they show in the Formatting pane, if available:

![Performing 'autocomplete' on a formatting option's value shows the available values](images/autocomplete.png)

Validation errors will show as yellow error lines (much like bad grammar identified in Microsoft Word) that are required to be fixed to be valid report themes.

![Yellow squiggly lines under an unrecognized enum value, with an error pop-up describing valid enum values for drop shadow presets](images/errors.png)

### As a report theme application builder (ISV)

Our schemas conform to [the draft-7 JSON schema spec](https://json-schema.org/specification-links.html#draft-7).  You may use this schema to help identify and document all available formatting to your clients, or use this schema in applications to programmatically generate custom theme JSON files.

## Use of the JSON theme schema

These schemas are used verbatim inside of Power BI Desktop to validate custom JSON theme when they are first imported to a report.  If the validation fails, Power BI Desktop will reject the custom theme.

The error messges that we generate in Power BI Desktop are based on [the Ajv library](https://ajv.js.org/); you may get different error messages if you use a different JSON schema validator.

## Limitations

We currently do not support the following items in the custom report theme JSON, though we may add support given feedback:
* References to dynamic content that reports support (other than `ThemeDataColor` expressions), e.g. `expr: { SparklineData: { ... } }`
* References from formatting colors to semantic colors, e.g. `"foreground"` for a `Fill` type.
* References to model-specific items, such as _conditional formatting_ that depends on fields or data values

### Known issues
The following describes known issues in previously-released reportThemeSchema JSON files.  "Open issues" are not prioritized for quick fixing and will be priotized as time allows.

#### Open issues

* Defining a default "canvas size" doesn't work; see [Issue #51](https://github.com/microsoft/powerbi-desktop-samples/issues/51).

### Fixed in September 2024 (2.136)

* All lists of formatting objects and properties are now in alphabetical order in the schema.  This change prevents extra needless diffs between schema versions due to code and capability refactoring, making it clearer what formatting options are added month-to-month.

#### Fixed in December 2023 (2.124)

* Default "group" visualType styling is exported into the schema (visual container groups)
* Export well-known `$id` repetition like "Active" and "Available" slicer pane cards, "default/hover/active/disabled" actionButton states, "default" for cardVisual/advancedSlicerVisual; see [Issue #59](https://github.com/microsoft/powerbi-desktop-samples/issues/59).

#### Fixed in May 2023 (2.117)
Issues fixed in the May 2023 release (2.117) of Power BI Desktop:
* Enumeration values are not clearly defined such as "labelOrientation"; took the fix of [using enum descriptors with `const`](https://github.com/json-schema-org/json-schema-spec/issues/57#issuecomment-247861695)
* Schema for "image" visualType is now exported + supported

#### Fixed in February 2023 (2.114)
Issues in the February 2023 release (2.114) and fixed in the March 2023 release (2.115) of Power BI Desktop:
* The top-level `icons` schema only supports icons defined in a list, not as a named object list.
* Certain "verticalAlignment" formatting options may only accept horizontal alignment options such as "left", "center", and "right" instead of "top", "middle", and "bottom".
* Eight-digit hex colors were not allowed for `Fill` definitions, where the last octet describes alpha transparency, e.g.: `#0000ff7f` -> `rgba(0, 0, 255, 0.5)`


## Comments or suggestions

Please leave suggestions and tag @yelper in your issue that you open on this repository.
