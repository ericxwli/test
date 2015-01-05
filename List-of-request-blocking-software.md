|Name|Used with|Switchboard|Active as of Q1 2015|
|----|---------|-----------|--------------------|
|[uMatrix](https://github.com/gorhill/uMatrix)|Chromium|✔|✔|
|[uBlock](https://github.com/gorhill/uBlock)|Chromium| |✔|
|[NoScript](https://noscript.net/)|Firefox||✔|
|[RequestPolicyContinued](https://github.com/RequestPolicyContinued/requestpolicy)|Firefox|✔|✔|
|[Policeman](https://github.com/futpib/policeman)|Firefox|✔|✔|

### Known Limitations
#### [uMatrix](https://github.com/gorhill/uMatrix/issues/97)|)
* From [issue #93](https://github.com/gorhill/uMatrix/issues/93) it seems that requests made on browser start, before the extension has loaded, are not blockable.
* From the comments in [issue #95](https://github.com/gorhill/uMatrix/issues/95), it seems that "webSockets, update-related and web store-related" requests are not blockable.
* From the comments in [#98](https://github.com/gorhill/uMatrix/issues/98), behind-the-scenes requests are enabled by default, and disabling them will break important functionality in the browser. B-T-S requests include those used for installing & updating extensions, requests made by extensions, and hyper-link auditing requests.
