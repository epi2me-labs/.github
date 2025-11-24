# Reusable Workflows

This directory contains reusable GitHub Actions workflows that can be used across all epi2me-labs repositories.

## Issue Auto-Reply Workflow

The `issue-autoreply.yml` workflow automatically replies to newly opened issues with a support message.

### Usage

To use this workflow in any epi2me-labs repository, create a workflow file (e.g., `.github/workflows/issue-autoreply.yml`) with the following content:

```yaml
name: Issue Auto-Reply

on:
  issues:
    types: [opened]

jobs:
  auto-reply:
    uses: epi2me-labs/.github/.github/workflows/issue-autoreply.yml@main
```

This will automatically add a comment to all newly opened issues directing users to the appropriate support channels.
