---
layout: docs
title: Basics
permalink: /guide/basics
---

The JSON document being validated or described we call the _instance_, and the document containing the description is called the _schema_.

The most basic schema is a blank JSON object, which constrains nothing, allows anything, and describes nothing:

    {}


You can apply constraints on an instance by adding validation keywords to the schema. For instance, the "type" keyword can be used to restrict an instance to an object, array, string, number, boolean, or null:

    { "type": "string" }


JSON Schema nests schemas to describe things like the values of items in an array, or the values of properties in an object. Multiple constraints can be combined, and you can also add annotations to your JSON instance:

    { "description": "A geographical coordinate"
    , "type": "object"
    , "properties":
        { "latitude": { "type": "number" }
        , "longitude": { "type": "number" }
        }
    }

JSON Schema is a hypermedia format ideally suited for using in HTTP. JSON Schema documents are identified by URIs, which can be used in HTTP Link headers, and inside JSON Schema documents to allow recursive definitions.
