# triggers for workflow

GitHub Actions can be triggered by various events and conditions. Here are some common triggers with examples:

## Push Events

Push events occur when code is pushed to a repository. This is one of the most common triggers for CI/CD workflows.

```yaml
on:
  push:
    branches:
      - main
      - "releases/**"
    paths:
      - "**.js"
```

This workflow will trigger when:

- Code is pushed to the `main` branch
- Code is pushed to any branch starting with `releases/`
- Only `.js` files are modified

## Pull Request Events

Pull request events trigger workflows when pull request activities occur.

```yaml
on:
  pull_request:
    types: [opened, synchronize, reopened]
    branches:
      - main
```

This workflow will trigger when:

- A pull request targeting the `main` branch is opened, synchronized (updated), or reopened.

## Issue Events

Issue events trigger workflows when issue-related activities happen.

```yaml
on:
  issues:
    types: [opened, edited, labeled]
```

This workflow will trigger when:

- A new issue is opened
- An existing issue is edited
- A label is added to an issue

## Manual Triggers

Manual triggers allow you to run workflows on-demand using the GitHub UI or API.

```yaml
on:
  workflow_dispatch:
    inputs:
      environment:
        description: "Environment to deploy to"
        required: true
        default: "staging"
      debug:
        description: "Enable debug mode"
        required: false
        type: boolean
```

This workflow can be manually triggered with:

- A required input to specify the deployment environment
- An optional boolean input to enable debug mode

## Scheduled Events

You can schedule workflows to run at specific times using cron syntax.

```yaml
on:
  schedule:
    - cron: "0 2 * * *"
```

This workflow will run:

- Every day at 2:00 AM UTC

## Repository Dispatch

Repository dispatch events allow external events to trigger workflows.

```yaml
on:
  repository_dispatch:
    types: [deploy, rollback]
```

This workflow can be triggered by sending a POST request to the GitHub API with:

- An event type of either `deploy` or `rollback`

Remember that you can combine multiple event types in a single workflow file, allowing for flexible and powerful automation scenarios.

## Workflow run

Workflow run events trigger based on another workflow's condition

```yaml
on:
  workflow_run:
    workflows:
      - other workflow
    types:
      - completed
```

in this example we say this workflow runs only if the workflow with name of `other workflow` is completed.

remember you cannot chain together more than three levels of workflows using workflow_run

## Exercise

### Objective

Create a GitHub Actions workflow file that incorporates multiple trigger types for a hypothetical web application repository.

### Instructions

1. Create a file named `.github/workflows/web-app-workflow.yml` in your repository.
2. Configure the workflow to trigger under the following conditions:

   a. On push events:

   - To the `main` branch
   - To any branch starting with `feature/`
   - Only when changes are made to `.js`, `.html`, or `.css` files

   b. On pull request events:

   - When a pull request is opened or updated
   - Only for pull requests targeting the `main` branch

   c. On a schedule:

   - Run every day at 1:00 AM UTC

   d. Manually, with the following input parameters:

   - `environment` (required): Options are 'dev', 'staging', or 'production'
   - `run_tests` (optional): A boolean to determine if tests should be run

3. Add a job named "build" that runs on ubuntu-latest.

### Bonus

Add a repository dispatch event trigger that listens for a custom event type named "deploy".
