[[shell]]
ciencat@SanYe_Uonlra:~$ cd /tmp
ciencat@SanYe_Uonlra:/tmp$ cd /missing
-bash: cd: /missing: No such file or directory
ciencat@SanYe_Uonlra:/tmp$ cd missing
ciencat@SanYe_Uonlra:/tmp/missing$  echo '#!/bin/sh' > semester
ciencat@SanYe_Uonlra:/tmp/missing$ echo "curl --head --silent
> https://baidu.com" >> semester
ciencat@SanYe_Uonlra:/tmp/missing$ cat semester
#!/bin/sh
curl --head --silent
https://baidu.com
ciencat@SanYe_Uonlra:/tmp/missing$ ./semester
-bash: ./semester: Permission denied
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 nre.txt
-rw-r--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ sudo ./semester
[sudo] password for ciencat:
Sorry, try again.
[sudo] password for ciencat:
Sorry, try again.
[sudo] password for ciencat:
sudo: ./semester: command not found
ciencat@SanYe_Uonlra:/tmp/missing$ curl
curl: try 'curl --help' or 'curl --manual' for more information
ciencat@SanYe_Uonlra:/tmp/missing$ curl --head --silent
curl: no URL specified!
curl: try 'curl --help' or 'curl --manual' for more information
ciencat@SanYe_Uonlra:/tmp/missing$ sudo apt install curl
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
curl is already the newest version (7.81.0-1ubuntu1.10).
curl set to manually installed.
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
ciencat@SanYe_Uonlra:/tmp/missing$ curl
curl: try 'curl --help' or 'curl --manual' for more information
ciencat@SanYe_Uonlra:/tmp/missing$ sudo snap install curl  # version 7.86.0, or
Interacting with snapd is not yet supported on Windows Subsystem for Linux 1.
This command has been left available for documentation purposes only.
ciencat@SanYe_Uonlra:/tmp/missing$ curl --head --silent https://baidu.com
HTTP/1.1 302 Moved Temporarily
Server: bfe/1.0.8.18
Date: Fri, 05 May 2023 07:35:56 GMT
Content-Type: text/html
Content-Length: 161
Connection: keep-alive
Location: http://www.baidu.com/

ciencat@SanYe_Uonlra:/tmp/missing$ curl --help
Usage: curl [options...] <url>
 -d, --data <data>          HTTP POST data
 -f, --fail                 Fail silently (no output at all) on HTTP errors
 -h, --help <category>      Get help for commands
 -i, --include              Include protocol response headers in the output
 -o, --output <file>        Write to file instead of stdout
 -O, --remote-name          Write output to a file named as the remote file
 -s, --silent               Silent mode
 -T, --upload-file <file>   Transfer local FILE to destination
 -u, --user <user:password> Server user and password
 -A, --user-agent <name>    Send User-Agent <name> to server
 -v, --verbose              Make the operation more talkative
 -V, --version              Show version number and quit

