
**Hey Federico Capoano,**

Here's my daily report summary for **Sept 8**

**PR [#419](https://github.com/openwisp/netjsongraph.js/pull/419)**

* Updated render logic and config:

  * `showGraphLabelsAtZoom` default disabled; README updated.
  * Implemented conditional graphRoam: reacts only to zoom, triggers resize on threshold crossing.
  * Renamed series IDs: `graph-series → network-graph`, `map-nodes → geo-map`.
* Updated tests to match new IDs and conditional roam behavior; all tests pass.

**PR [#441](https://github.com/openwisp/netjsongraph.js/pull/441)**

* Updated README structure:

  * Reorganized “Live Examples” to prioritize engaging examples.
  * Moved “Multiple links render” up, “Multiple interfaces” and “Date parse” to the end.
  * Replaced verbose “Configuration instructions” with concise “API reference.”
  * Normalized wording (“demo”→“example”) and simplified “Contributing.”
* Fixed broken examples:

  * Multiple tiles example now uses ArcGIS World Imagery.
  * Multiple interfaces example loads correctly from `dist/` in graph mode.
* Proposed re-recording `netjsonmap-multipleTiles.gif`.

**Plan for Tomorrow**

* Continue refining graphRoam behavior and zoom threshold handling for PR [#419](https://github.com/openwisp/netjsongraph.js/pull/419).
* Complete audit of map examples and finalize GIF updates for PR [#441](https://github.com/openwisp/netjsongraph.js/pull/441).
* Address any pending review comments on PRs [#419](https://github.com/openwisp/netjsongraph.js/pull/419) and [#441](https://github.com/openwisp/netjsongraph.js/pull/441).

Best Regards,
Yash
