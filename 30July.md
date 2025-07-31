**July 30, 2025**

Hi Federico Capoano,

Here’s my update for today:

**PR: [#668 – Prevent Clustering Overlap ](https://github.com/openwisp/openwisp-monitoring/pull/668)**

Today I focused on restoring the expected popup behavior in OpenWISP Monitoring and improving the overall map interaction experience:

- Replaced outdated Leaflet-based event bindings with the new `netjsongraphInstance.layer and onclick()` handler to align with the unified rendering pipeline.
- Introduced a **custom tooltip formatter** in the ECharts options to improve the visibility of node metadata (showing node name, label, or ID depending on availability).
- Verified that the issue with `loadPopUpContent` exists even with only the Uniform GeoJSON changes, confirming it stemmed from the event handling logic.
- Restored the original Leaflet popup behavior to ensure compatibility with Deepanshu’s work, which extends that functionality.
- Rebased the clustering PR to `master` after merging of the [#396 – Uniform GeoJSON PR](https://github.com/openwisp/netjsongraph.js/pull/396).

**Collaboration**

- Met with **Deepanshu** to:
    - Align on how **unifying the map rendering pipeline** improves maintainability and affects other dependent parts of the project and updated Deepanshu with the latest changes regarding the `loadpopup` function.
    - Finalize that only **node names** should be displayed in the popups.
    - Refactor my changes for better clarity and remove unnecessary code.

**Plan for Tomorrow**

- Complete final testing of the restored popup behavior.
- Push any remaining changes and request review.
- Check in with Deepanshu to confirm that no regressions affect his work.

Best regards,
**Yash**
