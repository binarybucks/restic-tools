# restic-tools
Wrapper around restic backup to simplify certain tasks. 
Repositories can be configured in `/etc/backup/$REPO.repo`. 
Local includes and excludes in `/etc/backup/local.config` or `/etc/backup/local.exclude`

* `backup $REPO local` for local backup to repo configured by 
* `backup $REPO monitor $HOST $WARN_HOURS $CRIT_HOURS` for Nagios/Icinga checks of backups
* `backup $REPO $ARGUMENTS` for invoking restic with $ARGUMENTS for the repository

In `local.config`:
* `BACKUP_HOSTNAME` is the name your host will show up as in restic
* `BACKUP_DIR` is the root of the directory you want to back up
* `HEALTHCHECK_URL` is an optional URL to [healthchecks.io](https://healthchecks.io/checks/) (comment out if you don't need it)
