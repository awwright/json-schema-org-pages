---
layout: docs
title: Validation
permalink: /guide/validation
---

The Validation Function.

A JSON Schema validation is a pure (mathematical) function call that determines if an instance is valid, invalid, or indeterminate (an error condition like an invalid schema).

## Validating an entire instance

Validating an instance is done

## Validating a part of an instance

You might be interested in validating only a part of an instance against a schema, seeing if just a property within the object instance, or an item in the array instance, causes any problems. This strategy might be used to determine if a field in a user interface should be highlighted with an error or not, for example.

## Dereferencing external schemas

JSON Schema uses URIs ([RFC 3986](https://tools.ietf.org/html/rfc3986)) to identify and name schemas. For human convienence, it is customary to use a URL and make the schema in question downloadable at that URL. However, this is not necessary, and no guarentee is made of availability. It is up to the party performing validation to provide all the necessary schemas to the validator at validation-time.

The only time it is appropriate for a computer program to download a schema from a remote party is if the client is a generic, RESTful User-Agent that can use the schema to style data for a user. In this case, the user agent must cache the schema according to the caching headers in the HTTP response. For more information, see [HTTP APIs](http).
