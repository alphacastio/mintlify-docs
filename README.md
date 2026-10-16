# Alphacast documentation

This repository contains the source for [learn.alphacast.io](https://learn.alphacast.io/introduction), the public documentation for [Alphacast](https://www.alphacast.io).

Use the documentation to learn how to manage datasets and repositories, connect data providers, build pipelines, and work with Alphacast through the API, Python SDK, and Model Context Protocol (MCP).

## Read the documentation

- [Get started](https://learn.alphacast.io/introduction)
- [API reference](https://learn.alphacast.io/api/overview)
- [Python SDK](https://learn.alphacast.io/python-sdk/overview)
- [MCP](https://learn.alphacast.io/mcp/overview)
- [Pipeline steps](https://learn.alphacast.io/steps/overview)

## Repository structure

The site uses [Mintlify](https://www.mintlify.com/docs). Pages are MDX files with YAML frontmatter.

| Path | Contents |
| --- | --- |
| `docs.json` | Site configuration, navigation, colors, and navbar links |
| `introduction.mdx`, `quickstart.mdx`, `authentication.mdx` | Getting started guides |
| `concepts/`, `uploading/`, `providers/` | Core concepts, data uploads, and data providers |
| `api/` | HTTP API reference |
| `python-sdk/` | Python SDK guides and reference |
| `mcp/` | MCP setup, tools, and prompting guides |
| `steps/` | Pipeline step documentation |
| `images/` | Documentation images |
| `.mintignore` | Content excluded from the published site |

Some files are retained as unpublished content. Check both `docs.json` and `.mintignore` before adding pages to the site.

## Preview locally

Install Node.js 20.17.0 or later and the [Mintlify CLI](https://www.mintlify.com/docs/cli/install), then run these commands from the repository root:

```bash
npm install -g mint
mint dev
```

Open `http://localhost:3000` to preview the site. Before submitting documentation changes, check internal links:

```bash
mint broken-links
```

## Contribute

Found an error or a missing explanation? [Open an issue](https://github.com/alphacastio/mintlify-docs/issues) or submit a pull request with your proposed change.

Keep changes focused, verify technical examples against the behavior they describe, and preview affected pages. Never include API keys, credentials, or private customer data in examples, screenshots, or issues.

See [CONTRIBUTING.md](CONTRIBUTING.md) for writing guidelines and [AGENTS.md](AGENTS.md) for instructions for coding agents.

## Publishing

Mintlify hosts the documentation and publishes changes from the configured deployment branch. Submit changes through a pull request for review; merging into the deployment branch can update the live site.