This is not the full help, this menu is stripped into categories.Use "--help category" to get an overview of all categories.
For all options use the manual or "--help all".
ciencat@SanYe_Uonlra:/tmp/missing$ man chmod
ciencat@SanYe_Uonlra:/tmp/missing$ chmod -c u+x semester
mode of 'semester' changed from 0644 (rw-r--r--) to 0744 (rwxr--r--)
ciencat@SanYe_Uonlra:/tmp/missing$ ./ semester
-bash: ./: Is a directory
ciencat@SanYe_Uonlra:/tmp/missing$ sh -l semester
curl: no URL specified!
curl: try 'curl --help' or 'curl --manual' for more information
semester: 3: https://baidu.com: not found
ciencat@SanYe_Uonlra:/tmp/missing$
ciencat@SanYe_Uonlra:/tmp/missing$ ls
newfile  nre.txt  semester
ciencat@SanYe_Uonlra:/tmp/missing$ cd ..
ciencat@SanYe_Uonlra:/tmp$ ls
missing
ciencat@SanYe_Uonlra:/tmp$ cd ..
ciencat@SanYe_Uonlra:/$ ls
bin       dev   init   lib64   mnt   root  snap  tmp
boot      etc   lib    libx32  opt   run   srv   usr
brighter  home  lib32  media   proc  sbin  sys   var
ciencat@SanYe_Uonlra:/$ ls -l
total 1408
lrwxrwxrwx  1 root root       7 Apr 19 05:35 bin -> usr/bin
drwxr-xr-x  1 root root    4096 Apr 18  2022 boot
-rw-r--r--  1 root root       2 May  5 15:09 brighter
drwxr-xr-x  1 root root    4096 May  5 14:36 dev
drwxr-xr-x  1 root root    4096 May  5 14:36 etc
drwxr-xr-x  1 root root    4096 May  3 20:21 home
-rwxr-xr-x  1 root root 1440152 May  3 19:39 init
lrwxrwxrwx  1 root root       7 Apr 19 05:35 lib -> usr/lib
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib32 -> usr/lib32
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib64 -> usr/lib64
lrwxrwxrwx  1 root root      10 Apr 19 05:35 libx32 -> usr/libx32drwxr-xr-x  1 root root    4096 Apr 19 05:35 media
drwxr-xr-x  1 root root    4096 May  3 20:05 mnt
drwxr-xr-x  1 root root    4096 Apr 19 05:35 opt
dr-xr-xr-x  9 root root       0 May  5 14:36 proc
drwx------  1 root root    4096 Apr 19 05:36 root
drwxr-xr-x  1 root root    4096 May  5 15:08 run
lrwxrwxrwx  1 root root       8 Apr 19 05:35 sbin -> usr/sbin
drwxr-xr-x  1 root root    4096 Apr 19 05:36 snap
drwxr-xr-x  1 root root    4096 Apr 19 05:35 srv
dr-xr-xr-x 12 root root       0 May  5 14:36 sys
drwxrwxrwt  1 root root    4096 May  5 15:35 tmp
drwxr-xr-x  1 root root    4096 Apr 19 05:35 usr
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/$ ls -all
total 1408
drwxr-xr-x  1 root root    4096 May  5 15:09 .
drwxr-xr-x  1 root root    4096 May  5 15:09 ..
lrwxrwxrwx  1 root root       7 Apr 19 05:35 bin -> usr/bin
drwxr-xr-x  1 root root    4096 Apr 18  2022 boot
-rw-r--r--  1 root root       2 May  5 15:09 brighter
drwxr-xr-x  1 root root    4096 May  5 14:36 dev
drwxr-xr-x  1 root root    4096 May  5 14:36 etc
drwxr-xr-x  1 root root    4096 May  3 20:21 home
-rwxr-xr-x  1 root root 1440152 May  3 19:39 init
lrwxrwxrwx  1 root root       7 Apr 19 05:35 lib -> usr/lib
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib32 -> usr/lib32
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib64 -> usr/lib64
lrwxrwxrwx  1 root root      10 Apr 19 05:35 libx32 -> usr/libx32drwxr-xr-x  1 root root    4096 Apr 19 05:35 media
drwxr-xr-x  1 root root    4096 May  3 20:05 mnt
drwxr-xr-x  1 root root    4096 Apr 19 05:35 opt
dr-xr-xr-x  9 root root       0 May  5 14:36 proc
drwx------  1 root root    4096 Apr 19 05:36 root
drwxr-xr-x  1 root root    4096 May  5 15:08 run
lrwxrwxrwx  1 root root       8 Apr 19 05:35 sbin -> usr/sbin
drwxr-xr-x  1 root root    4096 Apr 19 05:36 snap
drwxr-xr-x  1 root root    4096 Apr 19 05:35 srv
dr-xr-xr-x 12 root root       0 May  5 14:36 sys
drwxrwxrwt  1 root root    4096 May  5 15:35 tmp
drwxr-xr-x  1 root root    4096 Apr 19 05:35 usr
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/$ cd /home
ciencat@SanYe_Uonlra:/home$ cd missing
-bash: cd: missing: No such file or directory
ciencat@SanYe_Uonlra:/home$ cd ./missing
-bash: cd: ./missing: No such file or directory
ciencat@SanYe_Uonlra:/home$ cd ./tmp
-bash: cd: ./tmp: No such file or directory
ciencat@SanYe_Uonlra:/home$ cd /tmp
ciencat@SanYe_Uonlra:/tmp$ cd missing
ciencat@SanYe_Uonlra:/tmp/missing$ cd /
ciencat@SanYe_Uonlra:/$ cd ~
ciencat@SanYe_Uonlra:~$ cd /home
ciencat@SanYe_Uonlra:/home$ cd -
/home/ciencat
ciencat@SanYe_Uonlra:~$ cd /home
ciencat@SanYe_Uonlra:/home$ cd -
/home/ciencat
ciencat@SanYe_Uonlra:~$ cd ../home
-bash: cd: ../home: No such file or directory
ciencat@SanYe_Uonlra:~$ cd../../../missing
-bash: cd../../../missing: No such file or directory
ciencat@SanYe_Uonlra:~$ cd ../../../missing
-bash: cd: ../../../missing: No such file or directory
ciencat@SanYe_Uonlra:~$ cd ../../missing
-bash: cd: ../../missing: No such file or directory
ciencat@SanYe_Uonlra:~$ cd /tmp/missing
ciencat@SanYe_Uonlra:/tmp/missing$ cd /
ciencat@SanYe_Uonlra:/$ cd -
/tmp/missing
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 nre.txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ cd /
ciencat@SanYe_Uonlra:/$ ls -l
total 1408
lrwxrwxrwx  1 root root       7 Apr 19 05:35 bin -> usr/bin
drwxr-xr-x  1 root root    4096 Apr 18  2022 boot
-rw-r--r--  1 root root       2 May  5 15:09 brighter
drwxr-xr-x  1 root root    4096 May  5 14:36 dev
drwxr-xr-x  1 root root    4096 May  5 14:36 etc
drwxr-xr-x  1 root root    4096 May  3 20:21 home
-rwxr-xr-x  1 root root 1440152 May  3 19:39 init
lrwxrwxrwx  1 root root       7 Apr 19 05:35 lib -> usr/lib
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib32 -> usr/lib32
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib64 -> usr/lib64
lrwxrwxrwx  1 root root      10 Apr 19 05:35 libx32 -> usr/libx32drwxr-xr-x  1 root root    4096 Apr 19 05:35 media
drwxr-xr-x  1 root root    4096 May  3 20:05 mnt
drwxr-xr-x  1 root root    4096 Apr 19 05:35 opt
dr-xr-xr-x  9 root root       0 May  5 14:36 proc
drwx------  1 root root    4096 Apr 19 05:36 root
drwxr-xr-x  1 root root    4096 May  5 15:08 run
lrwxrwxrwx  1 root root       8 Apr 19 05:35 sbin -> usr/sbin
drwxr-xr-x  1 root root    4096 Apr 19 05:36 snap
drwxr-xr-x  1 root root    4096 Apr 19 05:35 srv
dr-xr-xr-x 12 root root       0 May  5 14:36 sys
drwxrwxrwt  1 root root    4096 May  5 15:35 tmp
drwxr-xr-x  1 root root    4096 Apr 19 05:35 usr
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/$ cd -
/tmp/missing
ciencat@SanYe_Uonlra:/tmp/missing$ cd semester
-bash: cd: semester: Not a directory
ciencat@SanYe_Uonlra:/tmp/missing$ mv
mv: missing file operand
Try 'mv --help' for more information.
ciencat@SanYe_Uonlra:/tmp/missing$ mv nre.txt next,txt
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 next,txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ mv next.txt next.txt
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 next,txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ ^C
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 next,txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ mv next,txt next.txt
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 next.txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ cp semester to ../home
cp: target '../home' is not a directory
ciencat@SanYe_Uonlra:/tmp/missing$ cp semester to /home
cp: cannot create regular file '/home/semester': Permission denied
cp: cannot stat 'to': No such file or directory
ciencat@SanYe_Uonlra:/tmp/missing$ rm newfile
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 next.txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$  > newtxt.txt
ciencat@SanYe_Uonlra:/tmp/missing$ > newfile
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 16:47 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 16:47 newtxt.txt
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 next.txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ cd..
cd..: command not found
ciencat@SanYe_Uonlra:/tmp/missing$ cd ..
ciencat@SanYe_Uonlra:/tmp$ mkdir assignment
ciencat@SanYe_Uonlra:/tmp$ ls -l
total 0
drwxr-xr-x 1 ciencat ciencat 4096 May  5 16:49 assignment
drwxr-xr-x 1 ciencat ciencat 4096 May  5 16:47 missing
ciencat@SanYe_Uonlra:/tmp$ cd .
ciencat@SanYe_Uonlra:/tmp$ cd ./missing
ciencat@SanYe_Uonlra:/tmp/missing$ cd ..
ciencat@SanYe_Uonlra:/tmp$ cd ./assignment
ciencat@SanYe_Uonlra:/tmp/assignment$ ^C
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
ciencat@SanYe_Uonlra:/tmp/assignment$ man ls
ciencat@SanYe_Uonlra:/tmp/assignment$  < file1
-bash: file1: No such file or directory
ciencat@SanYe_Uonlra:/tmp/assignment$ echo helll\ wold > next.txtciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ cat next.txt
helll wold
ciencat@SanYe_Uonlra:/tmp/assignment$ cat < next.txt
helll wold
ciencat@SanYe_Uonlra:/tmp/assignment$ cat < next.txt > .././missing bext.txt
-bash: .././missing: Is a directory
ciencat@SanYe_Uonlra:/tmp/assignment$ cat < next.txt > .././missing./bext.txt
-bash: .././missing./bext.txt: No such file or directory
ciencat@SanYe_Uonlra:/tmp/assignment$ cat < next.txt > .././missing./next.txt
-bash: .././missing./next.txt: No such file or directory
ciencat@SanYe_Uonlra:/tmp/assignment$ cat < next.txt > hello.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:58 hello.txt
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ cat < next.txt >> hello.txtciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat 22 May  5 16:59 hello.txt
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ cat < hello.txt
helll wold
helll wold
ciencat@SanYe_Uonlra:/tmp/assignment$ man |
> aaa
What manual page do you want?
For example, try 'man man'.
Command 'aaa' not found, did you mean:
  command 'jaaa' from deb jaaa (0.9.2-1)
  command 'ara' from deb python3-ara (1.5.7-1)
  command 'aa' from deb astronomical-almanac (5.6-7)
  command 'aha' from deb aha (0.5.1-2)
