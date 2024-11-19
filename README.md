# Job Scheduler Repository

## Overview

The Job Scheduler Repository is designed to facilitate the scheduling and execution of R scripts across multiple repositories and branches. This system allows team members to populate a job queue, which the scheduler reads and executes accordingly. The implementation ensures that jobs are run in the correct context, with appropriate error handling and logging.

## Features

- **Dynamic Job Queue**: Team members can add jobs to a text file, specifying the repository name, branch name, and script to execute.
- **Error Handling**: Robust error handling mechanisms are in place to manage script failures and notify relevant stakeholders.
- **Logging**: Execution logs are maintained for tracking job performance and troubleshooting.
- **Slack Notifications**: Real-time notifications are sent to Slack channels regarding job status updates.

## Adding Jobs to the Queue

To add a job to the queue, append a line to Wachtrij.txt located in the NETWORK_DIR. The line should follow this format:

repo_name|branch_name|script_path

This should be handled by the function `schedule_job()`.

## Logging and Notifications

Execution logs will be saved in the logs/ directory. Additionally, notifications regarding job execution status will be sent to the specified Slack channel.

## Error Handling

If a script fails during execution, an error message will be logged, and a notification will be sent via Slack. Review logs for detailed error information.

## Contribution Guidelines

Feel free to contribute by suggesting improvements or reporting issues. Please ensure that any changes are well-documented.
