---
# markdownlint-disable
# vale off
# tags used by just-the-docs theme
layout: default
title: KeepIT API
nav_order: 1
has_children: true
has_toc: true
# tags used by AI files
description: documentation landing page
topic_type: overview
ai_relevance: high
importance: 8
related_pages: 
    - /Resources
version: "v1.0"
last_updated: "2026-03-01"
# vale  on
# markdownlint-enable
---
 
 <!-- vale off -->

# KeepIT API

## Archive it. Find it. Keep it.

Welcome to the KeepIT API.

Use this API to manage your digital archive - organize collections, add items, and retrieve records with simple, lightweight REST endpoints.

## What you can do

- Create and browse archive collections
- Add items to a collection
- Retrieve a single collection or item by ID

## Getting started

1. Start the KeepIT json server
2. Send requests to `http://localhost:3000`
3. Use curl, Postman, or any API client to interact with the API

## API endpoints

### Collections

- Get all collections - `GET /collections`
- Get collections by ID - `GET /collections/{id}`
- Create a collection - `POST /collections`

### Items

- Get all items - `GET /items`
- Get an item by ID - `GET /items/{id}`
- Create an item - `POST /items`

## Learn more

* [Get all collections](get-all-collection.md)
* [Get collections by ID](get-collection-by-id.md)
* [Create a collection](create-a-collection.md)
* [Get all items](get-all-items.md)
* [Get items by ID](get-items-by-id.md)

## References

- [To-Do API Service](https://uwc2-apidoc.github.io/to-do-service-sp26/)

## Contact us

Have questions, feedback, or found an issue?

- GitHub: [KeepIT Repository](https://github.com/KhushbuB/KeepIt)
- Doc site: [khushbub.github.io/KeepIt](https://khushbub.github.io/KeepIt/)
