---
layout: docs
title: $schema
permalink: /keyword/$schema
---

## Function

   The "$schema" keyword is both used as a JSON Schema version
   identifier and the location of a resource which is itself a JSON
   Schema, which describes any schema written for this particular
   version.

   This keyword MUST be located at the root of a JSON Schema.  The value
   of this keyword MUST be a URI [RFC3986] and a valid JSON Reference
   [json-reference]; this URI MUST be both absolute and normalized.  The
   resource located at this URI MUST successfully describe itself.  It
   is RECOMMENDED that schema authors include this keyword in their
   schemas.

### Customization

   When extending JSON Schema with custom keywords, schema authors
   SHOULD define a custom URI for "$schema".  This custom URI MUST NOT
   be one of the predefined values.

## Valid Values

The value must be a string that is a valid URI.


## Examples

{ "$schema": "http://json-schema.org/draft-04/schema#" }


## Meta-schema

	{
		"type": "string",
		"format": "uri"
	}

