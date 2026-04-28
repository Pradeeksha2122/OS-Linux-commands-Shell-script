# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="1258" height="556" alt="image" src="https://github.com/user-attachments/assets/3ff51d2e-d1be-49f9-a25e-6d22d5c1377b" />



cat < file2
## OUTPUT
<img width="1252" height="495" alt="image" src="https://github.com/user-attachments/assets/1a5b6467-a26d-48aa-a18a-f1b993ff87ab" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="1238" height="599" alt="Screenshot 2026-04-28 234614" src="https://github.com/user-attachments/assets/5cf87e38-2cbb-486b-bf5f-376ba8dfff3f" />

 
comm file1 file2
 ## OUTPUT
 <img width="1054" height="586" alt="image" src="https://github.com/user-attachments/assets/234e8104-8b3b-4bc8-950b-18a20cc14980" />

diff file1 file2
## OUTPUT
<img width="1048" height="605" alt="image" src="https://github.com/user-attachments/assets/fdc8f223-f58a-4495-b196-31d1046c9e51" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
<img width="1182" height="622" alt="image" src="https://github.com/user-attachments/assets/97911ce7-3221-467c-8382-af723460819a" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="1135" height="615" alt="image" src="https://github.com/user-attachments/assets/218025f6-b8cb-47a9-986b-482e516d6d5d" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="1091" height="594" alt="image" src="https://github.com/user-attachments/assets/3c57d089-e810-448f-85e7-b3fed2c28fa6" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="944" height="576" alt="image" src="https://github.com/user-attachments/assets/a983fd8d-b1de-4b77-b484-b8d23b30b6d4" />



grep hello newfile 
## OUTPUT
<img width="1070" height="612" alt="image" src="https://github.com/user-attachments/assets/b15de6a0-66d3-4d94-b46a-4a9b12d1d6ef" />




grep -v hello newfile 
## OUTPUT
<img width="1045" height="618" alt="image" src="https://github.com/user-attachments/assets/51bc7015-1221-4887-8df8-a26b70a63f62" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="994" height="604" alt="image" src="https://github.com/user-attachments/assets/8795b500-742c-476a-9a04-6d5950190a96" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1069" height="610" alt="image" src="https://github.com/user-attachments/assets/c438b7b8-d664-43d7-9543-afb8eabfaef1" />




grep -R ubuntu /etc
## OUTPUT
<img width="1130" height="591" alt="image" src="https://github.com/user-attachments/assets/ad336eae-085e-4900-b0e5-dba4a21235f2" />



grep -w -n world newfile   
## OUTPUT
<img width="1001" height="607" alt="image" src="https://github.com/user-attachments/assets/65c948f1-f294-4d5d-bc77-8ed8c0274da2" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="959" height="586" alt="image" src="https://github.com/user-attachments/assets/d8ee2aa9-1fa4-4b09-8923-f27e3a113d9c" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1091" height="572" alt="image" src="https://github.com/user-attachments/assets/bce98e81-d268-41cc-b799-eee0edaf4d05" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="910" height="580" alt="image" src="https://github.com/user-attachments/assets/4fab0562-2a8b-46b3-bb96-db0610874ea4" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="1015" height="589" alt="image" src="https://github.com/user-attachments/assets/0936b178-ce86-495e-b504-a9eb01637a16" />


egrep '(world$)' newfile 
## OUTPUT
<img width="1000" height="564" alt="image" src="https://github.com/user-attachments/assets/f59950fc-e48e-4f59-8e40-47ccdb09fe23" />



egrep '(World$)' newfile 
## OUTPUT
<img width="932" height="590" alt="image" src="https://github.com/user-attachments/assets/49125796-5035-41a7-8e0f-23887b8efe5f" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="840" height="581" alt="image" src="https://github.com/user-attachments/assets/7ada24b3-786e-484c-a3b0-cc0af1805528" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1008" height="579" alt="image" src="https://github.com/user-attachments/assets/a00a20c8-e441-4ec2-b7fb-1bd778ca9aa8" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="881" height="573" alt="image" src="https://github.com/user-attachments/assets/febcad39-fbc3-4f90-b60d-b95b728e2cf9" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="891" height="588" alt="image" src="https://github.com/user-attachments/assets/882bf87b-3e19-4b42-9a73-d6bea138b0d4" />



