---
layout: docs
title: type
permalink: /keyword/type
---

## Function

Restricts which of the basic types the instance may be. A string restricts to a single type, an array of strings ensures the instance is one of several types.


## Valid Values

Must be a string, or array of strings.


## Examples


```javascript
schema = { "type": "null" }

assertValid(null)

assertInvalid(0)
assertInvalid("")
```


```javascript
schema = { "type": "number" }

assertValid(0)
assertValid(1)

assertInvalid("0")
assertInvalid(true)
```


```javascript
schema = { "type": "array" }

assertValid([])
assertValid([1])

assertInvalid(1)
assertInvalid({})
```


```javascript
schema = { "type": ["array", "object"] }

assertValid([])
assertValid({})

assertInvalid(1)
assertInvalid("foo")
```


## Meta-schema

	{
		"anyOf": [
			{
				"$ref": "#/definitions/simpleTypes"
			},
			{
				"type": "array",
				"items": {
					"$ref": "#/definitions/simpleTypes"
				},
				"minItems": 1,
				"uniqueItems": true
			}
		]
	}

