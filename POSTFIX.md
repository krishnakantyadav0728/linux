## POSTFIX

### How to send emails using email smtp

#### installation

check first already it is installed or not.

#rpm -qa | grep postfix

#rpm -qa | grep mailx

#yum install postfix

#yum install mailx


POSTFIX configuration.

#cd /etc/postfix/main.cf

#cd /etc/postfix

#ls -ltr

main.cf -->in this file we need to make changes.

recomndation- we need to take backup.

#cp main.cf main.cf_bkp

#vi main.cf

Add the following lines.

relayhost = [smtp.gmail.com]:587

myhostname= <your_hostname>

#hostname -f 


Location of sasl_passwd we saved.

smtp_sasl_password_maps = hash:/etc/postfix/sasl/sasl_passwd

Enables SASL authentication for postfix.

smtp_sasl_auth_enable = yes

smtp_tls_security_level = encrypt

Disallow methods that allow anonymous authentication.

smtp_sasl_security_options = noanonymous


Create a file under /etc/postfix/sasl/

#pwd

#mkdir sasl

#cd sasl/

#touch sasl_passwd

### How to genrate password.

go to gmail ->manage your google Account -> security-> go to search bar-> search apps password->

inside app passwords ->select app ->select other and smtp ->genrate app password ->copy the passwd and use the passwd.


#vi sasl_passwd

In side this file we need to add password.

[smtp.gmail.com]:587 example@gmail.com:password

convert the sasl_passwd file into db file.

#postmap sasl_passwd

#ls -ltr

#chmod 600 * to change the permission

start the postfix service.

#systemctl start postfix.service

#systemctl status postfix.service

### how to send email.

#echo "Test Mail from  sun" | mail -s "sun" example@gmail.com 

#echo "Test Mail from  sun" | mail -s "sun" -a testfile example@gmail.com 









