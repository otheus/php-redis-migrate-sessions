## Changelog : php-redis-migrate-sessions 

* 2019-12-09 *otheus* Refactor
  * Command-line argument now dictates direction of php session directory or file (only one at present)
  * Program is no longer re-entrant: find pipes to a while-loop which invokes redis-cli for each session
  * DRYRUN environment variable, if set, will disable execution of redis-cli and only output what would have been sent to it
  * VERBOSE tells the user of the progress
  * These "options" are set on the command-line as follows `DRYRUN=1 VERBOSE=1 php-redis-migrate-sessions /var/lib/php/sessions`
  
* 2013-02-15 *cavallari* Initial version
