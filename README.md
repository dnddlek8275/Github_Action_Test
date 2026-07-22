# GitHub Actions Test

A focused sandbox for learning how GitHub Actions reacts to pushes on the `main` branch.

The repository contains two small workflows: one verifies that a push can trigger a runner, while the other demonstrates repository-level environment variables and a multi-step job using a StarCraft-themed unit-production scenario.

## What This Repository Demonstrates

- Triggering workflows on pushes to `main`
- Running jobs on GitHub-hosted `ubuntu-latest` runners
- Defining workflow-level environment variables
- Reusing environment variables across multiple shell steps
- Following job output from the Actions tab

## Workflows

| Workflow | Trigger | Purpose |
| --- | --- | --- |
| `push_trigger.yml` | Push to `main` | Runs a single shell step confirming that the push triggered the workflow |
| `unit_production.yml` | Push to `main` | Runs a three-step unit-production scenario using shared environment variables |

The unit-production workflow defines values for a commander, unit, mineral cost, and voice line. Each step reads those values through the GitHub Actions `env` context and prints the current stage of the scenario.

## Repository Structure

```text
.
├── .github/
│   └── workflows/
│       ├── push_trigger.yml
│       └── unit_production.yml
├── test_gitaction
└── test_hello
```

The two text files are lightweight files used while testing commits and push-triggered workflow runs.

## Try It

1. Make a change to any tracked file.
2. Commit the change.
3. Push the commit to `main`.
4. Open the repository's **Actions** tab.
5. Inspect the logs for **Push Trigger Action** and **Unit Production**.

## Current Scope

This is a workflow-learning repository. It does not contain an application, automated test suite, build pipeline, or deployment configuration.
