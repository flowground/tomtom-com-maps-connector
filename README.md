# ![LOGO](logo.png) Maps **flow**ground Connector

## Description

A generated **flow**ground connector for the Maps API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/tomtom.com/maps/1.0.0/openapi.json<br/>
Generated at: 2019-05-07T17:44:24+03:00

## API Description

The Maps API web services suite offers the following APIs:
  - Raster
  The Maps Raster API renders map data that is divided into gridded sections called tiles. Tiles are square images (png or jpg format) in various sizes which are available at 19 different zoom levels, ranging from 0 to 20. For zoom level 0, the entire earth is displayed on one single tile, while at zoom level 20, the world is divided into 2<sup>40</sup> tiles.
  - Vector
  Similar to Maps Raster API, the Maps Vector API serves data on different zoom level ranging from 0 to 22. For zoom level 0, the entire earth is displayed on one single tile, while at zoom level 22, the world is divided into 2<sup>44</sup> tiles.
  The Maps Vector Service delivers geographic map data packaged in a vector representation of squared sections called vector tiles. Each tile includes pre-defined collections of map features (points, lines, road shapes, water polygons, building footprints, ect.) delivered in one of the specified vector formats. Format of the tile is formally described using protobuf schema.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Copyrights whole world

> The Copyrights API returns copyright information for<br/>
> the Maps API Raster Tile Service in JSON, JSONP, or XML format.<br/>
> This call returns copyright information for the whole world.

*Tags:* `Copyrights`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1
    Possible values: 1.
* `format` - _required_ - Format of the response
    Possible values: json, jsonp, xml.
* `callback` - _optional_ - Specifies the jsonp callback method. Only used when format is jsonp

### Captions

> This API returns copyright captions for the map service.

*Tags:* `Copyrights`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1.
    Possible values: 1.
* `format` - _required_ - Format of the response
    Possible values: json, jsonp, xml.
* `callback` - _optional_ - Specifies the jsonp callback method. Only used when format is jsonp

### Copyrights bounding box

> The Copyrights API returns copyright information for<br/>
> the Maps API Raster Tile Service in JSON, JSONP, or XML format.<br/>
> This call returns copyright information for a specific bounding box.

*Tags:* `Copyrights`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1
    Possible values: 1.
* `format` - _required_ - Format of the response
    Possible values: json, jsonp, xml.
* `minLon` - _required_ - Minimum longitude coordinate of bounding box defined in terms of latitude/longitude.
* `minLat` - _required_ - Minimum latitude coordinate of bounding box defined in terms of latitude/longitude.
* `maxLon` - _required_ - Maximum longitude coordinate of bounding box defined in terms of latitude/longitude.
* `maxLat` - _required_ - Maximum latitude coordinate of bounding box defined in terms of latitude/longitude.
* `callback` - _optional_ - Specifies the jsonp callback method. Only used when format is jsonp.

### Copyrights tile

> The Copyrights API returns copyright information for<br/>
> the Maps API Raster Tile Service in JSON, JSONP, or XML format.<br/>
> This call returns copyright information for the a specific map tile.

*Tags:* `Copyrights`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1
    Possible values: 1.
* `format` - _required_ - Format of the response
    Possible values: json, jsonp, xml.
* `zoom` - _required_ - Zoom level of tile to be rendered. Only used for tile-level
copyright calls.
    Possible values: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18.
* `X` - _required_ - X coordinate of the tile on zoom grid. Only used for tile-level
copyright calls.
* `Y` - _required_ - Y coordinate of the tile on zoom grid. Only used for tile-level
copyright calls.
* `callback` - _optional_ - Specifies the jsonp callback method. Only used when format is jsonp.

### Static Image

> The Static Image service renders a rectangular raster image<br/>
> in the style, size, and zoom level specified. The image can be requested<br/>
> using either a center point plus width and height or a bounding box.

*Tags:* `Raster`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1.
    Possible values: 1.
* `layer` - _optional_ - Layer of image to be rendered. <em>Hybrid</em> and <em>labels</em>
are intended for layering with other data and are only available in <em>png</em> format.
    Possible values: basic, hybrid, labels.
* `style` - _optional_ - Map style to be returned
    Possible values: main, night.
* `format` - _optional_ - Image format to be returned
    Possible values: png, jpg, jpeg.
* `zoom` - _optional_ - Zoom level of map image to be returned.
    Possible values: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22.
* `center` - _optional_ - Coordinates for the center point of the image.
Must be used with the <strong>width</strong> and
<strong>height</strong> parameters; cannot be used with <strong>bbox</strong>.
Uses EPSG:3857 projection (functionally equivalent to EPSG:900910).
* `width` - _optional_ - Width of the resulting image in pixels. Width must be a positive integer between 1 and 8192.
* `height` - _optional_ - Height of the resulting image in pixels. Height must be a positive integer between 1 and 8192.
* `bbox` - _optional_ - Bounding box for the image, using EPSG:3857 projection (functionally equivalent to EPSG:900910).
Values <strong>must</strong> be in the order of minLon, minLat, maxLon, maxLat.
MaxLat must be greater than minLat. Longitude values can be on both sides of the 180th meridian.
Cannot be used with <strong>center</strong>, <strong>width</strong>, or <strong>height</strong> parameters.
* `view` - _optional_ - Geopolitical view. Determines rendering of disputed areas. See the <a href="/maps-api/maps-api-documentation-raster/raster-tile">documentation</a> for an explanation of how this works in live services.
    Possible values: Unified, IN.

