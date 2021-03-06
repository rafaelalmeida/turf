# @turf/rewind

# rewind

Rewind [(Mutli)LineString](http://geojson.org/geojson-spec.html#linestring) or [(Multi)Polygon](http://geojson.org/geojson-spec.html#polygon) outer ring clockwise and inner rings counterclockwise (Uses [Shoelace Formula](http://en.wikipedia.org/wiki/Shoelace_formula)).

**Parameters**

-   `geojson` **[Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;([Polygon](http://geojson.org/geojson-spec.html#polygon) \| [MultiPolygon](http://geojson.org/geojson-spec.html#multipolygon) \| [LineString](http://geojson.org/geojson-spec.html#linestring) \| [MultiLineString](http://geojson.org/geojson-spec.html#multilinestring))>** input GeoJSON Polygon
-   `reverse` **\[[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)]** enable reverse winding (optional, default `false`)
-   `mutate` **\[[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)]** allows GeoJSON input to be mutated (significant performance increase if true) (optional, default `false`)

**Examples**

```javascript
var polygon = {
    "type": "Feature",
    "properties": {},
    "geometry": {
        "type": "Polygon",
        "coordinates": [
            [[121, -29], [138, -29], [138, -18], [121, -18], [121, -29]]
        ]
    }
};
var rewind = turf.rewind(polygon);

//addToMap
var addToMap = [rewind];
```

Returns **[Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;([Polygon](http://geojson.org/geojson-spec.html#polygon) \| [MultiPolygon](http://geojson.org/geojson-spec.html#multipolygon) \| [LineString](http://geojson.org/geojson-spec.html#linestring) \| [MultiLineString](http://geojson.org/geojson-spec.html#multilinestring))>** rewind Polygon

# rewindLineString

Rewind LineString - outer ring clockwise

**Parameters**

-   `coords` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)>>** GeoJSON LineString geometry coordinates
-   `reverse` **\[[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)]** enable reverse winding (optional, default `false`)

Returns **void** mutates coordinates

# rewindPolygon

Rewind Polygon - outer ring clockwise and inner rings counterclockwise.

**Parameters**

-   `coords` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)>>>** GeoJSON Polygon geometry coordinates
-   `reverse` **\[[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)]** enable reverse winding (optional, default `false`)

Returns **void** mutates coordinates

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/rewind
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
