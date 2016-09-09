---
layout: docs
title: type
permalink: /keyword/type
---

## Function


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

