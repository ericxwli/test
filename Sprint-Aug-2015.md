## Sprint of Aug 2015

Focus was on functional and performance improvements to layout.
Major highlights below.

### Optimising the analysis of CSS rules
* Modify jstyleparser to accept per-element rules. See https://github.com/radkovo/jStyleParser/pull/35
* Create a per document analyser, instead of per element analyser. The top level analyser creates the rule holder (which sets up rules in an ordered list). This holder can then be reused per element.

The above changes drastically improve layouting speed (about 5x).

### Proper support for `position:relative`

* Disabled caching of layouts, because it interferes with the bubbling up of floats. Floats bubble up in complicated ways:
  * For xy-plane, they continue bubbling up until the criteria defined in `isFloatLimit` are met.
  * For z-axis, they stop bubbling up when `position:relative` is encountered (apart from the above criteria).
