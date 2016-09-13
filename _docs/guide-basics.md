---
layout: docs
title: Basics
permalink: /guide/basics
---

The JSON document being validated or described we call the _instance_, and the document containing the description is called the _schema_.

The most basic schema is a blank JSON object, which constrains nothing, allows anything, and describes nothing:

```javascript
schema = {}

assertValid(null)
assertValid(true)
assertValid(12345)
assertValid("12345")
```

You can apply constraints on an instance by adding _validation keywords_ to the schema. For instance, the "type" keyword can be used to restrict an instance to an object, array, string, number, boolean, or null:

```javascript
schema = { "type": "string" }

assertValid("A string");
assertValid("12345");
assertValid(""); // empty string

assertInvalid(null);
assertInvalid(true);
assertInvalid(12345);
```

Most of the validation keywords only apply when the instance is of a certain type. "maxLength" will only error if the instance is a string, and "maximum" will only error if the instance is a number. Combine with "type" to ensure that the instance is run by at least one or the other:

```javascript
schema = {
	"type": ["string", "number"],
	"maxLength": 5,
	"maximum": 1000
}

assertValid(123);
assertValid("123");

assertInvalid(null);
assertInvalid(1234567890);
assertInvalid("1234567890");
```

JSON Schema nests schemas to describe things like the values of items in an array, or the values of properties in an object. Multiple constraints can be combined, and you can also add annotations to your JSON instance:

```javascript
{ "description": "A geographical coordinate"
, "type": "object"
, "properties":
{ "latitude": { "type": "number" }
, "longitude": { "type": "number" }
}
}
```


JSON Schema is a hypermedia format ideally suited for using in HTTP. JSON Schema documents are identified by URIs, which can be used in HTTP Link headers, and inside JSON Schema documents to allow recursive definitions.