egrep l{2} newfile
## OUTPUT
<img width="960" height="574" alt="image" src="https://github.com/user-attachments/assets/004b6c5f-0dab-4146-b81d-2094cd9df498" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="899" height="569" alt="image" src="https://github.com/user-attachments/assets/9749a48f-b1ac-4278-8e75-aa9bc6090611" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="1119" height="570" alt="image" src="https://github.com/user-attachments/assets/5dd56eee-551e-4d7c-bfda-3190b0321997" />



sed -n -e '$p' file23
## OUTPUT
<img width="963" height="601" alt="image" src="https://github.com/user-attachments/assets/7cad25a5-7994-4001-8260-e6d5c124f3c5" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="978" height="590" alt="image" src="https://github.com/user-attachments/assets/f66ef39e-bfd5-4346-ba4a-8f1dc7d2d858" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="982" height="585" alt="image" src="https://github.com/user-attachments/assets/cf33b826-f6aa-4617-b494-78c1997bb27c" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1069" height="583" alt="image" src="https://github.com/user-attachments/assets/04acb7c7-b85d-4597-b955-9602c975de1f" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="1148" height="589" alt="image" src="https://github.com/user-attachments/assets/d0fc344d-8c1b-4a5e-ae1a-539741ca4a91" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1116" height="608" alt="image" src="https://github.com/user-attachments/assets/33184624-a738-465f-a457-447f9b1a2a4e" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1010" height="592" alt="image" src="https://github.com/user-attachments/assets/7618cd5c-a55e-4b47-b160-75ca8864430d" />




seq 10 
## OUTPUT

<img width="976" height="574" alt="image" src="https://github.com/user-attachments/assets/4465f8c0-661d-48fd-8c8a-68dbe256ffd3" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1077" height="610" alt="image" src="https://github.com/user-attachments/assets/ef27e71a-cd4f-4175-91cb-607f7b999a79" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="986" height="573" alt="image" src="https://github.com/user-attachments/assets/03e3cb98-7fe9-4082-9e07-3d1fde797a0e" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="964" height="576" alt="image" src="https://github.com/user-attachments/assets/a2f8286e-f931-4ec1-8d48-07a752fc0123" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="1045" height="565" alt="image" src="https://github.com/user-attachments/assets/3772b708-0481-42e3-bbcc-906afbb9f608" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1008" height="589" alt="image" src="https://github.com/user-attachments/assets/d2ce80c8-46f8-4eb7-a00e-2eed3b10176d" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="975" height="592" alt="image" src="https://github.com/user-attachments/assets/b692ae19-9ac5-4f60-a752-3f35c367897b" />



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="1037" height="580" alt="image" src="https://github.com/user-attachments/assets/70e15378-a9dc-4d6c-b708-9de23dd2dc2c" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="1117" height="574" alt="image" src="https://github.com/user-attachments/assets/b407e779-9cca-4fb8-8676-82defcbc5a0e" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="1092" height="575" alt="image" src="https://github.com/user-attachments/assets/f6d4405d-8358-4fdd-b448-a0fb8c934eff" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="1105" height="605" alt="image" src="https://github.com/user-attachments/assets/621774b2-c8bd-4bd9-9130-f18c465a2083" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="911" height="602" alt="image" src="https://github.com/user-attachments/assets/4703e56a-d37a-4f4f-99b3-f1c160750a56" />





#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1130" height="587" alt="image" src="https://github.com/user-attachments/assets/155a10e9-bae7-4dc8-a161-9a5f02c3a4cb" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="926" height="591" alt="image" src="https://github.com/user-attachments/assets/f5a1d836-1c2d-4cb6-bb7a-5575fb560cf0" />


tar -xvf backup.tar
## OUTPUT
<img width="937" height="607" alt="image" src="https://github.com/user-attachments/assets/4f922f12-1b3c-4d28-951b-f3fbe14860f6" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1105" height="615" alt="image" src="https://github.com/user-attachments/assets/53016ffc-0f25-4a93-9113-8a4bce73c41a" />

