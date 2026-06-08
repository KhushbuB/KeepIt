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
last_updated: "2026-03-01"
# vale  on
# markdownlint-enable
---

# Create a collection

In this tutorial, you learn the operations to call to add a new collection.

Expect this tutorial to take about 15 minutes to complete.

## Create a new collection using Postman

Creating a new collection to the service requires you to use `POST` method to store the details of the new collection resource in the service.

To add a new collection:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/Keepit/api
    json-server -w Keepit-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{base_url}/collections`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```json
        {
            "name": "Van Gogh Photographs",
            "description": "Work of Vincent van Gogh in the Museum of Amsterdam.",
            "location": "Server K, Folder /VanGogh/",
            "itemCount": 3
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this.
    Note that the names should be the same as you used in
    your **Request body** and the response should include the new `id`.

    ```json
    {
        "name": "Van Gogh Photographs",
        "description": "Work of Vincent van Gogh in the Museum of Amsterdam.",
        "location": "Server K, Folder /VanGogh/",
        "itemCount": 3,
        "id": 5
    }
    ```
