# Feature / Result Viewer

The Feature / Result Viewer tool allows the developer of a data analytics service to have a visual overview of the results of an analysis, using familiar visualization methods.

## Building and Deployment from source

To build the source code, clone this repository and change the directory to it. If you haven't gulp installed, run

```
npm install --global gulp
```

Then to run from source, run:
```
gulp build
```

To be able to run the tool, you need to copy the files to the `htdocs` directory of an Apache web server (in the root directory).

## Docker deployment

To run the Feature / Result Viewer tool, run the following:

```
docker run -p 8087:80 docker-activage.satrd.es/feature-result-viewer:1.0
```
You can change the port from 8087 to any other port, by changing it in the commands above.

## Using the tool

The tool is implemented as a web interface. To run it, visit `http://localhost` from a web browser. If you've deployed through docker following the instructions above, visit [`http://localhost:8087`](http://localhost:8087/).

The tool allows the user to load data either from a local file (CSV or JSON) assumed to contain the results of an analysis, or by submitting a query to the AIOTES Data Lake. Any data in the form of an array of JSON records can be used as the input.

The loaded data are presented in a table view for the user to inspect. After data loading, the user is allowed to select between two visualization options: scatterplot and line plot. Selecting one of the visualizations reveals options for specifying which data attributes to use for the visualization attributes of each type of chart, such as x-axis, y-axis and point color. Once these options are specified, the user can click on the "Run" button to view the produced visualization in a separate panel.

## LICENSE

Copyright 2020 CERTH/ITI Visual Analytics Lab. This software is licensed under EUPL v1.2, check [LICENSE](./LICENSE) for more.