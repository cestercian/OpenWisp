**June 19, 2025**

Hi Federico, Nitesh,

Here’s my update for today:

- Enabled clustering in `device-map.js`, but the overlap prevention logic initially didn’t behave as expected.
- Investigated the issue and found that the configuration used `clusteringAttribute: "status"`, whereas the library logic expects a `category` field.
- Temporarily set `clusteringAttribute: "category"` and injected `feature.category = status` within `onEachFeature` to test the separation logic — which allowed the library to apply the correct offset logic but caused all clusters to render with the same grey color.
- Tried alternate strategies:
  - Defined a custom cluster creation function to use `status` directly — no change in result.
  - Modified the library itself to use `node.status` instead of `node.category` — the library logic worked as intended in isolation, but the behavior still didn’t reflect correctly in OpenWISP Monitoring.

Based on this, I concluded that the core cluster overlap prevention logic in the library is functioning correctly, and the issue lies in how data is passed or configured in OpenWISP Monitoring.

---

**Plan for Tomorrow:**

- Dive deeper into `device-map.js` to ensure that data is being passed in the format expected by the clustering logic (especially around the `status` attribute).
- Review how styling and icon classes are derived in Monitoring and confirm if there are any conflicts caused by changing `clusteringAttribute`.

Let me know if you have thoughts on where else I should investigate or if you'd suggest a different integration approach.

Regards,  
Yash
