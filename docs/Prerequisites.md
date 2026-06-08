---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
title: Prerequisites
nav_order: 2
parent: KeepIT API
# tags used by AI files
description: Prerequisites to use the API service
topic_type: overview
ai_relevance: high
importance: 6
api_endpoints: /collections
version: "v1.0"
last_updated: "2026-03-01"
# vale  on
# markdownlint-enable
---

# Prerequisites

These are the steps you must complete before you can run the tutorials for the **KeepIT API**.

Expect this preparation to take about 15 minutes.

## What you need

To complete the tutorials, install the following on your development system. You might want to open the links in separate browser tabs before you start.

- A current version of [Node.js](https://nodejs.org/en/download) (LTS version recommended)
- Version 0.17.4 of [json-server](https://www.npmjs.com/package/json-server/v/0.17.4)
- A fork of the [KeepIT repository](https://github.com/KhushbuB/KeepIt)
- The [Postman desktop app](https://www.postman.com/downloads/)

  **Note:** Because KeepIT runs locally on `http://localhost:3000`, the web version of Postman can't connect to it. Use the desktop app.

## Start the KeepIT server

1. Open a terminal and navigate to the `api` folder in your local copy of the KeepIT repository.

    ```bash
    cd <your repository workspace>
    cd KeepIt/api
    ```

2. Start the json-server using the KeepIT data file in the terminal.

    ```bash
    json-server -w keepit-source.json
    ```

3. Confirm the server is running. You should see output like this:

    ```
    \{^_^}/ hi!

    Loading keepit-source.json
    Done

    Resources
    http://localhost:3000/collections
    http://localhost:3000/items

    Home
    http://localhost:3000
    ```

## Test your setup

Run a test call from another terminal to confirm the server responds correctly.

```bash
curl http://localhost:3000/collections/1
```

If the server is running correctly, you should see a list of collections like this:

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

## Troubleshooting

If you get an error, check the following:

- You're in the correct directory (`KeepIt/api`)
- The `keepit-source.json` file exists in that folder
- json-server version 0.17.4 is installed (`json-server --version`)
- Node.js is installed and up to date (`node --version`)

Once your server responds correctly, you're ready to start the tutorials.
