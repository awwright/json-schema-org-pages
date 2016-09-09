---
layout: page
title: Introduction
permalink: /
---

JSON Schema is a vocabulary that allows you to annotate and validate JSON documents.

The default JSON Schema is a blank object, which validates nothing and describes nothing:

    {}

This empty, default JSON Schema validates successfully against anything. The JSON document being validated or described we call the _instance_, and the document containing the description is called the _schema_.

You can describe constraints on an instance by adding validation keywords to the schema. The most common one restricts which type the instance must be:

    { "type": "string" }

