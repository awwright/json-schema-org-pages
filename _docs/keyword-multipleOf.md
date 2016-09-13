---
layout: docs
title: multipleOf
permalink: /keyword/multipleOf
---

## Function

Requires that the instance be an integral multiple of the specified value.


## Valid Values

The keyword's value must be a number.


## Examples


Ensures the instance is an integer:

	{ "multipleOf": 1 }

Ensures the instance is an even integer:

	{ "multipleOf": 2 }

Ensures the instance has, at most, two decimal places of precision:

	{ "multipleOf": 0.01 }


## Meta-schema

	{
		"type": "number",
		"minimum": 0,
		"exclusiveMinimum": true
	}

