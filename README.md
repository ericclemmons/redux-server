# redux-server
> Redux-powered server &amp; middleware for predictably handling requests with immutable responses.

## Why?

Over the past several years, I've bounced between Express, Koa, Hapi, and finally back to Express for my server needs.

With React, React Router, & GraphQL, the server has become increasingly simple.

Unfortunately, the majority of middleware rely on clobbering objects & references (e.g. monkey-patching `res.send`, mutating objects `req.session`, adding to `res.locals`, etc.) just to send a request.

In fact, if a middleware calls `res.send`, other middleware have to hijack it with their own version just to intercept the response!

This approach allows for the `response` object to be handled dynamically, allowing for several scenarios:

- Universal API calls on both the client & server.
- Responding to various errors differently.
- Short-circuiting the dispatch with a redirect.
- Rendering the payload as JSON, HTML, or even Markdown.
- Hooking into the payload for tracking events.
- Simpler `response` object for logging & debugging.

- - - 

_More to come_
