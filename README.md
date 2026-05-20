# OpenSpec-Ready Next.js Blank Template

A minimal Next.js starter pre-configured with an OpenSpec `config.yaml`, ready to drop into an AI-assisted spec-driven development workflow.

This repo is the companion template for the Medium post:
**[Spec Kit vs. OpenSpec: I Built the Same App Twice to Find Out](https://medium.com/@raphaellondner/spec-kit-vs-openspec-i-built-the-same-app-twice-to-find-out-0fcdcfa08b46)**

---

## What is this?

This is a blank Next.js 16 application with several additions: 
- OpenSpec-initialized commands for Claude, Codex, Gemini and GitHub Copilot (OpenSpec v1.2)
- an `openspec/config.yaml` file that configures the project for spec-driven development. It is the starting point demonstrated in the blog post above.

The template is intentionally empty on the application side — the point is the OpenSpec configuration and how it shapes AI-assisted development from the very first prompt.

## Stack

| Layer | Technology |
|---|---|
| Framework | Next.js 16 (App Router) |
| Language | TypeScript (strict) |
| Styling | Tailwind CSS v4 + shadcn/ui |
| Database | PostgreSQL via Next.js API routes |
| Package manager | pnpm (workspace, root `node_modules`) |

## Quick Start

> Dependencies are resolved from the monorepo root (`doit_root`), two folders up. Run installs from there, not from this directory.

```bash
# From the monorepo root
pnpm install

# Start the dev server (runs on port 3002)
pnpm --filter doit_openspec_startup_template dev
```

## OpenSpec Configuration

The file that matters is [`openspec/config.yaml`](openspec/config.yaml). It tells your AI agent:

- The tech stack and storage conventions
- Which artifact rules to follow (proposals include a rollback plan, specs use Given/When/Then, complex flows get sequence diagrams)
- That this project uses a spec-driven schema (`schema: spec-driven`)

Edit this file to match your own project context before you start building.

## How it relates to the blog post

The blog post walks through using this template as a foundation for a spec-driven feature build — from writing the OpenSpec config to generating proposals, specs, and tasks with an AI agent, through to implementation.

Start here, read the post, and fork this template when you want to follow along.

---

> Part of the [DoIt](https://github.com/milissai/doit_root) monorepo template collection.
