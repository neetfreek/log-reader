# Log Reader

Read, parse, write selected log files' issues.

## Overview

Reads logs files for issues, copying log files if issues found. Also writes only issues and counts found from given 
log files - all time stamped for collection and organisation purposes.  Issues found are written to `./logs`. See 
the first example for default (no flags) behaviour.

Files to parse, directories for files, and issues to look for can be set by
passing flags (-f, -d, -k respectively).

Execute python3 log_reader.py for help.

## Examples

- `python3 log_reader.py`: check boot.log, messages, auth.log, daemon.log, kern.log in /var/log for mentions of 
  "error", "failed", "warning", case-insensitive

- `python3 log_reader.py -f boot.log -k error`: check boot.log in /var/log for mentions of "error", case-insensitive

- `python3 log_reader.py -d /example -f boot.log,test.log -k error,warning`: check boot.log and test.log in /example 
  for mentions of "error" and "warning", case-insensitive