# Feature / Result Viewer

The Feature / Result Viewer tool allows the developer of a data analytics service to have a visual overview of the results of an analysis, using familiar visualization methods.

## Building the source

To build the source code, clone this repository and run:

```
gulp build
```

To be able to run the tool, you need to copy the files to the `htdocs` directory of an Apache web server (in the root directory).

## Using the tool

The tool is implemented as a web interface. To run it, visit `http://localhost` from a web browser.

The tool allows the user to load data either from a local file (CSV or JSON) assumed to contain the results of an analysis, or by submitting a query to the AIOTES Data Lake. Any data in the form of an array of JSON records can be used as the input.

The loaded data are presented in a table view for the user to inspect. After data loading, the user is allowed to select between two visualization options: scatterplot and line plot. Selecting one of the visualizations reveals options for specifying which data attributes to use for the visualization attributes of each type of chart, such as x-axis, y-axis and point color. Once these options are specified, the user can click on the "Run" button to view the produced visualization in a separate panel.
