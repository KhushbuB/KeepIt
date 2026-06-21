---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
title: Get items by ID
parent: Resources
grand_parent: KeepIT API
nav_order: 5
# tags used by AI files
description: GET a `items` resource by ID from the service
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

# Get items by ID

Returns an archived item by ID with the service.

## Endpoint

```shell
{base_url}/items/{id}
```

## Parameters

- id - ID of the item you want to fetch from the Keepit service.

## Request headers

None

## Request body

None

## Response body

```json
{
  "id": 4,
  "title": "Oral history about Austin music scene",
  "creationDate": "2005-04-12",
  "accessionDate": "2018-08-22",
  "format": "MP3",
  "collection": "Texas Oral Histories"
}    
```

## Examples

### `GET` example request

```bash
curl http://localhost:3000/items/4
```

#### `GET` example response

```json
{
  "id": 4,
  "title": "Oral history about Austin music scene",
  "creationDate": "2005-04-12",
  "accessionDate": "2018-08-22",
  "format": "MP3",
  "collection": "Texas Oral Histories"
}   
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 200 | **Success:** Requested data returned successfully |
| ECONNREFUSED | Service is offline. Start, or restart the service and try again. |