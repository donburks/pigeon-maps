# Pigeon Maps - ReactJS maps without external dependencies

![Demonstration](https://github.com/mariusandra/pigeon-maps/blob/master/demonstration.gif?raw=true)

Demo: https://mariusandra.github.io/pigeon-maps/ (using maps from Wikimedia)

## What is it?

Tired of waiting 5 seconds to include 200kb of gzipped Google Maps JavaScript code just to display a few tiles and a marker?

Welcome to the club!

This project aims to provide a performance-first React-centric customizable map engine.

We're currently at:
- [14KB minified](https://raw.githubusercontent.com/mariusandra/pigeon-maps/master/static/demo.bundle.js)
- 4KB gzipped

Implemented:

- Show tiles
- Arbitrary overlays (markers, etc)
- Move the map by dragging
- Move the map by touch on mobile
- Zooming with the scroll wheel
- Zooming by touch
- Smooth / fractional zooming
- Zoom without flickering (keep old tiles until new ones load)

Missing:

- Map attributions
- Event handling (clicks, etc)
- Better wheel zoom handling
- Slide animation when dragging and letting go

## Code

```js
import Map, { Overlay } from 'pigeon-maps'

<Map center={[50.879, 4.6997]} zoom={12} width={600} height={400}>
  <Overlay position={[50.879, 4.6997]} offset={[15, 31]}>
    <img src='pin-green-large@2x.png' width={29} height={34} alt='' />
  </Overlay>
</Map>
```
