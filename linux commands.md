#### How to display name of current logged in user?
#whoami

#### how to check system date or time ?
#date 
#date %D

#### how to display files and directory present in current location
#ls
#ls -lt

#### how to clear the termnal
#clear
#clt+l

#### how to display content of a file on terminal
#cat (file name)

#### how to read a file and search for a word
#less (file)

#### How to read a file and search for a word
#more (file)

#### how to create file 
#touch

#### how to delete 
rm (file)

#### how to edit a file in linux
#vi (file)
#nano(file)

#### how to create a directory
mkdir (newfolde)
 
#### how to delete a directory
rmdir (dirname)


#### how to change path or move to another folder in linux
#cd /path/folder
#cd ..

#### how to check syntax and options available for a command 
#help
ex ls --help
   ls --help | more

#### how to read or get mor info about a command
#man means -manuall
#ex  ls man 

#### how to check which executable is using for a command
#which
#ex:which ls

#### how to use calculater in linux
#bc

#### how to check calender of last year in linux
#cal

#### how to check how  long server has been running in linux
#uptime 


#### how to record your activity on terminal in a file
#script
clt +d--> to exit the script terminal
and it will create one file defalt name of file typescript


#### How to create a file a short-cut of a long command in linux
#alias l="ls -ltr"

ex ls -ltr
  alias l="ls -ltr"

=================================
Zip and unzip of files and folder
=================================
#### how to compress a file in linux
#gzip -k file

#### how to decompress a file in linux
#gzip -d file
#gunzip file

#### how to compress a folder in linux
#tar -czf myfile.tar.gz myfiles/

#### how to decompress a file in linux  
#tar -xzf myfile.tar.gz

#### how to compress multiple files in one zipped file in linux
#zip myfles.zip file1 file2

#### how to unzip
#unzip myfiles.zip

#### how to list files in zipped file
#unzip -l myfiles.zip

#### how to download a file from internet
#wget URL_of_file
#wget -O opt_file.txt URL_of _file

#### how to call an API on linux
#curl http://numbersapi.com/random

#### how to install an application on linux
#apt or yum/dnf

ex yum install nginx

#### how to check if an application is installed or not on linux
#rpm -qa | grep app
rpm means redhat package manger
#dnf list installed

#### how to list available packages to install on linux
#apt search <package-name>
#yum/dnf list available

ex-- yum list available | grep java

#### how to start/stop a service on linux
#systemctl start service_name
#systemctl stop service_name


#### how to list all services on linux
#systemctl list-units --type=service --all

#### how to list all existing environment variable on linx
#printenv

#### how to add a new environment variables linux
#export JAVA_HOME="/usr/lib/jvm/java_version"
#export PATH=$JAVA_HOME/bin:$PATH

#### how to add a new environment variables permanently on linux
#source ~/ .bash_profile

#### how to print a specific column from a CSV file
#awk -F , '{print $2}' file.csv


#### How to display starting two characters of all line
#cut -c1-2 file.txt


#### how to display a specific line from a file
#sed -n '5p' file.txt

#### hows to replace a specific word within afile
#sed -n 's/from/to/g' file.txt

