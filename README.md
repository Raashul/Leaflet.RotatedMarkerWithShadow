Leaflet Rotated Marker with Rotated Shadow (Based on bbecquet/Leaflet.RotatedMarker)
===

Enables rotation of marker icons in Leaflet, and also rotation of marker shadow icons.

Compatible with versions 0.7.* and 1.* of Leaflet. Doesn't work on IE < 9.

```bash
npm install leaflet-rotatedmarker-with-shadow
```
```bash
bower install leaflet-rotatedmarker-with-shadow
```

Usage
---

```js
L.marker([48.8631169, 2.3708919], {
    rotationAngle: 45, rotationOrigin: 'center center', rotationShadowOrigin: 'left center'
}).addTo(map);
```

API
---

It simply extends the `L.Marker` class with three new options:

Option | Type | Default | Description  
-------|------|---------|------------
**`rotationAngle`** | `Number` | 0 | Rotation angle, in degrees, clockwise.
**`rotationOrigin`** | `String` | `'bottom center'` | The rotation center, as a [`transform-origin`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin) CSS rule.
**`rotationShadowOrigin`** | `String` | `'bottom center'` | The rotation center, as a [`transform-origin`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin) CSS rule.

and three new methods:

Method | Returns | Description
-------|---------|------------
**`setRotationAngle(newAngle)`** | `this` | Sets the rotation angle value.
**`setRotationOrigin(newOrigin)`** | `this` | Sets the rotation origin value.
**`setRotationShadowOrigin(newOrigin)`** | `this` | Sets the shadow rotation origin value.

The default `rotationOrigin` value will rotate around the bottom center point, corresponding to the "tip" of the marker for most commonly used icons. If your marker icon has no tip, or you want to rotate around its center, use `center center`.

Note
---

It ALSO rotate marker icon shadows, if you added shadow icon to your marker.
