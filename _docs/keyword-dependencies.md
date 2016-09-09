---
layout: docs
title: dependencies
permalink: /keyword/dependencies
---

## Function


## Valid Values


## Examples


## Meta-schema

	{
		"type": "object",
		"additionalProperties": {
			"anyOf": [
				{
					"$ref": "#"
				},
				{
					"$ref": "#/definitions/stringArray"
				}
			]
		}
	}

