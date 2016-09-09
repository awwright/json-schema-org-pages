---
layout: docs
title: Validation Property "type"
permalink: /keyword/type
---


### Valid values

The value of this keyword MUST be either a string or an array. If it is an array, elements of the array MUST be strings and MUST be unique.

String values MUST be one of the seven primitive types defined by the core specification.


### Conditions for successful validation

An instance matches successfully if its primitive type is one of the types defined by keyword. Recall: "number" includes "integer".



### Examples

    { "type": "object" }


