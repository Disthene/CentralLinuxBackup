# CentralLinuxBackup
A tool to centralize backups of all your Linux environements on one and unique server.

## Prerequisites
Install python 3
```
sudo apt-get install python3-pip python3-pyqt5
```
Install and update setup tools
```
pip install --upgrade setuptools
```
Install crontab for python3
```
python3 -m pip install python-crontab
```
Use a svc account on your machines.

## Installing

Extract the folder "backup" in /etc for example on your central server.

```
/etc/backup
```

## How to run

```
sudo python3 /etc/backup/Backup.py
```

##### Add a new Backup

To add a backup press "n" once you started the tool. 

First you'll be prompt to enter the name, or IP of the server. I do not handle errors there so take care for the moment. I just check if the server exists or not.

Second enter the path of the folder you want to backup. Again here I don't handle errors, and do not verify yet if the path exists.

Third is the repetition of your backup, here I use Cron so for the moment it's not possible to plan a backup at a specific time, but only to schedule it each X hours.

##### Delete a backup

To delete a backup press "d" once you started the tool.

You'll be prompt to enter the name of the server you want to delete. Notice it will move all current backup configured on this server. If you want to remove a specific folder do it manually by removing the script created in /etc/backup/yourserver/yourserver+dateyouplannedit.py and remove the line in config file.

A way to remove specific folders from planned backup will be added in the next versions.

##### Check current backups

To check the current backup configured press "c" once you started the tool. It will display the current config file. Notice that this config file is only here for displaying config, at the moment you can't configure back up through this file.

###### Best practice

Always leave the tool using "q" to log the changes.

## Built With

* [pyzo](http://pyzo.org/) 

## Versioning

Ver 1.0 

Current Version

Coming Ver 1.1 

Will add the possibility to remove specific folders

Will add the possibility to remove automatically the backups older than X days


## Authors

* **Cedric MATTHIS** - *Initial work* 

See also the list of [contributors](https://github.com/Disthene/CentralLinuxBackup/contributors) who participated in this project.

##### If you want to contribute feel free, all lines are commented. Let me know your improvements ;)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

