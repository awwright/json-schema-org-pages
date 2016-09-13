---
layout: docs
title: additionalProperties
permalink: /keyword/additionalProperties
---

## Function

This provides a default property definition for all properties that are not explicitly defined in an object type definition.


## Valid Values


## Examples


## Meta-schema

	{
		"anyOf": [
			{
				"type": "boolean"
			},
			{
				"$ref": "#"
			}
		],
		"default": {}
	}

