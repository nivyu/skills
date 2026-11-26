---
name: boundry-review
description: Review trust boundaries before granting or expanding access, sharing credentials or sensitive data with a new recipient, or enabling a new privileged job or integration. Use when changing who can run or modify privileged code or delegate permissions.
---

# Review trust boundaries

Apply this review as soon as the proposed implementation changes effective access, even if the original task was routine. A material architecture change triggers this review when it changes which people, systems, or code are trusted. Check inherited access before first activating privileged jobs or integrations, including when they use existing roles or credentials. Continue routine work under existing authorization when the identity, scope, destination, and controls already cover the operation.

## Identify what changes

Compare the current and proposed access. Identify who or what receives it, the resources and actions it covers, and where it applies. Include permissions the recipient can delegate, downstream credentials it can obtain, who controls the code that runs with the access, and how long the access lasts. Verify credential scope from configuration or provider metadata without retrieving secret values for review.

## Limit the authority and surface decisions

Prefer an existing authorized path that meets the goal. Where new access is necessary, scope it to the required identities, actions, resources, and duration. Separate provisioning from routine execution when that removes privileged access from the workload. Enforce any ceiling on delegated permissions through controls the delegate cannot change. Bind privileged execution to reviewed code, including the scripts it runs, and keep untrusted code outside the privileged context.

If the proposed action or its material consequences fall outside existing authorization, pause that action before changing access, handing off credentials or data, or starting privileged execution. Summarize the change, its effective reach, the narrower options, and how temporary access will end. Ask for approval of the outstanding decision and continue independent work. Revisit approval if the material scope changes.

## Verify the boundary

Before live use, verify that the required operations are allowed and that representative out-of-scope operations are denied. Use policy analysis, configuration checks, or tests with disposable resources as appropriate. If a limit the task relies on remains unverified, hold the affected live action and state which check is missing.

When temporary access ends, verify cleanup. Check the original access path and any downstream credentials separately, since closing one path may leave credentials issued through it valid.