Try: sudo apt install <deb name>
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l /
total 1408
lrwxrwxrwx  1 root root       7 Apr 19 05:35 bin -> usr/bin
drwxr-xr-x  1 root root    4096 Apr 18  2022 boot
-rw-r--r--  1 root root       2 May  5 15:09 brighter
drwxr-xr-x  1 root root    4096 May  5 14:36 dev
drwxr-xr-x  1 root root    4096 May  5 14:36 etc
drwxr-xr-x  1 root root    4096 May  3 20:21 home
-rwxr-xr-x  1 root root 1440152 May  3 19:39 init
lrwxrwxrwx  1 root root       7 Apr 19 05:35 lib -> usr/lib
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib32 -> usr/lib32
lrwxrwxrwx  1 root root       9 Apr 19 05:35 lib64 -> usr/lib64
lrwxrwxrwx  1 root root      10 Apr 19 05:35 libx32 -> usr/libx32drwxr-xr-x  1 root root    4096 Apr 19 05:35 media
drwxr-xr-x  1 root root    4096 May  3 20:05 mnt
drwxr-xr-x  1 root root    4096 Apr 19 05:35 opt
dr-xr-xr-x  9 root root       0 May  5 14:36 proc
drwx------  1 root root    4096 Apr 19 05:36 root
drwxr-xr-x  1 root root    4096 May  5 15:08 run
lrwxrwxrwx  1 root root       8 Apr 19 05:35 sbin -> usr/sbin
drwxr-xr-x  1 root root    4096 Apr 19 05:36 snap
drwxr-xr-x  1 root root    4096 Apr 19 05:35 srv
dr-xr-xr-x 12 root root       0 May  5 14:36 sys
drwxrwxrwt  1 root root    4096 May  5 16:49 tmp
drwxr-xr-x  1 root root    4096 Apr 19 05:35 usr
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l / | tail -n1
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l / | tail -n2
drwxr-xr-x  1 root root    4096 Apr 19 05:35 usr
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l / | tail -n2 > ls.txtciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat 22 May  5 16:59 hello.txt
-rw-r--r-- 1 ciencat ciencat 98 May  5 17:02 ls.txt
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ cat ls.txt
drwxr-xr-x  1 root root    4096 Apr 19 05:35 usr
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l | tail -n2 > ls.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  22 May  5 16:59 hello.txt
-rw-r--r-- 1 ciencat ciencat 106 May  5 17:04 ls.txt
-rw-r--r-- 1 ciencat ciencat  11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ cat ls.txt
-rw-r--r-- 1 ciencat ciencat  0 May  5 17:04 ls.txt
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ rm ls.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat 22 May  5 16:59 hello.txt
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ ls -l / | tail -n2 > ls.txtciencat@SanYe_Uonlra:/tmp/assignment$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat 22 May  5 16:59 hello.txt
-rw-r--r-- 1 ciencat ciencat 98 May  5 17:05 ls.txt
-rw-r--r-- 1 ciencat ciencat 11 May  5 16:54 next.txt
ciencat@SanYe_Uonlra:/tmp/assignment$ cat ls.txt
drwxr-xr-x  1 root root    4096 Apr 19 05:35 usr
drwxr-xr-x  1 root root    4096 Apr 19 05:36 var
ciencat@SanYe_Uonlra:/tmp/assignment$ curl --head --silen google.com
ciencat@SanYe_Uonlra:/tmp/assignment$ curl --head --silent google.com
q
quit
ciencat@SanYe_Uonlra:/tmp/assignment$ q
Command 'q' not found, but can be installed with:
sudo apt install python3-q-text-as-data
ciencat@SanYe_Uonlra:/tmp/assignment$ quit
Command 'quit' not found, did you mean:
  command 'quiz' from deb bsdgames (2.17-29)
  command 'quilt' from deb quilt (0.66-2.1)
  command 'qgit' from deb qgit (2.10-2)
  command 'luit' from deb x11-utils (7.7+5build2)
