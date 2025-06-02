**June 2, 2025**

Hi Federico, Nitesh,

Here’s my update for today:

- Implemented the logic for handling overlapping clusters in [netjsongraph.js#349](https://github.com/openwisp/netjsongraph.js/pull/349):
  - Calculated pixel-based offsets for clusters sharing the same position.
  - Positioned clusters in a circular layout using angle-based separation.
  - Converted adjusted pixel positions back to geographical coordinates with Leaflet’s `containerPointToLatLng`.
  - Introduced a configurable `clusterSeparation` option (default: 20px), and demonstrated its use in `netjson-clustering.html` with a 15px override.

- This ensures that clusters of different categories at the same location are rendered separately and clearly.

### Tomorrow:
- I plan to review the full set of changes in [PR #349](https://github.com/openwisp/netjsongraph.js/pull/349), refine the logic, and thoroughly test it in the context of [PR #668](https://github.com/openwisp/openwisp-monitoring/pull/668).
