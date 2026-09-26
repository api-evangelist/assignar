---
name: assignar-create-user-with-skill
description: Create a new user and assign a skill to that user.
api: openapi/assignar-openapi.yaml
operations:
- newUser
- createUserSkill
- getUserSkills
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/assignar-openapi.yaml ; every operationId checked against the contract
---

# assignar-create-user-with-skill

Create a new user and assign a skill to that user.

## Steps

1. 1. Call `newUser` with the required user fields in the request body.
2. 2. Call `createUserSkill` with the `userId` returned from step 1 and the skill data in the request body.
3. 3. Call `getUserSkills` with the same `userId` to verify the skill was added.

## Rules

- Auth: Include an OAuth2 bearer token in the `Authorization` header for all requests.
- Idempotency: `newUser` and `createUserSkill` are not idempotent; avoid duplicate calls.
- Errors: Expect standard HTTP error codes (4xx for client errors, 5xx for server errors) as defined by the API.
