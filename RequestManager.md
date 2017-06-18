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

Note that the exact policies of which features to enable / disable by default, and which additional features to present in the Request manager will change over a period of time. At the moment, the important takeaway is that the mechanism exists, and the user can control it.

### User Interface
The Request Manager can be viewed by clicking the button on the right-top of the browser frame, labelled `Req Mgr`. The keyboard shortcut is `Alt-R`.

Here is a screenshot of the Request Manager when browsing `gngr`'s homepage:
![Request Manager Screenshot](https://gngr.info/media/img/screens/v0.3.13-dev/reqManager.png)

In the above screenshot, you can notice that:
* There are no external CSS requests (there may be embedded stylesheets however).
* There are 13 Images.
* There are no Javascript requests.

All the above requests are on the `gngr.info` domain. A background color of `red` means that a request of that type has been denied, while `green` means it has been allowed.

The user can click a cell to enable or disable that particular request.

The row and column headers can also be clicked to enable/disable all entries in that row / column.

To change the defaults, you need to view the `*` scope and make changes there.