Try: sudo apt install <deb name>
ciencat@SanYe_Uonlra:/tmp/assignment$ curl --head --silent baidu.com
HTTP/1.1 200 OK
Date: Fri, 05 May 2023 09:09:24 GMT
Server: Apache
Last-Modified: Tue, 12 Jan 2010 13:48:00 GMT
ETag: "51-47cf7e6ee8400"
Accept-Ranges: bytes
Content-Length: 81
Cache-Control: max-age=86400
Expires: Sat, 06 May 2023 09:09:24 GMT
Connection: Keep-Alive
Content-Type: text/html

ciencat@SanYe_Uonlra:/tmp/assignment$ curl --head --silent baidu.com | --grep -i content-length
--grep: command not found
ciencat@SanYe_Uonlra:/tmp/assignment$ curl --head --silent baidu.com | grep -i content-length
Content-Length: 81
ciencat@SanYe_Uonlra:/tmp/assignment$ curl --head --silent baidu.com | grep -i content-length | cut --delimiter=' ' -f2
81
ciencat@SanYe_Uonlra:/tmp/assignment$ cd /sysfs
-bash: cd: /sysfs: No such file or directory
ciencat@SanYe_Uonlra:/tmp/assignment$ cd /sys
ciencat@SanYe_Uonlra:/sys$ ls
block  class  devices   fs      module
bus    dev    firmware  kernel  power
ciencat@SanYe_Uonlra:/sys$ ls -l
total 0
drwxr-xr-x 2 root root 0 May  5 14:36 block
drwxr-xr-x 2 root root 0 May  5 14:36 bus
drwxr-xr-x 7 root root 0 May  5 14:36 class
drwxr-xr-x 2 root root 0 May  5 14:36 dev
drwxr-xr-x 4 root root 0 May  5 14:36 devices
drwxr-xr-x 2 root root 0 May  5 14:36 firmware
drwxr-xr-x 3 root root 0 May  5 14:36 fs
drwxr-xr-x 5 root root 0 May  5 14:36 kernel
drwxr-xr-x 3 root root 0 May  5 14:36 module
drwxr-xr-x 2 root root 0 May  5 14:36 power
ciencat@SanYe_Uonlra:/sys$ cd backlight/
-bash: cd: backlight/: No such file or directory
ciencat@SanYe_Uonlra:/sys$ cd dev/
ciencat@SanYe_Uonlra:/sys/dev$ ls -l
total 0
ciencat@SanYe_Uonlra:/sys/dev$ sudo su
[sudo] password for ciencat:
Sorry, try again.
[sudo] password for ciencat:

