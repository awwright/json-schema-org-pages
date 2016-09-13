---
layout: docs
title: maxLength
permalink: /keyword/maxLength
---

## Function

When the instance value is a string, this indicates maximum allowable length (inclusive) of the string.


## Valid Values


## Examples

Prohibits all strings except the empty (zero-length) string:

	{ "maxLength": 0 }

Caps strings at max tweetable length:

	{ "maxLength": 140 }


## Meta-schema

	{
		"$ref": "#/definitions/positiveInteger"
	}

