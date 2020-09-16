# DAX sample model

The **Adventure Works DW 2020** Power BI Desktop sample model is designed to support your DAX learning. The model is based on the [Adventure Works data warehouse sample](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=tsql#data-warehouse-downloads) for AdventureWorksDW2017—however, the data has been modified to suit the objectives of the sample model and updated to 2020. Download the [PBIX](Adventure%20Works%20DW%202020.pbix) or the [BAK](Adventure%20Works%20DW%202020.bak).

## Scenario
![An image of the Adventure Works company logo is shown.](https://docs.microsoft.com/en-us/power-bi/guidance/media/dax-sample-model/adventure-works-logo-150x150.png)

The Adventure Works company represents a bicycle manufacturer that sells bicycles and accessories to global markets. The company has their data warehouse data stored in an Azure SQL Database.

## Model structure

The model has seven tables:

|Table|Description|
|-----|-------|
|**Customer**|Describes customers and their geographic location. Customers purchase products online (Internet sales).|
|**Date**|There are three relationships between the **Date** and **Sales** tables, for order date, ship date, and due date. The order date relationship is active. The company's reports sales using a fiscal year that commences on July 1 of each year. The table is marked as a date table using the **Date** column.|
|**Product**|Stores finished products only.|
|**Reseller**|Describes resellers and their geographic location. Reseller on sell products to their customers.|
|**Sales**|Stores rows at sales order line grain. All financial values are in US dollars (USD). The earliest order date is July 1, 2017, and the latest order date is June 15, 2020.|
|**Sales Order**|Describes sales order and order line numbers, and also the sales channel, which is either **Reseller** or **Internet**. This table has a one-to-one relationship with the **Sales** table.|
|**Sales Territory**|Sales territories are organized into groups (North America, Europe, and Pacific), countries, and regions. Only the United States sells products at the region level.|

The model doesn't contain any DAX calculations.
