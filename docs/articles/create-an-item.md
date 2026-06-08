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
last_updated: "2026-03-01"
# vale  on
# markdownlint-enable
---

# Create an item

In this tutorial, you learn the operations to call to add a new item.

Expect this tutorial to take about 15 minutes to complete.

## Create a new item using Postman

Creating a new item to the service requires you to use `POST` method to store the details of the new collection resource in the service.

To add a new item:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/Keepit/api
    json-server -w Keepit-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{base_url}/items`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```json
        {
            "title": "Photo of The Starry Night",
            "creationDate": "1996-09-23",
            "accessionDate": "2026-06-08",
            "format": "JPG",
            "collection": "Van Gogh Photographs"
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this.
    Note that the names should be the same as you used in
    your **Request body** and the response should include the new `id`.

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