### Tile

> The Maps API Vector Service delivers vector tiles, which are representations of square sections of map data.

*Tags:* `Vector`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1
    Possible values: 1.
* `layer` - _required_ - Layer of tile to be rendered
    Possible values: basic, hybrid, labels.
* `style` - _required_ - Style of tile to be rendered
    Possible values: main.
* `zoom` - _required_ - Zoom level of tile to be rendered
    Possible values: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22.
* `X` - _required_ - x coordinate of tile on zoom grid
* `Y` - _required_ - y coordinate of tile on zoom grid
* `view` - _optional_ - Geopolitical view. Determines rendering of disputed areas. See the <a href="/maps-api/maps-api-documentation-vector/tile">documentation</a> for an explanation of how this works in live services.
    Possible values: Unified, IL, IN.
* `language` - _optional_ - Language to be used for labels in the response. The default is NGT: Neutral Ground Truth, which uses each place's local official language and script (where available). See the <a href="/maps-api/maps-api-documentation-vector/tile">documentation</a> for a full list of options.

### Tile

> The Maps API Raster Service delivers raster tiles, which are representations of square sections of map data.

*Tags:* `Raster`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1.
    Possible values: 1.
* `layer` - _required_ - Layer of tile to be rendered. <em>Hybrid</em> and <em>labels</em> are intended for layering with other data and are only available in <em>png</em> format.
    Possible values: basic, hybrid, labels.
* `style` - _required_ - Style of tile to be rendered
    Possible values: main, night.
* `zoom` - _required_ - Zoom level of tile to be rendered
    Possible values: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22.
* `X` - _required_ - x coordinate of tile on zoom grid
* `Y` - _required_ - y coordinate of tile on zoom grid
* `format` - _required_ - Format of the response.
    Possible values: jpg, png.
* `tileSize` - _optional_ - Tile dimensions in pixels. <em>512</em> is only available for the <em>main</em> style and <em>basic</em> or <em>labels</em> layers.
    Possible values: 256, 512.
* `view` - _optional_ - Geopolitical view. Determines rendering of disputed areas. See the <a href="/maps-sdk-web/functional-examples#geopolitical-views">documentation</a> for an explanation of how this works in live services.
    Possible values: Unified, IN.

### GetMap

> The GetMap call implements the Web Map Service 1.1.1 standard<br/>
> to access TomTom raster map tiles. This service is described<br/>
> in the response to the GetCapabilities API call.

*Tags:* `WMS / WMTS`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1
    Possible values: 1.
* `request` - _required_ - Request type
    Possible values: GetMap.
* `srs` - _required_ - Projection used in describing the <b>bbox</b> EPSG:3857 is
recommended, particularly at higher zoom levels. (Note that
EPSG:3857 is functionally equivalent to EPSG:900913/EPSG:3785)
    Possible values: EPSG:3857, EPSG:4326.
* `bbox` - _required_ - Bounding box in the projection stated in <b>srs</b>
(minLon,minLat,maxLon,maxLat)
* `width` - _required_ - Width of the resulting image, in pixels Maximum value is 2048
* `height` - _required_ - Height of the resulting image, in pixels Maximum value is 2048
* `format` - _required_ - Image format to be returned
    Possible values: image/jpeg, image/png.
* `layers` - _required_ - Map layers requested Currently only the basic layer is available
    Possible values: basic.
* `styles` - _optional_ - Map styles to be returned. Currently, no styles are available. This
parameter is present for forward compatibility; it must be used and
left blank.
    Possible values: .
* `service` - _optional_ - Service type
    Possible values: WMS.
* `version` - _required_ - WMS service version
    Possible values: 1.1.1.

### GetCapabilities

> The GetCapabilities call is part of TomTom's implementation of version 1.1.1<br/>
> the Web Map Service (WMS). It provides descriptions of the other calls<br/>
> that are available in the implementation.

*Tags:* `WMS / WMTS`

#### Input Parameters
* `versionNumber` - _required_
    Possible values: 1.
* `service` - _required_
    Possible values: WMS.
* `request` - _required_
    Possible values: GetCapabilities.
* `version` - _optional_ - WMS service version
    Possible values: 1.1.1.

### WMTS

> The WMTS GetCapabilities call implements version 1.0.0 of<br/>
> the <a href="http://www.opengeospatial.org/standards/wmts">Web Map Tile Service</a><br/>
> (WMTS) standard. It returns metadata that allows compatible calling systems to construct<br/>
> calls to TomTom's raster map tile service. See the<br/>
> <a href="/maps-api/maps-api-documentation-raster/wmts">documentation</a><br/>
> for more information on WMTS.

*Tags:* `WMS / WMTS`

#### Input Parameters
* `versionNumber` - _required_ - Version of the service to call. The current version is 1
    Possible values: 1.
* `key` - _required_ - Your API key for calling this service.
* `wmtsVersion` - _required_
    Possible values: 1.0.0.

## License

**flow**ground :- Telekom iPaaS / tomtom-com-maps-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
