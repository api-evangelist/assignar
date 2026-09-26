---
name: assignar-create-order-with-task
description: Create a new order and add a task to it.
api: openapi/assignar-openapi.yaml
operations:
- newOrder
- newOrderTask
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/assignar-openapi.yaml ; every operationId checked against the contract
---

# assignar-create-order-with-task

Create a new order and add a task to it.

## Steps

1. 1. Call `newOrder` with the required order fields in the request body.
2. 2. Call `newOrderTask` using the `orderId` returned from step 1 and provide the task details in the request body.

## Rules

- Auth: Include an OAuth2 bearer token in the `Authorization` header (`Authorization: Bearer <token>`).
- Idempotency: POST operations (`newOrder`, `newOrderTask`) support the `Idempotency-Key` header to avoid duplicate creation.
