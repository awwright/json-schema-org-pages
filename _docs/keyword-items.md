---
layout: docs
title: items
permalink: /keyword/items
---

## Function

Validates individual items in an array, if an array instance:

If the property is an array, it specifies a list of schemas that must validate against each respective item of an array instance,

If the property is an object, functions the same as "additionalItems" by providing a schema that every item in the instance array must validate against.


## Valid Values

Must be an array or an object.

## Examples

```javascript
schema = { "items": {"type":"string"} }

assertValid([])
assertValid(["123"])
assertValid(["1", "2", "3"])
assertValid(123) // skips non-array instances

assertInvalid([123])
assertInvalid([1, 2, 3])
```

```javascript
schema = { "type":"array", "items": [{"type":"number"}, {"type":"string"}] }

assertValid([]) // items are optional without "minItems"
assertValid([1])
assertValid([1, "2"])
assertValid([1, "2", null]) // additional items are unconstrained without additionalItems or maxItems

assertInvalid(["1", 2])
assertInvalid([null])
```

## Meta-schema

	{
		"anyOf": [
			{
				"$ref": "#"
			},
			{
				"$ref": "#/definitions/schemaArray"
			}
		],
		"default": {}
	}