gunzip backup.tar.gz
## OUTPUT
<img width="940" height="609" alt="image" src="https://github.com/user-attachments/assets/c50b96d8-86d1-4407-bd36-00dd9ef58151" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="995" height="608" alt="image" src="https://github.com/user-attachments/assets/1816338e-689d-46d7-ae6a-d844e069b5dd" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1158" height="613" alt="image" src="https://github.com/user-attachments/assets/9ec3e862-011c-4863-9ae2-5167d0399589" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="1015" height="614" alt="image" src="https://github.com/user-attachments/assets/65204b67-ae61-411d-8309-626b758e0837" />

 
ls file1
## OUTPUT
<img width="952" height="600" alt="image" src="https://github.com/user-attachments/assets/dbfe905b-4e07-4a70-beeb-4ecbc274db6e" />

echo $?
## OUTPUT 
<img width="879" height="613" alt="image" src="https://github.com/user-attachments/assets/b575f534-b3bb-4b1f-a286-fe0f4105936a" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="970" height="608" alt="image" src="https://github.com/user-attachments/assets/0ab15fd0-969a-4499-89d1-52839151e29a" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="1015" height="590" alt="image" src="https://github.com/user-attachments/assets/0d5525f3-5de1-448d-8c6f-42fa4681feee" />


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
<img width="932" height="612" alt="image" src="https://github.com/user-attachments/assets/8d16a211-1e5b-42d3-b806-d3903dd36c8e" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="902" height="613" alt="image" src="https://github.com/user-attachments/assets/d1f5228b-23ab-43df-8e61-f3ffe7cebb09" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="975" height="607" alt="image" src="https://github.com/user-attachments/assets/e60b5613-1645-4ff7-8ff0-71acbcefdf29" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="1038" height="606" alt="image" src="https://github.com/user-attachments/assets/c05a8472-81d0-43ca-b42c-a6bfadcfcea3" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="931" height="600" alt="image" src="https://github.com/user-attachments/assets/d955bae0-9c19-41f2-9be1-82dc83cba462" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="1017" height="600" alt="image" src="https://github.com/user-attachments/assets/6dd757ac-0294-4b45-bd26-a363219f2af7" />

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
<img width="859" height="605" alt="image" src="https://github.com/user-attachments/assets/0b0a6ad1-3de2-4905-a8af-22316f58a2b7" />

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="1013" height="602" alt="image" src="https://github.com/user-attachments/assets/e62c2e1c-1e46-47bb-9d1d-748f95fdae72" />



cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="1053" height="611" alt="image" src="https://github.com/user-attachments/assets/1319d244-1b86-4f33-a307-3bc0a30ee4ac" />


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="817" height="615" alt="image" src="https://github.com/user-attachments/assets/6ab0f1c0-ac6b-445c-b31e-1cb910283135" />

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="994" height="609" alt="image" src="https://github.com/user-attachments/assets/be4dd3d8-bf3a-4dc2-9fb0-1e72a0780724" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
<img width="1007" height="608" alt="image" src="https://github.com/user-attachments/assets/ea56b6fb-5069-4d33-b5a5-3e25046633d9" />


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="1018" height="595" alt="image" src="https://github.com/user-attachments/assets/fb736b75-fea8-4885-aac0-f451a006a2f2" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="993" height="605" alt="image" src="https://github.com/user-attachments/assets/029858d0-ccec-4d79-abf9-d113b8c4f5a0" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="950" height="616" alt="image" src="https://github.com/user-attachments/assets/dba3f798-54ad-4d73-8020-c09fe5ff77da" />



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
<img width="1019" height="605" alt="image" src="https://github.com/user-attachments/assets/5c18a4b5-0d76-4c54-b885-2feed2e20f4a" />

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
<img width="1011" height="602" alt="image" src="https://github.com/user-attachments/assets/87375c7e-f2c3-4d10-be14-97b3fba5fc70" />

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
<img width="1158" height="605" alt="image" src="https://github.com/user-attachments/assets/f078ff30-3700-49cd-9841-97d7717efe68" />

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
<img width="1165" height="604" alt="image" src="https://github.com/user-attachments/assets/b32225ff-039c-49cb-81d1-37c3a421da53" />
<img width="1226" height="605" alt="image" src="https://github.com/user-attachments/assets/3eba2b9c-fe8b-4f12-ae37-76391d9b1a40" />


 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 <img width="981" height="601" alt="image" src="https://github.com/user-attachments/assets/8c544bd2-6bd9-4b51-8bc8-17693b9c9bea" />

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="1056" height="604" alt="image" src="https://github.com/user-attachments/assets/5b64f2be-f9f0-484e-b64d-6e4350ce506c" />


# RESULT:
The Commands are executed successfully.
