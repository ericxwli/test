## Implementation Notes

### TODO
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
 
## Tests
Apart from the w3c tests, here are some more:
* [Philip's canvas tests](https://philip.html5.org/tests/canvas/suite/tests/)

## Security considerations
* Reading from a canvas could be a special permission, since it apparently enables fingerprinting. (Needs study).