# Sqlitos product guide

Sqlitos is a desktop workspace for people who need to understand and operate SQLite databases with more context than a one-off query window can provide.

It combines exploration, SQL work, schema design and routine operations around the database file itself. The aim is simple: make the state of a database easier to see, the effect of a change easier to judge, and the next action easier to choose.

> **Capability note:** availability can depend on how a database is opened. Direct local files unlock desktop-specific operations; remote and optional cloud-connected workflows are additive, not required for everyday SQLite work.

## The product surface

| Area | What you can do | Typical outcome |
| --- | --- | --- |
| **Explore** | Browse tables, columns, rows, views, indexes, triggers and foreign keys. Visualize relationships and inspect storage. | Understand an unfamiliar `.sqlite` file without reconstructing it by hand. |
| **Query** | Run SQL, format statements, inspect results, reuse snippets, revisit history and inspect a query plan. | Turn an investigative question into a measured query. |
| **Design** | Build tables with columns, constraints, foreign keys and checks. Compare schemas and create a migration draft. | Change a schema with the current structure in view. |
| **Migrate** | Maintain versioned migrations, apply them transactionally and use recorded down SQL when supplied. | Keep schema changes explicit and reviewable. |
| **Operate** | Run integrity and foreign-key checks, inspect PRAGMAs, manage backups, import/export data and review activity. | Treat the database as an operating system, not just a file. |
| **Search & AI-ready data** | Create and query FTS5 indexes; build local embedding collections and run similarity search. | Make text-heavy data more discoverable without leaving the workspace. |

## A practical session

### 1. Establish the shape

Open a database and start with the schema view. Identify tables, foreign keys, indexes and triggers. Move to the database browser only once the data model makes sense.

### 2. Investigate without losing the thread

Use the SQL workspace for the question at hand. Query history and snippets preserve useful work; query-plan tooling helps reveal costly scans, joins or missed indexes before a query becomes habitual.

### 3. Change with a visible boundary

Use the table designer for a constrained change, or the schema-diff workspace to compare two real database files. Sqlitos can generate migration SQL, and it explicitly marks changes that need manual SQLite rebuild work rather than pretending every difference is safe to automate.

### 4. Close the loop

Validate the database with health checks, take a backup before a material operation, and review operational activity. For repeat work, scheduled SQL and managed backup jobs can keep a routine from becoming an afterthought.

## Connection modes

| Mode | Designed for | Notes |
| --- | --- | --- |
| **Local SQLite file** | Primary desktop workflow. | Open and work with the file on your machine. Desktop-only operations such as local backups are available in this mode. |
| **Remote connection** | Teams or environments where the database lives behind a service. | Adds a connection path without making a hosted service a requirement for the core product. |
| **Optional connected services** | Authentication, scheduled operations, cloud backup destinations or collaboration-oriented workflows. | These are opt-in extensions. The local desktop experience remains the foundation. |

## Safety by product design

Sqlitos keeps high-impact database actions visible:

- schema diffs separate safe automation from changes requiring manual review;
- applied migrations are recorded and run within a transactional boundary;
- a migration can carry explicit rollback SQL rather than implying an undo exists;
- integrity, foreign-key and journal-mode signals are available in the health workflow;
- backups are a first-class operation, not an external footnote;
- the desktop app isolates renderer processes and uses explicit IPC boundaries for local operations.

## Keyboard-first, without hiding the UI

The workspace includes a command palette, page navigation history, saved workspaces and a shortcut reference. Keyboard flow is useful when you already know the target; the product still keeps key database state visible for the moment when you do not.

## What Sqlitos is not

Sqlitos does not require moving a SQLite file into a cloud service just to inspect it. It also does not disguise irreversible work as a harmless click. The product is intentionally opinionated about keeping data close, actions inspectable and operational context available.

## Next step

Visit [sqlitos.vercel.app](https://sqlitos.vercel.app) for the product site, or watch the [Releases](../releases) page for desktop builds.
