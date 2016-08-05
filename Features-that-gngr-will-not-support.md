## Never ever
* [WPAD](https://en.wikipedia.org/wiki/Web_Proxy_Autodiscovery_Protocol) (4)
* [Battery Status API](https://www.w3.org/TR/battery-status/) (1) & (2)
* [Hyper-link auditing](https://html.spec.whatwg.org/multipage/semantics.html#hyperlink-auditing)
* Geo Location
* Any Camera or Mic APIs
* Resource timing APIs. (5)

## Needs more thought
These features are good to have sometimes, but have fingerprinting potential. They should surely be opt-in though.
* WebGL
* WebRTC
* Canvas
* KeyboardEvent.code (can be misused for fingerprinting keyboard).


## References
1. http://blog.add0n.com/2016/03/23/html5-apis-fingerprint-users-how-to-prevent.html
2. https://blog.lukaszolejnik.com/battery-status-readout-as-a-privacy-risk/
3. https://www.browserleaks.com/
4. https://news.ycombinator.com/item?id=12167209
5. https://github.com/w3c/resource-timing/issues/64
6. https://www.chromium.org/Home/chromium-security/client-identification-mechanisms