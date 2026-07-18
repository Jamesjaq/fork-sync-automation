# Fork Sync Automation

This repository contains a GitHub Action that automatically syncs all your forked repositories with their upstream sources.

## What It Does

- Runs on a schedule (daily by default)
- Syncs all your forks with their upstream repositories
- Updates the default branch with the latest changes from upstream

## How It Works

The workflow uses the GitHub CLI to:
1. List all your forked repositories
2. Sync each fork with its upstream source
3. Force update the default branch if needed

## Configuration

Edit `.github/workflows/sync-forks.yml` to change:
- **Schedule**: Modify the `cron` expression (default: daily at 2 AM UTC)
- **Frequency**: Change from daily to weekly, hourly, etc.

## Requirements

- Your personal access token is automatically available via `secrets.GITHUB_TOKEN`
- The workflow runs with your account permissions

## Schedule

Currently runs: **Daily at 02:00 UTC**

To modify, edit the cron expression in the workflow file.

## Manual Trigger

You can also manually trigger the sync by:
1. Going to the **Actions** tab
2. Selecting **Sync All Forks**
3. Clicking **Run workflow**

## Logs

After each run, check the **Actions** tab to see:
- Which forks were synced
- Any failures or errors
- Summary statistics
