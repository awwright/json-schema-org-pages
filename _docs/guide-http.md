---
layout: docs
title: HTTP APIs
permalink: /guide/http
---

As a hypermedia format, JSON Schema is naturally suited for using in HTTP, as a more machine-accessible RESTful format than HTML frequently allows.

## Profile media-type parameter

To distinguish different "flavors" or profiles of JSON documents from each other, use the `profile` media-type parameter:

    Content-Type: application/json; profile="http://example.com/my-hyper-schema#"

## Link header

Use the HTTP `Link` header to annotate existing HTTP apis:

    Link: <http://example.com/my-hyper-schema#>; rel="describedBy"

The "describedby" link relation is a generic link relation first described in [POWDER](https://www.w3.org/TR/powder-dr/#semlink).
