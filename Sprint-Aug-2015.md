## Sprint of Aug 2015

Focus was on functional and performance improvements to layout.
Major highlights below.

### Optimising the analysis of CSS rules

### Proper support for `position:relative`

* Disabled caching of layouts, because it interferes with the bubbling up of floats. Floats bubble up in complicated ways:
  * For xy-plane, they continue bubbling up until the criteria defined in `isFloatLimit` are met.
  * For z-axis, they stop bubbling up when `position:relative` is encountered (apart from the above criteria).
