---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
title: Get all items
parent: Resources
grand_parent: KeepIT API
nav_order: 4
# tags used by AI files
description: GET all `item` resources from the service
topic_type: reference
ai_relevance: high
importance: 7
api_endpoints: /items
version: "v1.0"
last_updated: "2026-03-01"
# vale  on
# markdownlint-enable
---

 <!-- vale off -->

# Get all items

Returns all the items archived with the service.

## Endpoint

```shell
{base_url}/items
```

## Parameters

None

## Request headers

None

## Request body

None

## Response body

```json
  {
    "id": 1,
    "title": "Photo of Congress Avenue, 1920",
    "creationDate": "1920",
    "accessionDate": "2019-05-14",
    "format": "TIFF",
    "collection": "Austin Photographs"
  }
```

## Examples

### `GET` example request

```bash
curl http://localhost:3000/items
```

#### `GET` example response

```json
[
  {
    "id": 1,
    "title": "Photo of Congress Avenue, 1920",
    "creationDate": "1920",
    "accessionDate": "2019-05-14",
    "format": "TIFF",
    "collection": "Austin Photographs"
  },
  {
    "id": 2,
    "title": "Map of Austin, 1885",
    "creationDate": "1885",
    "accessionDate": "2020-02-03",
    "format": "PDF",
    "collection": "Austin Photographs"
  },
  {
    "id": 3,
    "title": "Austin American-Statesman, June 1936",
    "creationDate": "1936-06",
    "accessionDate": "2021-09-15",
    "format": "PDF",
    "collection": "Texas Newspapers"
  },
  {
    "id": 4,
    "title": "Oral history about Austin music scene",
    "creationDate": "2005-04-12",
    "accessionDate": "2018-08-22",
    "format": "MP3",
    "collection": "Texas Oral Histories"
  }
]
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 200 | **Success:** Requested data returned successfully |
| ECONNREFUSED | Service is offline. Start, or restart the service and try again. |