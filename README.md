# Sketchpacks.com API documentation

This repository contains the documentation for [Sketchpacks](http://www.sketchpacks.com)’s API.

#### Contents

- [Overview](#1-overview)
- [Resources](#2-resources)
  - [Plugins](#21-plugins)

## 1. Overview

Sketchpacks' API is a JSON-based API. All requests are made to endpoints beginning:
`http://www.medium.com/api/v1`


## 2. Resources

The API is RESTful and arranged around resources. 

### 2.1. Plugins

#### A collection of all plugins

The REST API endpoint exposes this list of plugins as a collection of resources. A request to fetch a list of plugins looks like this:

```
GET http://www.sketchpacks.com/api/v1/plugins
```

The response is a list of plugin objects. 

Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
[
	{
		"name": "sync.sketchplugin",
		"description": "Use Google Sheets to sync typography across your team.",
		"author": "Stan",
		"owner": "nolastan"
	},
	{
		"name": "qordoba-for-sketch",
		"description": "Qordoba’s Sketch plugin allows designers to translate their mockups to other languages, making product internationalization easier.",
		"author": "Qordoba",
		"owner": "Qordobacode"
	}
]

```
