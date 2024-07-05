# What is cron?
cron is a time-based job scheduler in Unix-like operating systems. It allows users to schedule scripts or commands to run automatically at specified intervals (e.g., daily, weekly, monthly). cron jobs are used for automating repetitive tasks such as system maintenance, backups, and monitoring.

## Components of cron:
### crontab:

A crontab (cron table) is a file containing a list of commands to be executed at specified times.

Each user can have their own crontab, and there is also a system-wide crontab.

The crontab file follows a specific format to specify the schedule.

### cron Daemon:

The cron daemon is a background process that runs continuously and checks the crontab files for scheduled jobs.

It executes the commands at the times specified in the crontab.

## What is /etc/cron.allow?
/etc/cron.allow is a file that specifies which users are allowed to use the cron service to schedule jobs. If this file exists, only the users listed in it are permitted to schedule cron jobs.

## What is /etc/cron.deny?
/etc/cron.deny is a file that specifies which users are not allowed to use the cron service to schedule jobs. If this file exists, users listed in it are prohibited from scheduling cron jobs.
