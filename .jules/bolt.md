## 2024-11-11 - [Avoid .bind(this) in requestAnimationFrame]
**Learning:** Calling `.bind(this)` inside `requestAnimationFrame` creates a new function object 60 times a second, leading to unnecessary memory allocation and garbage collection pauses that can cause frame drops.
**Action:** Bind the function once in the constructor and reuse the bound reference in the animation loop.
