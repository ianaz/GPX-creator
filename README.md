# gpx-creator
Javascript/NodeJS GPX 1.1 generator by code. Open for changes


### Usage
```
let GPXService = require('../GpxService').GPXService;
GPXService = new GPXService();
GPXService.setAuthor("Silvio Rainoldi");
GPXService.addPoint({
    lat: 40.5923423420,
    lon: 10.8923342,
    date: new Date(),
    elevation: 560
});
let output = GPXService.toXML();
```


Will output something like this

```
<?xml version="1.0"?>
<gpx
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns="http://www.topografix.com/GPX/1/1"
    xsi:schemaLocation="http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd"
    version="1.1"
    creator="Silvio Rainoldi" ><metadata>
    <name></name>
    <author><name>Silvio Rainoldi</name></author>
    <time>2016-12-05T20:25:59.448Z</time>
</metadata><trk>
    <name></name>
    <cmt></cmt>
    <desc></desc>
    <src></src>
<trkseg>
<trkpt lat="40.592342342" lon="10.8923342">
    <ele>560</ele>
    <time>2016-12-05T20:25:59.448Z</time>
</trkpt>
</trkset>
</trk>
</gpx>
```