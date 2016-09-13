---
layout: docs
title: minLength
permalink: /keyword/minLength
---

## Function

When the instance value is a string, this indicates minimum (inclusive) length of the string.


## Valid Values

Requires that the instance not be empty:

	{ "minLength": 1 }

Requires that the instance be 10 characters or more:

	{ "minLength": 10 }


## Examples


## Meta-schema

	{
		"$ref": "#/definitions/positiveIntegerDefault0"
	}

