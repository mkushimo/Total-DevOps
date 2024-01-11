Crontab
 
To allow or deny access to specific users, crontab uses the files /etc/cron.allow and /etc/cron.deny. Based on the existence of /etc/cron.allow and /etc/cron.deny files, crontab decides whom to give access to cron in following order.

If cron.allow exists – only the users listed in the file cron.allow will get an access to crontab.
If cron.allow does not exist – all users except the users listed into cron.deny can use crontab
If neither of the file exists – only the root can use crontab
If a user is listed in both cron.allow and cron.deny – that user can use crontab.
crontab -l : To display the cron jobs.
crontab -e : To edit the cron table.

crontab -r : To remove the crontable without confirmation.
crontab -ir: To remove the crontable with confirmation.

To list,schedule or remove cron job for the particular user, use below commands.
#crontab -l -u mithun
#crontab -e -u mithun
#crontab -ir -u mithun

Crontab Format

# Minute   Hour    Day of Month          Month               Day of Week        Command /Script
# (0-59)    (0-23)        (1-31)            (1-12 or Jan-Dec)   (0-6 or Sun-Sat)    /usr/bin/find


Run the cron job every minute.
*/1 * * * *

Run the cron job every 10 minutes.

*/10 * * * *
