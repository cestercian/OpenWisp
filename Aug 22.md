### August 22, 2025  

Hi Federico Capoano,  

Here is the Summary of today's progress:  

---

#### PR #153 – Display Number of Clients  
[PR #153](https://github.com/openwisp/netjsongraph.js/pull/153)  

- Addressed requested changes from @nemesifier and fixed a related bug.  
- **Graph mode**:  
  - Added `showGraphLabelsAtZoom` to control label visibility by zoom level.  
  - Switched to label formatter to prevent snap-backs.  
  - Introduced stable series IDs (`graph-series`) with series-only updates to maintain zoom continuity.  
- **Map mode**:  
  - Fixed zoom/pan drift using `L.DomUtil.getPosition` in `LeafletView.js`.  
  - Label toggles now target only `id: "map-nodes"`.  
- **Labels**:  
  - Implemented fallback to `node.name` or `String(node.id)` when `node.label` is missing.  
- **Cleanup**:  
  - Removed all debug logs and test hooks.  
  - Updated examples; ESLint/Prettier checks are clean.  
- **Root cause fixed**: Eliminated full `setOption` resets that caused zoom snap-backs. Using formatter + stable series IDs + series-only updates now preserves continuous zoom.  
- **Verification steps**: `showGraphLabelsAtZoom` configurable in `netjsongraph.html`; labels appear smoothly past threshold, no snap-backs.  

---

#### PR #411 – Added Client-Nodes Functionality  
[PR #411](https://github.com/openwisp/netjsongraph.js/pull/411)  

- Worked on expanding client-node support with 11 commits:  
  - **Mesh Data Support**:  
    - Introduced detection & conversion utilities for Mesh-format data → automatic NetJSON transformation.  
    - Enhanced client overlay logic for combined WiFi client counts.  
    - Core/update modules now convert Mesh data upfront for seamless downstream processing.  
  - **Code Updates**:  
    - Updated `netjsongraph.clients.js`.  
    - Expanded `mesh-network-nodes.json` with richer node/client info; removed `onReady` highlight feature.  
    - Refactored client overlay: WiFi client markers now combine counts; node info sidebar recursively renders nested arrays/properties. Labels prefer interface names where available.  
  - **Visualization Improvements**:  
    - Adjusted overlay plugin radius (5 → 6) and gap (5 → 4).  
    - Expanded mesh nodes & clients; updated legend UI.  
    - Refined node spacing & radius calculations for better layout.  
  - **Refactor**: Extracted mesh utilities into new module `netjsongraph.mesh.js` for better maintainability.  
  - **Chores**: Prettier formatting & cleanup.  

---

**Plans for Tomorrow**:  
- For **PR #153**: finalize after confirmation on label rendering & zoom stability.  
- For **PR #411**: address any pending review comments, polish visualization consistency, and prepare documentation/examples.  
