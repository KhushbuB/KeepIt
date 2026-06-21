---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
title: Create a collection
parent: Tutorials
nav_order: 1
grand_parent: KeepIT API
# tags used by AI files
description: Create a `collection` resource to the service
topic_type: tutorial
ai_relevance: high
importance: 6
api_endpoints: /collections
version: "v1.0"
last_updated: "2026-06-21"
# vale  on
# markdownlint-enable
---

# Create a collection

A museum archivist wants to organize Vincent van Gogh's photographs stored on a server. Before adding individual photographs as items, the archivist needs to create a collection to group them together.

In this tutorial, you create a `Van Gogh Photographs` collection using the KeepIT API.

Expect this tutorial to take about 15 minutes to complete.

## Before you begin

Make sure your local KeepIT service is running. If it is not, start it with this command:

```shell
cd <your-github-workspace>/Keepit/api
json-server -w Keepit-source.json
```

## Create the Van Gogh Photographs collection using Postman

To create a new collection:

1. Open the Postman app on your desktop.
1. Create a new request with these values:
    * **METHOD**: `POST`
    * **URL**: `{base_url}/collections`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:

        ```json
        {
            "name": "Van Gogh Photographs",
            "description": "Work of Vincent van Gogh in the Museum of Amsterdam.",
            "location": "Server K, Folder /VanGogh/",
            "itemCount": 3
        }
        ```

1. Choose **Send**.

1. Confirm the response body matches the request body and includes a new `id`.

    ```json
    {
        "name": "Van Gogh Photographs",
        "description": "Work of Vincent van Gogh in the Museum of Amsterdam.",
        "location": "Server K, Folder /VanGogh/",
        "itemCount": 3,
        "id": 5
    }
    ```

The `id` value confirms the collection is created and stored in the service. You can now add individual photographs to this collection as items.

## Next steps

- [Create an item](create-an-item.md) to add a Van Gogh photograph to this collection.
