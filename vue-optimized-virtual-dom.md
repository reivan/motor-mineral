I've read [Rendering Mechanism](https://vuejs.org/guide/extras/rendering-mechanism.html) from Vue docs.

Notes:

- Virtual DOM is a pattern that separates UI building with components (delarative) from commiting changes to DOM (imperative).
- Vue adds a complie step to the rendering pipeline (converting `.vue` files into render functions). During this compile step vue adds some optimizations. This helps make reconciliation faster (virtual DOM diffing).
