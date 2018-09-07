# Edit your Location (and optionally reproject into different coordinate system)
A MoreApp Widget to retrieve the GPS location and edit it afterwards. The version 0.0.2 introduced the possibility to transform the coordinates into a desired coordinate system.

### How to enable the reprojection
#### 1. You have to obtain a PROJ4 Definition string
This string defines how to perform the projection. Currently hundreds of coordinate systems are supported.

##### Method #1: Online on EPSG.io
 To find your desired projection definiton you can e.g. go to https://epsg.io and search for the target coordinate system you want to reproject your location data into. Then scroll down to the **Export** Section and select the **PROJ4** tab. Then copy the string.

This is an example of how a PROJ4 Definition String for the UTM Zone 32N looks like:

 ```
 +proj=utm +zone=32 +ellps=GRS80 +towgs84=0,0,0,0,0,0,0 +units=m +no_defs
 ```
 
 And the whole as a GIF Animation:
 
![GIF Animation of getting the PROJ4 Definition from EPSG.io](./get-proj4-definition.gif)

##### Method #2: Getting the definition string with QGIS

![GIF Animation of getting the PROJ4 Definition with QGIS](./get-proj4-def-with-qgis.gif)

#### 2. Paste your proj4 definition into your moreapp widget
You set the projection coordinate system by pasting the proj4 definition file into the widget. To do so you have to open the `property panel` by clicking the pencil/edit symbol when hovering over your widget. Then paste your copied string into the `PROJ4 Definition String` Section.

![GIF Animation of getting the PROJ4 Definition with QGIS](./get-proj4-def-with-qgis.gif)


