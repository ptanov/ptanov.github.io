---
layout: post
title: Приложения за работа с GPS координати, създаване/споделяне на маршрути (gpx)
tags: tourism routes gps gpx openstreetmap garmin komoot strava software
categories: tourism
---
Различни полезни приложения/команди за работа с GPS/gpx и допълнителен софтуер, който ползвам, когато искам да създам или споделя маршрут

# [Komoot](http://komoot.com)

От доста време търся приложение/сайт, в който да мога да търся/създавам маршрути и най-накрая стигнах до едно, което намирам, че покрива почти всичките изисквания - <http://www.komoot.com>

## Предимства:
 - лесно споделяне на завършен преход с други хора.
 - лесно споделяне на плануван преход с други хора.
 - рутиране - човек може да избере две (или повече) точки и приложението автоматично прави маршрут по познатите от него пътеки ([openstreetmaps]({% post_url 2018-02-03-gps-software %}#openstreet-map)).
 - highlights (точка или сегмент) - хората могат да отбелязват неща, които си заслужават да бъдат посетени. Можеш да използваш тези точки за създаване на маршрут (например, сегмент: <https://www.komoot.com/highlight/276916>, точка: <https://www.komoot.com/highlight/137873>).
 - добавяне на снимки към завършени преходи - те се визуализират върху картата (стига да са с gps координати, например <https://www.komoot.com/tour/20446198/zoom>).
 - сваляне на оригинален gpx файл от нерегистрирани потребители (трябва да се scroll-не надолу в страницата).

## Недостатъци:
 - малка общност в България (малко highlights) :(
 - ако снимките нямат gps координати - не ги синхронизира по време - това може да стане ръчно ([Приложения за работа с GPS координати (gpx)]({% post_url 2018-02-03-gps-software %})).
 - в приложението няма опция за търсене на маршрут, но може да се търси с гугъл (например, търсене за [komoot botev](https://www.google.bg/search?q=komoot+botev)) - за това е важно името на прехода да е подробно.
 - offline работата като цяло е платена, но може да се ползва пълнофункционално безплатно за един регион. Така или иначе обичам да подкрепям стойностните приложения за това си мисля, че нещо ако си струва не е проблем да се плати, а в случая - еднократно.
 - не може да се добавя точка или сегмент към коментар към маршрут и да се ползва като дневник на пътуването (<http://help.komoot.de/forums/213895-ideas/suggestions/20118877--highlight-visible-only-for-a-tour>)

# [Strava](https://www.strava.com/)

Разликата между [komoot](http://komoot.com) и [strava](http://strava.com) (освен всичко друго) е че едното е специализирано в измерването на спортните постижения и мотивацията на спортистта, а другото - към откриването на нови приятни места и маршрути... За това за маршрути ползвам komoot, а за неща свързани с натоварване бих ползвал strava, където можеш да гледаш различните сегменти и да сравняваш представянето си с останалите (например, <https://www.strava.com/segments/13828544?filter=overall>)... Алтернатива на strava е [endomondo](http://endomondo.com). Иначе и тук има възможност за [създаване на маршрут](https://www.strava.com/routes/new) както и разглеждане на [heatmap](https://www.strava.com/heatmap#14.34/23.28999/42.58066/hot/winter) - къде спортуват хората най-често, например: [зимни спортове на Витоша](https://www.strava.com/heatmap#14.34/23.28999/42.58066/hot/winter)

# Други сайтове с маршрути, карти и статистика
 - <http://www.mygpsfiles.com/app/> - визуализиране (и споделяне) на много маршрути (gpx) на една карта
 - <http://www.ibpindex.com/index.php/en/> - определяне на трудност на маршрут
 - <http://www.javawa.nl/analyser.html> - статистика за маршрут
 - <https://www.nicetrails.com/app/> - 3D визуализация на маршрут
 - [FatMap](http://fatmap.com) - много полезна карта, с анализ на склонове във връзка с лавинната безопастност и планирането на маршрут (ориентация, наклон, т.н.). Също така има маршрути с описания, макар и малко
 - <http://www.gpsvisualizer.com/> - import and convert of multiple sources, web gps babel
 - <https://tripsjournal.com/marshruti> - добре подредени и описани маршрути в България
 - [GaiaGPS](https://www.gaiagps.com) - подреждане на маршрути в папки, визуализиране на цяла папка с маршрути върху карта
 - <https://www.gps-tour.info>
 - <http://www.gpsies.com/>
 - <http://en.wikiloc.com/wikiloc/home.do>
 - <http://everytrail.com>
 - <https://tracedetrail.fr> - организиране на състезания

# Други приложения и команди
 - linux app for visualization of tracks + images - [GPS prune](https://wiki.openstreetmap.org/wiki/GpsPrune)
 - сваляне на записани данни от [Holux M-241](https://wiki.openstreetmap.org/wiki/Holux_M-241) `gpsbabel -r -w -t -i m241 -f /dev/ttyUSB0 -o gpx -F track.gpx` (run with sudo if you don't have access to USB ports)
 - добавяне на GPS координати към снимки на базата на часа на снимката и записан маршрут (gpx) `exiftool -geotag *.gpx *.jpg` или `gpscorrelate -g track.gpx  -O -10800 *.jpg`, други [примери с ExifTool]({% post_url 2019-03-20-exiftool %}).
 - обединяване на GPS координати (gpx файл) и пулс (heart rate) от MiBand 3 (csv файл) [сорс код](https://github.com/ptanov/gpxmergeheartrate): `docker run --rm -it -v /etc/timezone:/etc/timezone:ro -v "$(pwd)":/data ptanov/gpxmergeheartrate Day* Ex* out && cp out "out.gpx" && rm -f out`

# Синхронизиране на метаданните на снимки с GPS координати (по време)
 - [примери с ExifTool]({% post_url 2019-03-20-exiftool %})

# Карта на България
 Съществуват няколко подробни карти за България:
 - bgmountains <http://kade.si> <http://bgmountains.org>, безплатна
 - openstreet map <http://openstreetmap.org>, безплатна, лесна за редакция
 - <http://karta.bg>, платена

# Openstreet Map
 Човек лесно може да добавя и редактира тази карта. За да се ползва на Гармин устройство трябва да се "рендерира" за Гармин. Това може да стане "на ръка" или да се свали наготово от сайт и да се качи на устройството. Всеки един сайт прилага различни стилове и филтри към данните от openstreet map и за това те изглеждат по различен начин - за туризъм, за кола и за други.

# Сваляне на карти за Гармин:
 - <http://www.wanderreitkarte.de/garmin_de.php> с цветовете на маркираните пътеки, но на немски
 - bgmountains: <http://bgmountains.org/en/maps/garmin-maps/category/9-bgmountains>

  > Full version for MS Windows, BGMountains 20170706 Cyr direct copy: Full version for direct upload into the receiver BGMountains 20170706 Cyr IMG

 - openstreet map: <https://wiki.openstreetmap.org/wiki/OSM_Map_On_Garmin/Download> - <http://garmin.openstreetmap.nl/>

 > bulgaria without typ
[   ] osm_generic_windows.exe   92M  Map installer for BaseCamp / MapSource on the Windows platform.
http://osm.pleiades.uni-wuppertal.de/garmin/generic/20-08-2017/546c7030f55760a3175a43f6744f6972/
direct copy: [   ] osm_generic_gmapsupp.zip  88M  Compressed file containing a single image that can be placed directly onto the SD-card of the GPS. Unzip first!

 - karta.bg <https://support.karta.bg/?mod=licenses-manual>
 > Посетете www.karta.bg и влезте във Вашия потребителски профил от "Вход" в горния десен ъгъл на екрана. Главен файл, съдържащ картата TOPO LAT GPS

# Как да направим сами Garmin карта от Openstreet maps
TODO - в отделен пост

# Карти за телефон (iPhone/Android)
За iOS и Андроид има много приятно приложение за карти - [MAPS.me](https://maps.me/download/) (освен [komoot](#komoot)), за Андроид има друго приложение с много функционалност, но дървен интерфейс - [oruxmaps](http://www.oruxmaps.com/cs/en/more/downloads) (някой път бих писал по-подробно за него и функционалността му, например как без Интернет да имаш Google satellite images) - кратко описание: <http://planinar.org/bgmountains-%D0%BA%D0%B0%D1%80%D1%82%D0%B0-%D0%B7%D0%B0-android/>.

# Прогноза за времето
 - [Прогноза за времето]({% post_url 2018-02-04-tourism %}#прогноза-за-времето)