[1]+  Stopped                 sudo su
ciencat@SanYe_Uonlra:/sys/dev$ sudo su
[sudo] password for ciencat:
Sorry, try again.
[sudo] password for ciencat:
root@SanYe_Uonlra:/sys/dev# cd /sys
root@SanYe_Uonlra:/sys# ls -l
total 0
drwxr-xr-x 2 root root 0 May  5 14:36 block
drwxr-xr-x 2 root root 0 May  5 14:36 bus
drwxr-xr-x 7 root root 0 May  5 14:36 class
drwxr-xr-x 2 root root 0 May  5 14:36 dev
drwxr-xr-x 4 root root 0 May  5 14:36 devices
drwxr-xr-x 2 root root 0 May  5 14:36 firmware
drwxr-xr-x 3 root root 0 May  5 14:36 fs
drwxr-xr-x 5 root root 0 May  5 14:36 kernel
drwxr-xr-x 3 root root 0 May  5 14:36 module
drwxr-xr-x 2 root root 0 May  5 14:36 power
root@SanYe_Uonlra:/sys# quit()
>
> aa
bash: syntax error near unexpected token `aa'
root@SanYe_Uonlra:/sys# sudo q
sudo: q: command not found
root@SanYe_Uonlra:/sys# exit
exit
ciencat@SanYe_Uonlra:/sys/dev$ sudo find
.
ciencat@SanYe_Uonlra:/sys/dev$ cd
ciencat@SanYe_Uonlra:~$ cd ——
-bash: cd: ——: No such file or directory
ciencat@SanYe_Uonlra:~$ cd —
-bash: cd: —: No such file or directory
ciencat@SanYe_Uonlra:~$ cd ~
ciencat@SanYe_Uonlra:~$ cd tmp
-bash: cd: tmp: No such file or directory
ciencat@SanYe_Uonlra:~$ cd ./home
-bash: cd: ./home: No such file or directory
ciencat@SanYe_Uonlra:~$ cd /home
ciencat@SanYe_Uonlra:/home$ cd ./tmp
-bash: cd: ./tmp: No such file or directory
ciencat@SanYe_Uonlra:/home$ cd /tmp
ciencat@SanYe_Uonlra:/tmp$ ls -l
total 0
drwxr-xr-x 1 ciencat ciencat 4096 May  5 17:05 assignment
drwxr-xr-x 1 ciencat ciencat 4096 May  5 16:47 missing
ciencat@SanYe_Uonlra:/tmp$ cd ./missing
ciencat@SanYe_Uonlra:/tmp/missing$ sudo finf
sudo: finf: command not found
ciencat@SanYe_Uonlra:/tmp/missing$ sudo find
.
./newfile
./newtxt.txt
./next.txt
./semester
ciencat@SanYe_Uonlra:/tmp/missing$ cd .
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 16:47 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 16:47 newtxt.txt
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 next.txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ cd ..
ciencat@SanYe_Uonlra:/tmp$ cd -
/tmp/missing
ciencat@SanYe_Uonlra:/tmp/missing$ cat next.txyt
cat: next.txyt: No such file or directory
ciencat@SanYe_Uonlra:/tmp/missing$ mv next.txt hello.txt
ciencat@SanYe_Uonlra:/tmp/missing$ ls -l
total 0
-rw-r--r-- 1 ciencat ciencat  0 May  5 15:22 hello.txt
-rw-r--r-- 1 ciencat ciencat  0 May  5 16:47 newfile
-rw-r--r-- 1 ciencat ciencat  0 May  5 16:47 newtxt.txt
-rwxr--r-- 1 ciencat ciencat 50 May  5 15:30 semester
ciencat@SanYe_Uonlra:/tmp/missing$ echo helloworld  >> hello.
txt
ciencat@SanYe_Uonlra:/tmp/missing$ cat hello.txt
helloworld
ciencat@SanYe_Uonlra:/tmp/missing$ echo hello >> hello.txt
ciencat@SanYe_Uonlra:/tmp/missing$ cat hello.txt
helloworld
hello
ciencat@SanYe_Uonlra:/tmp/missing$ xdg-open
Command 'xdg-open' not found, but can be installed with:
sudo apt install xdg-utils
ciencat@SanYe_Uonlra:/tmp/missing$ xdg-open hello.txt
Command 'xdg-open' not found, but can be installed with:
sudo apt install xdg-utils
ciencat@SanYe_Uonlra:/tmp/missing$  man xdg-open
No manual entry for xdg-open
ciencat@SanYe_Uonlra:/tmp/missing$ ^C
ciencat@SanYe_Uonlra:/tmp/missing$