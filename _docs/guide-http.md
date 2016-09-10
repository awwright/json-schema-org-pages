---
layout: docs
title: HTTP APIs
permalink: /guide/http
---

As a hypermedia format, JSON Schema is naturally suited for using in HTTP, as a more machine-accessible RESTful format than HTML frequently allows.


## Profile media-type parameter

To distinguish different "flavors" or profiles of JSON documents from each other, use the `profile` media-type parameter:

    Content-Type: application/json; profile="http://example.com/my-hyper-schema#"

The "profile" media-type parameter is never supposed to be dereferenced or used to download a schema, it is strictly an identifier provided for the benefit of clients that have pre-programmed knowledge of what that profile means.


## Link header

If a client has requested a JSON document from an HTTP server, you can use the `Link` header to define where a schema may be downloaded from, if the client doesn't already know anything about the JSON document or its profile type.

The link relation used is "describedby", a generic link relation first described in [POWDER](https://www.w3.org/TR/powder-dr/#semlink).

    Link: <http://example.com/my-hyper-schema#>; rel="describedBy"

If the user-agent doesn't know how to handle the received JSON profile, it can download a JSON Schema describing the profile from the provided "describedBy" link.

User agents that download a schema must do so from the Link header, and must cache the schema and follow the provided caching headers.
