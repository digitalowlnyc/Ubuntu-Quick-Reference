# QUICK REFERENCE: Cron

## General

- Cron runs with a limited env. You can `source "$HOME/.profile"` to help get around this. 

## Logging and Notifications

- Cron does not get logged by default (verified=16.04). To enable logging, edit settings in `/etc/rsyslog.d/50-default.conf
`

- If turned on, Cron will log to `/var/log/rsyslog` with the label `CRON`

- Cron will send an email with the output of a command to the root user **unless** you put the following in your crontab:
```
MAILTO=""
```
