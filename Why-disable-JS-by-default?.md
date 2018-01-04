(Javascript is a general purpose language that is also being used on the server side but here we use `Javascript` to mean Javascript running inside a user's browser)

In the past decades, Javascript has played a key role in shaping our internet experience. From simple interactions (such as "Like", "Upvote", "Reply" buttons) to entire apps and games distributed on the internet, they have been made possible thanks to Javascript.

However, the proliferation of Javascript makes it a security (and privacy) nightmare. Javascript is essentially remote code running inside the browser. What makes it especially powerful, and dangerous, is that the remote party can update their Javascript without active participation of the user.

## Attacks possible through Javascript

### Cross-site scripting
Quoting Wikipedia:
> Cross-site scripting (XSS) is a type of computer security vulnerability typically found in web applications. XSS enables attackers to inject client-side scripts into web pages viewed by other users.

### Launching DoS attacks on other sites

### Side channel attacks
* [ANC](https://www.vusec.net/projects/anc/)
* [Meltdown and Spectre](https://spectreattack.com/)

### Deception
* Tab nabbing
* Resource siphoning (cryptocurrency mining, etc)

## Mitigations

### By users
Users can disable Javascript by default, and enable it for trusted sites only. Possible methods:
* Most mainstream browsers have settings to disable Javascript, but it's not presented to the user in a convenient way. Luckily there are extensions to help with this:
  * uMatrix, NoScript, requestPatrol, and others that provide a fine grained control
  * uBlock and others which help reduce JS usage from third-parties
* Sandboxing the browser application

### By browser developers
* Reducing granularity of time measurement APIs
* Throttling execution of scripts
* Provide more options to user to permit or disallow Javascript
* (long term) Reduce APIs available to the JS context

### By website developers
* Render static pages on the server side. This allows users to stay secure by disabling JS by default.
* Preventing XSS attacks through input validation
* Use of SRI to prevent attacks from third parties