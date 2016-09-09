---
layout: page
title: JSON Schema
permalink: /
---

JSON Schema is a vocabulary that allows you to annotate and validate JSON documents.

## Introduction

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

<a href="doc">Continue reading the Reference guide.</a>

## The Specification

If you implement or use JSON Schema, get involved with the community of other developers! We officially hang out at the following places:

<ul>
	<li>the <a href="https://groups.google.com/forum/#!forum/json-schema">Google Group</a> - For general questions, support, announcements, suggestions, and controversy; start here.</li>
	<li>the <a href="http://github.com/json-schema-org/json-schema-spec">Specification repository on GitHub</a> - If you have a particular change you'd like to propose, and you've discussed it with the community, get involved at the GitHub repository.</li>
	<li>the <a href="http://github.com/json-schema-org/json-schema-spec">Website repository on GitHub</a> - If you have an implementation you'd like to list, a change to make to one of the pages on this website, or have found a spelling problem, open an issue here.</li>
	<li>the <a href="irc://chat.freenode.net/json-schema">IRC channel</a> (<a href="https://webchat.freenode.net/?channels=json-schema">Freenode Webchat</a>) - If you wanna chat with people who implement and use JSON Schema, join our Freenode channel. Say something, and be patient for a response! It might take a few hours for the right person to see your question.</li>
</ul>
