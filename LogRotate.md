## LogRotate

logRotate is a utility tool in linux.

Rotation, Compression, Deletion.

#logrotate

#yum install logrotate

Config files.

#/etc/logrotate.conf

#/etc/logrotate.d 

Log Files Location.

#/var/log/

#less /etc/logrotate.conf

#cd /etc/logrotate.d 

#ls -ltr

#less firewalld

============

#example

#cd /var/log

#mkdir myapp

#cd myapp

#touch my_app.log

#cd /etc/logrotate.d 

#touch myapp

#vi myaap

/var/log/myapp/*.log{ 
		daily
		size 10M
}

save.


#cd /var/log/myapp/

#ls -lh

#truncate -s 15M my_app.log

how to check log file is correct or not.

#logrotate -d /etc/logrotate.conf

#logrotate /etc/logrotate.conf ===> manually tiger

