# Alphacast documentation instructions

## Project

This repository contains the public documentation published at https://learn.alphacast.io. It covers Alphacast concepts, the HTTP API, data uploads and providers, pipeline steps, the Python SDK, and MCP.

- Write pages as MDX with YAML frontmatter.
- Configure the site and navigation in `docs.json`.
- Check `.mintignore` before exposing existing content. Some pipeline API pages and integrations are intentionally unpublished.
- Consult https://www.mintlify.com/docs for current Mintlify configuration and component behavior.

## Writing and terminology

- Write in English, consistent with the existing documentation.
- Use active voice and address the reader as "you".
- Keep sentences concise and use sentence case for headings.
- Use **bold** for UI labels and `code` for commands, paths, parameters, and identifiers.
- Use Alphacast for the product name. Distinguish repositories, datasets, pipelines, and pipeline steps.
- Use Python SDK for the Python client and Model Context Protocol (MCP) when introducing MCP.
- Preserve exact endpoint paths, parameter names, tool names, and UI labels.
- Reuse existing components and page structure where practical.

## Accuracy and public content

- Verify technical claims against the relevant implementation or authoritative documentation. Do not invent endpoints, tools, defaults, provider counts, or supported behavior.
- State uncertainty when behavior cannot be verified.
- Use placeholders for credentials and synthetic data for examples. Do not publish API keys, internal operational details, or private customer data.
- Keep edits within the requested scope. Do not expose ignored pages or change navigation unrelated to the task.

## Validation

- Run `mint dev` from the repository root to preview changes to rendered pages or layout at http://localhost:3000.
- Run `mint broken-links` to check internal documentation links.
- When editing `docs.json`, validate the JSON and check that navigation targets exist and are intended to be public.
- Check README links to local files separately; Mintlify excludes the README from the published site.
- Run `git diff --check` and review the final diff before handing off.
- Report the checks performed and any validation that could not be completed. Local checks do not prove the published site has changed.

## Delivery

- Submit changes through a pull request when requested; do not push directly to the deployment branch.
- Mintlify can publish changes automatically from its configured deployment branch. Treat a merge or push to that branch as a potential production deployment.
- Do not merge or publish without explicit authorization for that action. Complete any review required by the user before an authorized deployment.
