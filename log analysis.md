## LOGS Analysis and monitoring

### what are log files.

A log file stores events, processes, messages, and other data from applications operating systems, or devices.

They provide information based on the action performed by users, playing an important role in monitoring.

Log directory in linux.

#/var/log

#cd /var/log

In side this file we get so many log files.

some of the important files.

boot, chron, secure, maillog, httpd, messages.

#ls 

#less filename

#tail -f cron --latest log

#tail -f secure

#less messages

#cd httpd/

#less error_log

#grep -i "error" error_log

#cat error_log | grep -i "error"

forward a log to any file.

#cat error_log | grep -i "error" > logs_anaylysis

#ls


