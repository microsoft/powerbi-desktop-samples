# Power BI Desktop Performance Analyzer

In Power BI Desktop you can find out how each of your report elements, such as visuals and DAX formulas, are performing. Using the [Performance Analyzer](https://docs.microsoft.com/en-us/power-bi/desktop-performance-analyzer), you can see and record logs that measure how each of your report elements performs when users interact with them, and which aspects of their performance are most (or least) resource intensive. It also allows you to export the results to a json format with further details that you can analyze.

Here you'll find:
- A [sample json file](performanceAnalyzerExport.schema.json) that is an export from the Performance Analyzer
- A [sample pbix file](PerformanceAnalyzerExportReport.pbix) that can be used to analyze the output from the Performance Analyzer
- A [Word doc](Power%20BI%20Performance%20Analyzer%20Export%20File%20Format.docx) that describes the way visuals query data and render on screen, and the way the Performance Analyzer records the events of the visual lifecycle.
