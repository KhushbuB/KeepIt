---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
parent: Resources
grand_parent: KeepIT API
nav_order: 2
# tags used by AI files
description: GET a `collections` resource by ID from the service
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

# Get collections by ID

Returns a archived collections by ID with the service.

## Endpoint

```shell
{base_url}/collections/{id}
```

## Parameters

- id - ID of the collection you want to fetch from the Keepit service.

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
curl http://localhost:3000/collections/4
```

#### `GET` example response

```json
[
  {
    "id": 4,
    "name": "Texas Oral Histories",
    "description": "Audio recordings of interviews with Texas residents.",
    "location": "Server C, Folder /tx-oral-histories/",
    "itemCount": 22
  }
]   
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 200 | **Success:** Requested data returned successfully |
| ECONNREFUSED | Service is offline. Start, or restart the service and try again. |