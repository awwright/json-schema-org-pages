---
layout: docs
title: Data Model
permalink: /guide/model
---


JSON Schema operates on a basic data model derived from the JSON grammar. JSON Schema treats a JSON document as an "instance" that can have one of six primitive types:

* object - an unordered map of a string to an instance
* array - an ordered list of instances
* string - a Unicode string
* number - an arbritrary length, floating point number
* boolean - one of the two special values `true` or `false`
* null - the special value `null`

JSON Schema defines two instances as equal if and only if they are of the same type and carry the same mathematical value (codepoint-for-codepoint, property-for-property, or item-for-item, in the case of strings, objects, and arrays, respectively). Two instances that are JSON-Schema-equal will always validate the same, regardless of whitespace, escapes, or formatting.

JSON Schema does not provide any way to specify how the data is formatted; for instance, verifying presence or absence of whitespace, `\uXXXX` escaped vs. UTF-8 encoded forms in strings, order of properties in an object, or duplicate properties in an object. These are considered parser-level duties, and are defined in JSON itself.

Although validators are defined in terms of this data model, JSON Schema only defines how to validate an `application/json` document, serialized as a series of bytes. JSON Schema does not provide any way to describe in-memory objects like pointers, `NaN`, `undefined`, imaginary numbers, native Date objects, unserialized structs, etc.

However, JSON Schema can help _annotate_ a serialized object that it is correctly _parsed_ back into a native representation. For example, JSON Schema can annotate a string as an RFC 3339 date, and you can use a JSON parser that looks for these annotations and automatically converts it to your language's native `Date` object, if any.

Likewise, you could also use JSON Schema to annotate a property as serialized version of an object representing a geographical coordinate, and automatically convert this JSON object to an instance of a `GeoCoord` in your native application.

Despite these restrictions, you _can_ still use JSON Schema to validate in-memory objects:

* The in-memory objects _must_ be serializable to JSON (circular references removed or reduced to a string reference), and
* The validator _must_ return the same result as if they were first serialized to JSON before validation.
