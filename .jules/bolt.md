## 2025-03-31 - O(n*m) Complexity in React Render Paths
**Learning:** Recomputing complex state or iterating over large arrays inside helper functions called during render (like mapping over a list of rooms and searching a large list of courses for each) causes O(n*m) render bottlenecks. `Intl.DateTimeFormat` is also surprisingly expensive when instantiated multiple times per render.
**Action:** Memoize mappings (like Map or Set) of large collections outside the render loop and use O(1) lookups during render.
