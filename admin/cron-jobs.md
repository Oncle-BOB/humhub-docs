Cron Job Setup
=======

The following guides are meant to help you with your Cron Job setup, since those settings are highly dependent on your actual environment we can't assure those setting will work for your.

> Note: Make sure to use the right [php cli executable](http://php.net/manual/en/features.commandline.introduction.php) for your jobs!

### CloudLinux (CentOS) 6
The following is a default setup for CloudLinux (CentOS) 6 and may not work for all users.

```
/usr/local/bin/php /home/USERNAME/public_html/WEB-DIRECTORY/protected/yii cron/hourly >/dev/null 2>&1

30 * * * *

/usr/local/bin/php /home/USERNAME/public_html/WEB-DIRECTORY/protected/yii cron/daily >/dev/null 2>&1

00 18 * * *
```

### cPanel Hosted Server
The following is a default setup for cPanel Hosted Server and may not work for all users.

```
php-cli /home/USERNAME/public_html/WEB-DIRECTORY/protected/yii cron/hourly >/dev/null 2>&1

0,30 * * * *

php-cli /home/USERNAME/public_html/WEB-DIRECTORY/protected/yii cron/daily >/dev/null 2>&1

00 0,12 * * *
```

### IIS Windows Server
Using [Schtasks](https://technet.microsoft.com/en-us/library/cc725744.aspx) would be recommended over many other options for Windows 2012 and Windows 8 users.

`Example TBA`

### Plesk
Refer to this [post](https://stackoverflow.com/questions/16700749/setting-up-cron-task-in-plesk-11)

![](http://i.imgur.com/TbWEsjC.png)

### OVH
This [procedure](https://github.com/humhub/humhub/issues/2718#issuecomment-330910142) based on php 5.6 (adapt to your PHP version). For details on the task manager cron ovh [Follow this link](https://www.ovh.com/us/g1990.hosting_automated_taskscron)!

Based on the official [humhub documentation](http://docs.humhub.org/admin-installation-configuration.html) you need to get something similar to this <a href="https://www.hostingpics.net/viewer.php?id=390363cron.jpg"><img src="https://img11.hostingpics.net/thumbs/mini_390363cron.jpg" alt="Heberger image" /></a>

### Debian
Please read up on this [article](https://debian-administration.org/article/56/Command_scheduling_with_cron).

`Example TBA`

### Ubuntu
Please read up on this [how-to guide](https://help.ubuntu.com/community/CronHowto).

`Example TBA`

### Other Server(s)
`TBA`

### *IMPORTANT NOTICE*
*This guide is subject to changes and all information provided are for example use, it is best to speak with your service providers about how best to setup your Cron Jobs with their services.*
