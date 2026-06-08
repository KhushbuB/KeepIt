---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
parent: Resources
nav_order: 1
# tags used by AI files
description: GET all `collections` resources from the service
topic_type: reference
ai_relevance: high
importance: 7
api_endpoints: /collections
version: "v1.0"
last_updated: "2026-03-01"
# vale  on
# markdownlint-enable
---

 <!-- vale off -->

# Get all collections

Returns all the collections archived with the service.

## Endpoint

```shell
{base_url}/collections
```

## Parameters

None

## Request headers

None

## Request body

None

## Response body

```json
[
  {
    "id": 1,
    "name": "Austin Photographs",
    "description": "Historical and contemporary photographs of Austin, Texas.",
    "location": "Server A, Folder /austin-photos/",
    "itemCount": 18
  }
]     
```

## Examples

### `GET` example request

```bash
curl http://localhost:3000/collections
```

#### `GET` example response

```json
[
  {
    "id": 1,
    "name": "Austin Photographs",
    "description": "Historical and contemporary photographs of Austin, Texas.",
    "location": "Server A, Folder /austin-photos/",
    "itemCount": 18
  },
  {
    "id": 2,
    "name": "Austin Photographs",
    "description": "Historical maps of Austin and surrounding areas.",
    "location": "Server A, Folder /austin-maps/",
    "itemCount": 12
  },
  {
    "id": 3,
    "name": "Texas Newspapers",
    "description": "Digitized issues of historical Texas newspapers.",
    "location": "Server B, Folder /tx-newspapers/",
    "itemCount": 34
  },
  {
    "id": 4,
    "name": "Texas Oral Histories",
    "description": "Audio recordings of interviews with Texas residents.",
    "location": "Server C, Folder /tx-oral-histories/",
    "itemCount": 22
  }
]%   
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 200 | **Success:** Requested data returned successfully |
| ECONNREFUSED | Service is offline. Start, or restart the service and try again. |