The Request Manager is one of the central features of `gngr`. It is inspired by an extension called [uMatrix](https://github.com/gorhill/uMatrix), which allows the user to control what features are allowed for a website, with a very fine level of granularity. While `uMatrix` is an add-on, the `Request Manager` in `gngr` is a core feature built into the browser engine.

Currently, the features controlled by the Request Manager are:
* Cookies
* CSS
* Images
* Javascript
* XHR (XML HTTP Request)
* Frames
* Referrer Header

### Why
The request manager exists because the above features offer avenues for attacking / tracking the client. Cookies, Javascript, XHR are the most potent and are hence disabled by default for all websites. (The default can be changed easily as will be described below).

### User Interface
The Request Manager can be viewed by clicking the button on the right-top of the browser frame, labelled `Req Mgr`. The keyboard shortcut is `Alt-R`.

Here is a screenshot of the Request Manager when browsing `gngr`'s homepage:
![Request Manager Screenshot](https://gngr.info/media/img/screens/v03.10/reqMgr.png)
