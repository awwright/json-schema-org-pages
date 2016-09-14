---
layout: docs
title: additionalItems
permalink: /keyword/additionalItems
---

## Function

The value of "additionalItems" MUST be either a boolean or an object.
If it is an object, this object MUST be a valid JSON Schema.

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

