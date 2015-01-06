|Name|Used with|Switchboard*|Active as of Q1 2015|
|----|---------|-----------|--------------------|
|[uMatrix](https://github.com/gorhill/uMatrix)|Chromium|✔|✔|
|[uBlock](https://github.com/gorhill/uBlock)|Chromium| |✔|
|[NoScript](https://noscript.net/)|Firefox||✔|
|[RequestPolicyContinued](https://github.com/RequestPolicyContinued/requestpolicy)|Firefox|✔|✔|
|[Policeman](https://github.com/futpib/policeman)|Firefox|✔|✔|

### Known Limitations
#### [uMatrix](https://github.com/gorhill/uMatrix/issues/97)
* From [issue #93](https://github.com/gorhill/uMatrix/issues/93) it seems that requests made on browser start, before the extension has loaded, are not blockable.
* From the comments in [issue #95](https://github.com/gorhill/uMatrix/issues/95), it seems that "webSockets, update-related and web store-related" requests are not blockable.
* From the comments in [#98](https://github.com/gorhill/uMatrix/issues/98), behind-the-scenes requests are enabled by default, and disabling them will break important functionality in the browser. B-T-S requests include those used for installing & updating extensions, requests made by extensions, and hyper-link auditing requests.

### * Switchboard
The name for the concept comes from the name of the HTTP-SwitchBoard extension (predecessor to uMatrix).

The extensions which have a switchboard like interface enable the user to block requests based on the request's domain name, the primary frame's domain-name, and also the type of request.

In contrast, extensions like NoScript have a global switch. If I allow scripts from DontBeEvil.com, they are enabled on all domains. They don't prevent XSS attacks, for example.

If there's a better name for this concept, please do suggest one.