## 2024-10-24 - [Avoid Redundant String Allocations in Render Loop]
**Learning:** Found string concatenation and DOM style updates running every frame (60fps) for the CSS 3D UI, even when the camera wasn't moving. This is a common performance bottleneck in WebGL + DOM syncing apps.
**Action:** Implemented caching for the CSS transform string by adding a `hasChanged()` method to the Camera. This avoids ~60 string allocations and DOM style repaints per second and prevents GC stutter.
