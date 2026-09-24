# Crowdtest Task Context

## Repository baseline

- Upstream repository: https://github.com/langgenius/dify
- Participant fork: https://github.com/mengqian1233/dify
- Task branch: `zhongce-47`
- Source baseline commit: `74af4f230813a7465e121cd74883585f8819ee2a`

All four evaluations must use the same commit from the task branch. Pin the final commit URL in the crowdtest prompt or attachment metadata after committing these task materials.

## Business context

This repository is an existing Dify codebase. The requested change is an incremental enhancement to the Workflow application experience: allow a configured workflow output to be presented as a safe, structured visual report in the published Workflow WebApp while retaining access to the original output.

The detailed functional requirements and acceptance criteria are provided in the crowdtest prompt and rubrics. This file supplies repository and environment facts only; it does not prescribe an implementation.

## Available material

- `crowdtest/sample-business-data.json`: sanitized example source data for reproducing report-rendering scenarios without a paid external service.
- Existing repository source code, lockfiles, development scripts, tests, and project documentation.

## Environment constraints

- Do not require paid external APIs or real model credentials to verify the new report-rendering behavior.
- Do not commit `.env` files, access tokens, credentials, generated build artifacts, dependency directories, database volumes, caches, or user-uploaded content.
- Preserve the existing Workflow API response and streaming-event contracts.
- Follow the repository's own scoped development instructions and use the commands supported by this exact baseline.

## Required verification scenarios

The implementation must provide reproducible verification for:

1. The feature is disabled and the existing result experience remains unchanged.
2. The feature is enabled and valid example data produces a report containing summary metrics, explanatory content, a table, and supported charts.
3. The report view can switch back to the original workflow output.
4. Empty, malformed, partially missing, oversized, and unsafe input is handled without a page crash or script execution.
5. Existing workflows without the new configuration remain readable and runnable.

## Delivery expectations

- Commit all relevant source changes, tests, fixtures, and documentation in this repository.
- Record the exact verification commands that were actually run and their results.
- If an environment limitation prevents a check, record the limitation and the command needed to reproduce it; do not claim an unexecuted check passed.

