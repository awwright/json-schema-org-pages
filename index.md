---
layout: page
title: Introduction
permalink: /
---

JSON Schema is a vocabulary that allows you to annotate and validate JSON documents.

The JSON document being validated or described we call the _instance_, and the document containing the description is called the _schema_.

The most basic schema is a blank JSON object, which constrains nothing, allows anything, and describes nothing:

    {}


You can apply constraints on an instance by adding validation keywords to the schema. For instance, the "type" keyword can be used to restrict an instance to an object, array, string, number, boolean, or null:

    { "type": "string" }

