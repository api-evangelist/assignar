---
name: assignar-create-and-retrieve-contact
description: Create a new contact and then retrieve it to confirm creation.
api: openapi/assignar-openapi.yaml
operations:
- postContact
- getContact
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/assignar-openapi.yaml ; every operationId checked against the contract
---

# assignar-create-and-retrieve-contact

Create a new contact and then retrieve it to confirm creation.

## Steps

1. 1. Use `postContact` with required body fields for the new contact.
2. 2. Use `getContact` with the `contactId` returned from the creation response.

## Rules

- Auth: Include an OAuth2 bearer token in the `Authorization` header.
- Idempotency: `postContact` is not idempotent; avoid duplicate calls.
