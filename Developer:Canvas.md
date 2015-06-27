## Implementation Notes

### TODO
* Function that add a curved subpath to the current drawing path (for example: context.arc()) need to be transformed by the current transformation matrix. Right now, only the points are being transformed, and not radius, etc.
* globalCompositeOperation = lighter and copy don't have a direct equivalent in Swing Graphics. Needs custom implementation. Java implementation is different from the HTMLcanvas implementation.
* Following APIs are yet to be implemented:
  * Config APIs
    * font
    * textAlign
    * textBaseline
    * measureText
    * createRadialGradient
    * createPattern
    * shadowOffsetX
    * shadowOffsetY
    * shadowBlur
    * shadowColor
    
  * Draw APIs
    * drawFocusIfNeeded
    * strokeText
    * drawImage

  * Interaction and Animation
    * isPointInPath
    * addHitRegion
    * removeHitRegion
    * clearHitRegion 
 
