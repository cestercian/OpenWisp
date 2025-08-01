Here’s your formatted daily update for **August 1, 2025**, based on the changes visible in your screenshots:

---

**August 1, 2025**

Hi Federico Capoano,

Here’s my update for today:

**PR: [#668 – Restore Leaflet Popup Handling in Monitoring](https://github.com/openwisp/openwisp-monitoring/pull/668)**

Today I focused on improving the **device map scale control, bounds handling, and world-wrapping behavior**:

* Refactored the `device-map.js` file to:

  * **Unify and clean up** logic for adding Leaflet's scale control based on config.
  * Restore and **refactor auto-bounding** logic for map features using a temporary layer to calculate bounds without rendering it.
  * Preserve interaction clarity by **bringing point features to the front** above polygons.
  * Enhance error handling when bounds fitting fails.
* Implemented logic to:

  * **Restrict horizontal panning** to three wrapped world widths.
  * Fix **wraparound issues near the dateline** by appending cloned feature sets east/west when crossing ±180° longitude, avoiding visual gaps or bounce-backs.
  * Validate feature presence before applying bounding logic, preventing runtime errors when no features are present.

These changes ensure backward compatibility with older behavior (like that in [issue #462](https://github.com/openwisp/openwisp-monitoring/issues/462)) while fully aligning with the new unified rendering system.

**Plan for Tomorrow**

* Conduct final review and cleanup of the PR.
* Confirm with you if any legacy behavior still needs to be retained.
* Address any final feedback and prep for merge.

Best regards,
**Yash**

---

Let me know if you'd like a version for GitHub comments, Slack, or anything else!
