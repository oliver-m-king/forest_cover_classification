<center><h1>Oliver King - Forest Cover Classification</h1></center>
<center><img src="https://raw.githubusercontent.com/oliver-m-king/forest_cover_classification/main/tree_image.png" alt="Image by Freepik" width="500" height="300"></center>

The purpose of this project is to develop a machine learning model that can accurately predict the species of tree making up the forest cover of a plot of land based on observations of its elevation; slope; aspect; distances to water features, roads, and firepoints; hillshade; and soil composition.

Five Jupyter notebooks are presented, covering the following stages of analysis:<br>
<pre>
<b>Stage 1</b>         Data Exploration<br>
<b>Stage 2</b>         Data Extraction, Transformation, and Loading<br>
<b>Stage 3</b>         Feature Engineering<br>
<b>Stages 4 and 5</b>  Model Defintion and Training<br>
<b>Stage 6</b>         Model Evaluation<br>
</pre>

Outputs of the notebooks can be found <a href="https://1drv.ms/u/s!ArLx8iGvui0agV8AQZFH-4dXY_q2?e=OLfu7e">here.</a>

<h3>The dataset</h3>

This dataset contains observations of a selection of geographic data on 30 x 30 meter cells located in the Roosevelt National Forest of northern Colorado.<br>
There are 581,012 observations of 12 independent variables.<br>
The aim of this project is to develop a model that can accurately predict what type of forest cover a 30m x 30m cell in any area <i>similar</i> to the Roosevelt National Forest has, based on measurements of it's elevation; aspect; distance to water, roads and firepoints; hillshade; and soil type.

Independent variables were derived from data originally obtained from US Geological Survey (USGS) and USFS data.

<table>
    <tr>
        <th>Feature</th>
        <th>Type</th>
        <th>Measurement</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>Elevation</td>
        <td>Quantitative</td>
        <td>Meters</td>
        <td>Elevation in meters</td>
    </tr>
    <tr>
        <td>Aspect</td>
        <td>Quantitative</td>
        <td>Azimuth</td>
        <td>Aspect in degrees azimuth</td>
    </tr>
    <tr>
        <td>Slope</td>
        <td>Quantitative</td>
        <td>Degrees</td>
        <td>Slope in degrees</td>
    </tr>
    <tr>
        <td>Horizontal Distance To Hydrology</td>
        <td>Quantitative</td>
        <td>Meters</td>
        <td>Horizontal distance to nearest surface water features</td>
    </tr>
    <tr>
        <td>Vertical Distance To Hydrology</td>
        <td>Quantitative</td>
        <td>Meters</td>
        <td>Vertical distance to nearest surface water features</td>
    </tr>
    <tr>
        <td>Horizontal Distance To Roadway</td>
        <td>Quantitative</td>
        <td>Meters</td>
        <td>Horizontal distance to nearest roadway</td>
    </tr>
    <tr>
        <td>Hillshade 9am</td>
        <td>Quantitative</td>
        <td>ArcGIS index, 0 to 255</td>
        <td>Hillshade index at 9am, summer solstice</td>
    </tr>
    <tr>
        <td>Hillshade Noon</td>
        <td>Quantitative</td>
        <td>ArcGIS index, 0 to 255</td>
        <td>Hillshade index at noon, summer solstice</td>
    </tr>
    <tr>
        <td>Hillshade 3pm</td>
        <td>Quantitative</td>
        <td>ArcGIS index, 0 to 255</td>
        <td>Hillshade index at 3pm, summer solstice</td>
    </tr>
    <tr>
        <td>Horizontal Distance To Fire Points</td>
        <td>Quantitative</td>
        <td>Meters</td>
        <td>Horizontal distance to nearest wildfire ignition points</td>
    </tr>
    <tr>
        <td>Wilderness Area<sup>1</sup></td>
        <td>Qualitative</td>
        <td>Boolean (4 one-hot columns)</td>
        <td>Wilderness area designation</td>
    </tr>
    <tr>
        <td>Soil Type<sup>2</sup></td>
        <td>Qualitative</td>
        <td>Boolean (40 one-hot columns)</td>
        <td>Soil type designation</td>
    </tr>
    <tr>
        <td>Cover Type<sup>3</sup></td>
        <td>Qualitative</td>
        <td>Integer, bewteen 1 and 7</td>
        <td>Forest cover type designation</td>
    </tr>
</table>

<b><sup>1</sup></b> The set includes data from four wilderness areas located in the Roosevelt National Forest of northern Colorado.  These areas represent forests with minimal human-caused disturbances, so that existing forest cover types are more a result of ecological processes rather than forest management practices.<br>
1. Rawah Wilderness Area
2. Neota Wilderness Area
3. Comanche Peak Wilderness Area
4. Cache la Poudre Wilderness Area
    
<b><sup>2</sup></b> The soil type is based on a USFS Ecological survey, and there are 40 distinct values.

<b><sup>3</sup></b> There are 7 distinct values for the cover type, each of which contains information on which tree species makes up the bulk of the forest cover for the area.
1. Spruce/Fir
2. Lodgepole Pine
3. Ponderosa Pine
4. Cottonwood/Willow
5. Aspen
6. Douglas-fir
7. Krummholz

The dataset was sourced from the <a href="https://archive.ics.uci.edu/ml/datasets/Covertype">Center for Machine Learning and Intelligent Systems, University of California Irvine</a><br>

<i>Image by Freepik</i>
