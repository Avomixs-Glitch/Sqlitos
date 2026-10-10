<div align="center">

# Sqlitos

### Your database. Your machine. Your momentum.

**A modern, desktop-first workspace for exploring, designing and operating SQLite databases — without giving up control of your data.**

[![Official site](https://img.shields.io/badge/Official%20site-sqlitos.vercel.app-0D1117?style=for-the-badge&logo=vercel&logoColor=white)](https://sqlitos.vercel.app)
[![Desktop first](https://img.shields.io/badge/Architecture-Desktop--first-2DD4BF?style=for-the-badge)](#desktop-first-by-design)
[![Privacy](https://img.shields.io/badge/Data%20model-Local--first-7C3AED?style=for-the-badge)](#your-data-stays-yours)

[Official website](https://sqlitos.vercel.app) · [Releases](../../releases) · [Security](SECURITY.md) · [Feedback](../../issues)

</div>

<a href="https://sqlitos.vercel.app">
  <img src="./assets/sqlitos-workspace-hero.png" alt="Sqlitos: an abstract, local-first database workspace" />
</a>

<br />

> **Sqlitos turns a database file into a workspace.** Inspect the structure, write SQL with confidence, evolve schemas deliberately and keep operations close to the data they affect.

## Table of contents

- [The database workspace, rethought](#the-database-workspace-rethought)
- [Built for the work around data](#built-for-the-work-around-data)
- [Desktop-first by design](#desktop-first-by-design)
- [Your data stays yours](#your-data-stays-yours)
- [Getting started](#getting-started)
- [Product surface](#product-surface)
- [Security](#security)
- [This repository](#this-repository)

## The database workspace, rethought

Working with SQLite is usually fragmented: one tool to inspect tables, another to run queries, a third to understand relationships, and a collection of scripts for everything operational.

Sqlitos brings that work into one focused desktop experience. It is for developers, product builders and data-minded teams who need a fast path from **“What is in this database?”** to **“I understand it, I changed it safely, and I can explain what happened.”**

| From | To |
| --- | --- |
| Opening a file and guessing its shape | A navigable schema, relationships and operational context |
| One-off SQL and scattered scripts | A deliberate workspace with history, snippets and query tools |
| Risky schema changes | Inspectable diffs, migrations and database-aware guardrails |
| Local data hidden behind opaque files | A product experience built around visibility and control |

## Built for the work around data

### `01` Understand

Start with the structure. Explore tables, columns, foreign keys, indexes, views and triggers in a visual workspace designed to make unfamiliar databases legible.

### `02` Ask

Use a dedicated SQL editor with history, reusable snippets, result exploration and query-plan tooling. The goal is not merely to execute SQL — it is to understand its effect.

### `03` Shape

Design tables, compare schemas and prepare migrations from the same place where you inspect the current state. Schema work becomes a reviewable workflow rather than a leap of faith.

### `04` Operate

Move from development into confidence: integrity and health checks, PRAGMA inspection, backups, import/export, storage visibility and change-oriented diagnostics.

## Product surface

| Explore | Query | Build | Operate |
| :--- | :--- | :--- | :--- |
| Schema map | SQL editor | Table designer | Health monitor |
| Database browser | Query history | Migrations | Backups |
| Tables & relations | Query plans | Schema diff | Import / export |
| Storage view | Snippets | Indexes & triggers | PRAGMA controls |

<details>
<summary><strong>More capabilities in the workspace</strong></summary>

<br />

- Full-text search with SQLite FTS5
- Vector and embedding-oriented workflows
- Auto API and optional realtime capabilities
- Optional remote database connection
- Scheduled operations and notification-oriented tooling
- Authentication, role-aware controls and security-audit views

</details>

## Desktop-first by design

```mermaid
flowchart LR
  DB[(Your SQLite file)] <-- direct local access --> APP[Sqlitos Desktop]
  APP --> EXP[Explore]
  APP --> SQL[Query]
  APP --> SCH[Design]
  APP --> OPS[Operate]
  APP -. opt-in .-> CLOUD[Cloud services]
  APP -. optional .-> REMOTE[Remote server]
```

The local desktop app is the centre of Sqlitos. A server is not required to open and work with a SQLite file. Optional cloud and remote-server capabilities are additive: they support workflows that need them without redefining the local experience.

## Your data stays yours

Sqlitos is designed around a simple premise: **a local database should remain local unless you explicitly decide otherwise.**

- Open a SQLite file directly from your machine.
- Keep local exploration and SQL work independent of a hosted database service.
- Configure remote connections, backups or cloud features intentionally when your workflow calls for them.
- Keep secrets out of issues and public repositories.

## Getting started

### Discover Sqlitos

Visit [sqlitos.vercel.app](https://sqlitos.vercel.app) for the official product experience and current product information.

### Install the desktop app

When a version is available, download the installer for your platform from [Releases](../../releases):

| Platform | Distribution |
| --- | --- |
| Windows | `.exe` installer |
| macOS | `.dmg` disk image |
| Linux | AppImage |

Then open Sqlitos, choose a SQLite file and begin with the schema explorer.

## Security

Sqlitos uses a layered approach appropriate to desktop database work:

- isolated and sandboxed Electron renderer processes;
- explicit IPC boundaries between the interface and local system operations;
- runtime validation at application and server boundaries;
- bearer-token protection and restrictive CORS defaults for the optional remote server.

Please do not disclose vulnerabilities in public issues. Read [SECURITY.md](SECURITY.md) for responsible reporting.

## This repository

This is the official public home for the **Sqlitos product**: its positioning, public documentation, release notes and feedback.

The application source code is intentionally not published here. This keeps product code, development infrastructure and sensitive implementation details separate from the public product experience.

### Share feedback

Have a workflow Sqlitos should make easier? [Open an issue](../../issues) with the context, the desired outcome and — when reporting a defect — the version and steps to reproduce.

For documentation contributions and public feedback guidelines, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

<div align="center">

Built for people who want to move fast **without moving their data away**.

<a href="https://sqlitos.vercel.app"><strong>Explore Sqlitos →</strong></a>

</div>

