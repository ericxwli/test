## Implementation Notes

### TODO
* Function that add a curved subpath to the current drawing path (for example: context.arc()) need to be transformed by the current transformation matrix. Right now, only the points are being transformed, and not radius, etc.
* globalCompositeOperation = lighter doesn't have a direct equivalent in Swing Graphics. Needs custom implementation.
