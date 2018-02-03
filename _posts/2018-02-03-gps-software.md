---
layout: post
title: Приложения за работа с GPS координати (gpx)
tags: tourism routes gps gpx openstreetmap garmin
categories: tourism
---
Различни полезни приложения/команди за работа с GPS/gpx

От години ползвам разни команди/приложения, които накратко ще опиша тук:
 - визуализиране (и споделяне) на много маршрути (gpx) на една карта: http://www.mygpsfiles.com/app/
 - определяне на трудност на маршрут http://www.ibpindex.com/index.php/en/
 - 3D визуализация на маршрут: https://www.nicetrails.com/app/
 - import and convert of multiple sources, web gps babel: http://www.gpsvisualizer.com/
 - linux app for visualization of tracks + images - [GPS prune](https://wiki.openstreetmap.org/wiki/GpsPrune)
 - сваляне на записани данни от [Holux M-241]( https://wiki.openstreetmap.org/wiki/Holux_M-241 )

 `gpsbabel -r -w -t -i m241 -f /dev/ttyUSB0 -o gpx -F track.gpx` (run with sudo if you don't have access to USB ports)
 - добавяне на GPS координати към снимки на базата на часа на снимката и записан маршрут (gpx)

 `exiftool -geotag *.gpx *.jpg`

 или

 `gpscorrelate -g track.gpx  -O -10800 *.jpg`

# Карта на България
 Съществуват няколко подробни карти за България:
 - bgmountains http://kade.si http://bgmountains.org, безплатна
 - openstreet map http://openstreetmap.org, безплатна, лесна за редакция
 - http://karta.bg, платена

# Openstreet Map
 Човек лесно може да добавя и редактира тази карта. За да се ползва на Гармин устройство трябва да се "рендерира" за Гармин. Това може да стане "на ръка" или да се свали наготово от сайт и да се качи на устройството. Всеки един сайт прилага различни стилове и филтри към данните от openstreet map и за това те изглеждат по различен начин - за туризъм, за кола и за други.

# Сваляне на карти за Гармин:
 - http://www.wanderreitkarte.de/garmin_de.php с цветовете на маркираните пътеки, но на немски
 - bgmountains: http://bgmountains.org/en/maps/garmin-maps/category/9-bgmountains

  > Full version for MS Windows, BGMountains 20170706 Cyr direct copy: Full version for direct upload into the receiver BGMountains 20170706 Cyr IMG

 - openstreet map: https://wiki.openstreetmap.org/wiki/OSM_Map_On_Garmin/Download > http://garmin.openstreetmap.nl/

 > bulgaria without typ
[   ] osm_generic_windows.exe   92M  Map installer for BaseCamp / MapSource on the Windows platform.
http://osm.pleiades.uni-wuppertal.de/garmin/generic/20-08-2017/546c7030f55760a3175a43f6744f6972/
direct copy: [   ] osm_generic_gmapsupp.zip  88M  Compressed file containing a single image that can be placed directly onto the SD-card of the GPS. Unzip first!

 - karta.bg https://support.karta.bg/?mod=licenses-manual
 > Посетете www.karta.bg и влезте във Вашия потребителски профил от "Вход" в горния десен ъгъл на екрана. Главен файл, съдържащ картата TOPO LAT GPS

# Как да направим сами Garmin карта от Openstreet maps
TODO - в отделен пост

# Сайтове с маршрути
 - [Създаване/споделяне на маршрути]({% post_url 2018-02-03-routes %}#други-сайтове-с-маршрути)
