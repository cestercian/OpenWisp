**May 28, 2025**

Hi Federico, Nitesh,

Here’s my update for today:

- **CSS PR – Full Refactor Summary**  
  [netjsongraph.js#374](https://github.com/openwisp/netjsongraph.js/pull/374)

  • **Namespacing**  
    – All global CSS/JS selectors have been converted to `.njg-container` and `.njg-*` classes to prevent conflicts.  
    – Old IDs like `graphChartContainer`, `loadingContainer`, and `closeButton` were replaced with classes; `graphChartContainer` was restored later for compatibility.

  • **Code Updates**  
    – JavaScript modules (`core.js`, `util.js`, `gui.js`) now create and query the new class names.  
    – Tests were updated to reflect the new DOM structure.  
    – Added fallback sizing logic when the library is mounted directly on `document.body`.

  • **CSS Cleanup**  
    – Every rule is now scoped under `.njg-container`.  
    – Removed duplicate blocks and scoped icon rules (e.g., `.iconfont`, `.icon-eye`).

  • **Docs**  
    – Updated `README` to mention `.njg-container`.

  **Result:** The library’s styles and DOM are now fully self-contained, avoiding conflicts with host pages while preserving all functionality.

- **Cluster PR Work**  
  [netjsongraph.js#349](https://github.com/openwisp/netjsongraph.js/pull/349)  
  Continued exploring and testing different approaches. I'm currently working on a logic where clusters repel each other when they get too close. I’ll implement and update you on the progress soon.

## Plan for Tomorrow

- Final refinements and review for [PR #374](https://github.com/openwisp/netjsongraph.js/pull/374) if needed

- Continue developing and testing the cluster repelling logic for [PR #349](https://github.com/openwisp/netjsongraph.js/pull/349)
