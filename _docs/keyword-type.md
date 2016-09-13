---
layout: docs
title: type
permalink: /keyword/type
---

## Function

This is a type definition value. This can be an object type definition, an array type definition, simple type, or a union type


## Valid Values


## Examples


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

