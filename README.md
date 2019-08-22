Day 1:

ls: lists directories
cd : switch directories
pwd: displays the current directory
mkdir: creates a new directory
rmdir: remove an empty directory
cp: copy files or directories
rm: remove file or directory
mv: move files and directories, or change the names of files and directories



ls: lists directories:

-a: all the files, together with hidden files (files beginning with.).
-d: list only the directory itself, not the file data in the directory (usually)
-l: long data string listing, including file attributes, permissions and other data; (common)


ls -l 
ls -ld
ls -a

###############


cd : switch directories

examples:
Use the mkdir command to create the runoob directory
 mkdir runoob  # create dir named runoob

Use the absolute path to switch to the runoob directory
 cd /root/runoob  # change to dir /root/runoob

Use the relative path to switch to the runoob directory
cd -  # change to the dir to last dir you have changed 

# means to go back to your home directory, which is /root
cd  ~   # change to home dir for current user

# means to go to the current directory, which means to go to /root directory;
 cd ..  # change to upper dir

##########

pwd: displays the current directory
mkdir: creates a new directory

-m: permissions for configuration files! Direct configuration, do not need to see the default permissions (umask) face ~
-p: to help you directly create the required directory (including the directory above) recursively!
 mkdir -p /test/hhh  # create two dirs and one belones to another

rmdir: remove an empty directory
rmdir dirname  # remove a dir named dirname
 
##################

cp: copy files or directories

cp file1 file2  # copy the content of file1 to file2
cp file1 /mnt/files  # copy file named file1 to  /mnt/file

rm: remove file or directory

rm  file  #just remove a file 

rm -fr dirname  # force remove a dir named dirname
rm -fr file    # force remove a file named file


mv: move files and directories, or change the names of files and directories

mv file1 /mnt  # move file named file1 to /mnt dir
mv file1 file2 #rename file1 to file2 ,and it can be rename dir


#### some userful commands you may know ##### 
more
less 
vi
vim 
cd 
pwd
ls
su
passwd 
chgrp 
chown 
mv 
cp 
touch
mkdir 
rm 
ssh uername@x.x.x.x -p port 
ifconfig  -a
ip addr show eth0

#####################################










Day 2:

init     # system run level
Commands:
  0              Power-off the machine. init 0
  6              Reboot the machine     init 6
  2, 3, 4, 5     Start runlevelX.target unit  init 2/3/4/5
  1, s, S        Enter rescue mode   init 1
init 0/3/5/6     basiclly you should know 

date   # show date
date "+%Y~%m~%d %H-%M-%S"  # show date or time in custom format
wget http://url         ##download something from the url
curl -o/O  http://url   ##download something from the url

ps: to see process on the system
 To see every process on the system using standard syntax:
          ps -e
          ps -ef
          ps -eF
          ps -ely

 To see every process on the system using BSD syntax:
          ps ax
          ps axu

 
netstat -altnp |grep 22
ss -anlpe 
kill -9 pid  
uname -n/r/o

uname --help # when you meet a command you don't know how to use it you should to know use '--help' or 'man uname ' to help you 






Day 3:

# to check server cpu infomation
lscpu 
/cat /proc/cpuinfo 

# The top command can view the overall operation of the system timely and dynamically. It is a utility tool integrating multi-party information monitoring system performance and operation information

top

# to check disk usage 
df -hm 
df -hT

# to check memory usage
free -hm

# kill all process by force related to specific process 

killall -9 [process name]   
killall5 -9 [process name]

eg : killall -9 httpd  # kill all process by force related to httpd 
	 kill -9 httpd     # kill main process by force named httpd 

# The uname command is used to print information about the current system (kernel version number, hardware architecture, host name, operating system type, and so on)

uname -a  # print all info 
uanme -n  # print node name 
uname -o  # print operating-system type 
uanme -r  # print kernel version 

#The uptime command prints how long the system has been running and the average load on the system. The uptime command displays the following information: the current time, how long the system has been running, how many users are currently logged in, and the average load of the system over the past 1 minute, 5 minutes, and 15 minutes.

uptime 

##
who   # which user and which session using by user 
##
last   #last time who logged into the system successfully 
lastb  #last time who logged into the system falied 

# wc is a tool to count some info you want from input 

wc -l  # to count lines from input 
wc -w  # to count how many words from input 
