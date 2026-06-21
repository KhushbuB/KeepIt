---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
title: Create an item
parent: Tutorials
nav_order: 2
grand_parent: KeepIT API
# tags used by AI files
description: Create an `items` resource to the service
topic_type: tutorial
ai_relevance: high
importance: 6
api_endpoints: /items
version: "v1.0"
last_updated: "2026-06-21"
# vale  on
# markdownlint-enable
---

# Create an item

After creating the `Van Gogh Photographs` collection, the museum archivist needs to add individual photographs to it. Each photograph is stored as an item linked to the collection.

In this tutorial, you add a photograph of *The Starry Night* as an item in the `Van Gogh Photographs` collection.

Expect this tutorial to take about 15 minutes to complete.

## Before you begin

- Complete the [Create a collection](create-a-collection.md) tutorial. This tutorial adds items to the `Van Gogh Photographs` collection created in that tutorial.
- Make sure your local KeepIT service is running. If it is not, start it with this command:

    ```shell
    cd <your-github-workspace>/Keepit/api
    json-server -w Keepit-source.json
    ```

## Add The Starry Night photograph as an item using Postman

To create a new item:

1. Open the Postman app on your desktop.
1. Create a new request with these values:
    * **METHOD**: `POST`
    * **URL**: `{base_url}/items`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:

        ```json
        {
            "title": "Photo of The Starry Night",
            "creationDate": "1996-09-23",
            "accessionDate": "2026-06-08",
            "format": "JPG",
            "collection": "Van Gogh Photographs"
        }
        ```

1. Choose **Send**.

1. Confirm the response body matches the request body and includes a new `id`.

    ```json
    {
        "title": "Photo of The Starry Night",
        "creationDate": "1996-09-23",
        "accessionDate": "2026-06-08",
        "format": "JPG",
        "collection": "Van Gogh Photographs",
        "id": 5
    }
    ```

The `id` value confirms the item is created and linked to the `Van Gogh Photographs` collection.
