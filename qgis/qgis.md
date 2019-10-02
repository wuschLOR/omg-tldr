## QGIS
Linux packages are available ``` sudo apt install qgis ```

### gather data 

http://hgis.cartomatic.pl/post/hgis-wms-w-qgis


### basic usage

language change -> settings -> general

![language selection](qgis_img/language.PNG)

new project (don't forget to save)
first data OSM

![OSM DATA](qgis_img/osm.PNG)

add world map by writing world to the coordinate field at the bottom

![two layers](qgis_img/multilayer.PNG)

play around with the transparency ot the world map by double kicking the layer 

![transparency](qgis_img/transparency.PNG)

change the CRS -> project-> properties -> CRS

![CRS change](qgis_img/changing_the_reference_system.PNG)

* important to note here is to use the appropriate spheroid (here 3857 WGS 84)
* if everything fails use gis.stackoverflow.com


### import data 

TODO read WMS wiki

!https://www.geoportal.gov.pl/uslugi/usluga-przegladania-wms

!http://mapy.geoportal.gov.pl/wss/service/img/guest/ORTO/MapServer/WMSServer

get data link 

![data source manager](qgis_img/data_source_manager.PNG)

![import data source](qgis_img/orto_pl.PNG) 

![working connection](qgis_img/data_source_manager_running_connection.PNG)


highlight -> add -> close -> wait

-> not working change tactics

!https://www.geoportal.gov.pl/uslugi/usluga-przegladania-wmts
!http://mapy.geoportal.gov.pl/wss/service/WMTS/guest/wmts/ORTO

![data source manager](qgis_img/data_source_manager.PNG)

![import data source](qgis_img/orto_pl.PNG) 

![error yay](qgis_img/wmts_error.png)


change 

```
http://mapy.geoportal.gov.pl/wss/service/WMTS/guest/wmts/ORTO?SERVICE=WMS&REQUEST=GetCapabilities
```

to

```
http://mapy.geoportal.gov.pl/wss/service/WMTS/guest/wmts/ORTO?SERVICE=WMTS&REQUEST=GetCapabilities
```

because the service was changed and the error is misleading

if everything is working

![wmts selection](qgis_img/wmts.png)

highlight -> add -> close -> wait

![wmts working](qgis_img/wmts_working.png)



repeat with heigth data
* http://mapy.geoportal.gov.pl/wss/service/WMTS/guest/wmts/ISOK_CIEN

repeat historical German maps but this time check the ignore button for get map capabilities


* http://hgis.cartomatic.pl/page/services
* http://hgis.cartomatic.pl/?tag=/qgis
* http://wms.hgis.cartomatic.pl/topo/2180/m25k?service=WMS&request=GetCapabilities


### bayern services

* https://geoportal.bayern.de/geoportalbayern/seiten/dienste


### thueringen

* use [Geoproxy Freistaat](https://www.geoportal-th.de/Portals/0/Downloads/Geoproxy/Allgemeine%20Beschreibung%20der%20frei%20verf%C3%BCgbaren%20Dienste_WMS_opendata_Geobasisdaten-TLBG.pdf) Thüringen pdf document for further documentation
* http://www.geoproxy.geoportal-th.de/geoproxy/services
* add 1679 DTM and 2032


### multilayermagic

add layer styling toolbox

![layer styling toolbox](qgis_img/layermodification.png)

check for transparency settings set them to no transparency, check the colorize checkbox and select a nice color

![different color and normal mixing](qgis_img/layermodification_color_normal.PNG) 

to make the two layers interact with each other and actualy be usefull change blending mode from **normal** to **multiply**

![different color and multipication mixing](qgis_img/layermodification_color_multiplication.PNG)


remember some layers only are displayed at certain scales

![scale not ok](qgis_img/scaling_too_big.png)

![scale ok](qgis_img/scaling_ok.png)


### download heigthdata for specific places

* https://www.geoportal-th.de/de-de/
* https://www.geoportal-th.de/de-de/Downloadbereiche/Download-Offene-Geodaten-Th%C3%BCringen/Download-H%C3%B6hendaten

find location you wannt e.g. buchenwald and download the corresponding data

![data selection grid](qgis_img/th_multiselection_grid.PNG)

![data bulk download](qgis_img/th_multiselection.PNG)
