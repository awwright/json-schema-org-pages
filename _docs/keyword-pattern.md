---
layout: docs
title: pattern
permalink: /keyword/pattern
---

## Function

When the instance value is a string, this provides a regular expression that a instance string value should match in order to be valid.

The regular expression should be ECMA 262 compatible.


## Valid Values


## Examples

```javascript
schema = { "type":"string", "pattern": "[0-9]+" }

assertValid("12345")
assertValid("contains a number: 1")
assertValid(null) // something besides a string is not constrained

assertInvalid("contains no numbers")

```

## Meta-schema

	{
		"type": "string",
		"format": "regex"
	}

