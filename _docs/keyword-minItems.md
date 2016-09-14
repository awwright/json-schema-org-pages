---
layout: docs
title: minItems
permalink: /keyword/minItems
---

## Function

If an array instance, verifies that the array does not have more than the specified number of items.

## Valid Values


## Examples

```javascript
schema = { "minItems": 2 }

assertValid([1, 2, 3])
assertValid([1, 2])

assertInvalid([1])
assertInvalid([])
```

## See also

* [maxItems](maxItems)

## Meta-schema

	{
		"$ref": "#/definitions/positiveIntegerDefault0"
	}

