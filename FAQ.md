# Concerns About Java

##

# General

## Why does it block cookies and javascript etc by default?

Those technologies are a major concern from a security and privacy perspective. Cookies allow servers, especially third parties, to track you. Javascript opens up an even larger avenue for tracking and finger-printing, while also opening up a huge surface for attack.

Apart from the security concerns, executing javascript by default consumes more power, which is especially significant on mobile devices. 

That said, `gngr` does allow you to change this policy, either globally or on a per-site basis, via the [[RequestManager]].

