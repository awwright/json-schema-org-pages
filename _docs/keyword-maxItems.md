---
layout: docs
title: maxItems
permalink: /keyword/maxItems
---

## Function

If an array instance, verifies that the array has at least the specified number of items.

## Valid Values

## Examples

```javascript
schema = { "maxItems": 2 }

assertValid([])
assertValid([1])
assertValid([1, 2])

assertInvalid([1, 2, 3])
```


## See also

* [minItems](minItems)


## Meta-schema

	{
		"$ref": "#/definitions/positiveInteger"
	}

