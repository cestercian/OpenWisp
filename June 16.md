**June 16, 2025**

Hi Federico, Nitesh,

Here’s my update for today:

- For [netjsongraph.js#349](https://github.com/openwisp/netjsongraph.js/pull/349):
  - Updated the cluster-click behavior in `netjsongraph.render.js`:
    - Removed the logic that exploded a cluster into child nodes on click.
    - Implemented a new behavior where clicking on a cluster pans the map to the cluster location and zooms in by +2 levels (capped at the max zoom level).
- For [openwisp-monitoring#668](https://github.com/openwisp/openwisp-monitoring/pull/668):
  - Re-updated the minified JS file to reflect the latest changes from NetJSONGraph.
  - Fixed the shrinking map issue by setting the `max-width` of the map container to `100%`.

**Plan for Tomorrow:**
- Begin removing unused logic and redundant code from the NetJSONGraph clustering implementation to improve clarity and maintainability.
- Review any pending feedback on both PRs.
- Use the DB file provided by Federico to test changes locally in OpenWISP Monitoring.

Let me know if you have any suggestions or priorities to focus on.

Regards,  
Yash
