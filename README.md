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
<img width="982" height="610" alt="image" src="https://github.com/user-attachments/assets/a9c01e67-0cb8-48a2-901c-bfd6777eeb11" />



cat < file2
## OUTPUT
<img width="981" height="610" alt="image" src="https://github.com/user-attachments/assets/8067185f-035a-4516-b5e9-b6bbc486e690" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="937" height="600" alt="image" src="https://github.com/user-attachments/assets/25f80c3b-f530-4df3-8e41-955225250aad" />

comm file1 file2
 ## OUTPUT
<img width="981" height="607" alt="image" src="https://github.com/user-attachments/assets/89dec203-d6ba-406d-bd77-1e5370584fe7" />

 
diff file1 file2
## OUTPUT
<img width="1088" height="605" alt="image" src="https://github.com/user-attachments/assets/4c711cd4-0fa6-417a-a5cf-d625819c69e5" />


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
<img width="1097" height="601" alt="image" src="https://github.com/user-attachments/assets/ed81dfa3-9fbb-49c4-8f8d-148b59d63c85" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="1126" height="613" alt="image" src="https://github.com/user-attachments/assets/a6576436-c837-46e9-a7f0-0f47bc3a31c0" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="1145" height="605" alt="image" src="https://github.com/user-attachments/assets/f3a4c0f6-5f9d-4da9-8888-869b8e854b77" />


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
<img width="1138" height="604" alt="image" src="https://github.com/user-attachments/assets/a63111ee-b9a2-4d6f-a981-9cca73d0f644" />



grep hello newfile 
## OUTPUT
<img width="1109" height="599" alt="image" src="https://github.com/user-attachments/assets/8e9f80ee-d6f1-4a13-adbd-0697588696a1" />



grep -v hello newfile 
## OUTPUT
<img width="993" height="603" alt="image" src="https://github.com/user-attachments/assets/af7051f5-a0b7-4d2b-8e69-6eb54b77d9a8" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1036" height="604" alt="image" src="https://github.com/user-attachments/assets/9aeb2bf1-f0db-4828-b463-b0ac1d630761" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1081" height="604" alt="image" src="https://github.com/user-attachments/assets/c15295f5-1230-40ae-8572-7f96394bbc47" />




grep -R ubuntu /etc
## OUTPUT
<img width="1090" height="608" alt="image" src="https://github.com/user-attachments/assets/54fb6308-f3c6-4ae3-b9cb-70e3a59287f6" />



grep -w -n world newfile 
## OUTPUT
<img width="1103" height="611" alt="image" src="https://github.com/user-attachments/assets/8d37e279-931c-45c2-a43e-5afaaf19db7d" />

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
<img width="968" height="604" alt="image" src="https://github.com/user-attachments/assets/f4d23eb0-e872-4d62-8fb3-c434766fce03" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1107" height="595" alt="image" src="https://github.com/user-attachments/assets/dbd429f8-cd60-4288-a6f4-918d95e0b3ab" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1074" height="607" alt="image" src="https://github.com/user-attachments/assets/524220e7-dc19-4e57-a75a-4902a9457588" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="1004" height="602" alt="image" src="https://github.com/user-attachments/assets/8f5f3656-e2fe-498d-9229-83f884c78bb5" />



egrep '(world$)' newfile 
## OUTPUT
<img width="958" height="603" alt="image" src="https://github.com/user-attachments/assets/23de92b4-17b0-4bd2-a40a-1e1aa7c9e5dd" />



egrep '(World$)' newfile 
## OUTPUT
<img width="1111" height="596" alt="image" src="https://github.com/user-attachments/assets/bb117060-9aa6-48d3-9f0f-558bd79c41b0" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1089" height="609" alt="image" src="https://github.com/user-attachments/assets/3167db28-8280-47b7-a26a-b0331d629155" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1071" height="614" alt="image" src="https://github.com/user-attachments/assets/aa17fe24-3651-4d8f-a8f2-e10fc5210cba" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1155" height="608" alt="image" src="https://github.com/user-attachments/assets/e9871de1-a9f0-47b4-b668-677160ac90f1" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1208" height="610" alt="image" src="https://github.com/user-attachments/assets/cb8ab74f-3be8-4b57-bd03-057283787f34" />



egrep l{2} newfile
## OUTPUT
<img width="1086" height="612" alt="image" src="https://github.com/user-attachments/assets/c6ae1b23-c565-4782-a4bb-39ab401edb08" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="928" height="608" alt="image" src="https://github.com/user-attachments/assets/ed214dd6-d459-4c96-a7b8-8d7b9a5f7df4" />

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
<img width="1151" height="606" alt="image" src="https://github.com/user-attachments/assets/8d4f6d15-3c07-4d2e-9300-0460a689ec42" />


sed -n -e '$p' file23
## OUTPUT
<img width="1188" height="612" alt="image" src="https://github.com/user-attachments/assets/8ba06781-a61e-4d9c-998e-c0752307c17b" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1084" height="605" alt="image" src="https://github.com/user-attachments/assets/55936b3f-0fdc-4553-983b-8d968e2e6631" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1010" height="607" alt="image" src="https://github.com/user-attachments/assets/fe6e9940-b9c6-4e9b-a3be-cd5ef544c329" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1086" height="609" alt="image" src="https://github.com/user-attachments/assets/b0800050-4a03-4e35-8e18-f246f589bc35" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="1070" height="598" alt="image" src="https://github.com/user-attachments/assets/33ebe157-bdff-4972-8fd7-7482c943e388" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="961" height="604" alt="image" src="https://github.com/user-attachments/assets/98cab10b-85a7-44e2-bef6-4bb4e4d6a222" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="945" height="615" alt="image" src="https://github.com/user-attachments/assets/7259f661-686a-4dd5-a6d6-5f5f33ff5fd2" />



seq 10 
## OUTPUT
<img width="957" height="611" alt="image" src="https://github.com/user-attachments/assets/40e5033a-b8f8-44a0-a1d4-e76fcd672616" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1102" height="608" alt="image" src="https://github.com/user-attachments/assets/83f531c3-6fd2-4df1-b5f6-71f8fab7f346" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1060" height="605" alt="image" src="https://github.com/user-attachments/assets/2d219378-9900-4d66-a1ba-ca7b464a723f" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="1085" height="611" alt="image" src="https://github.com/user-attachments/assets/248810bd-487c-49ad-9352-4b2a3e298d1a" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="1054" height="605" alt="image" src="https://github.com/user-attachments/assets/43b728d1-0230-419e-b052-7c67fcdb06d0" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1040" height="593" alt="image" src="https://github.com/user-attachments/assets/e3343504-75e1-4b37-8c1e-f368632732af" />
<img width="1085" height="608" alt="image" src="https://github.com/user-attachments/assets/f80fb962-f6c2-4efc-9b63-4fa8855eef8b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT




sed -n '2,4{s/$/*/;p}' file23

![s16](./op.img/s16.png)

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
![sort](./op.img/sort.png)

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

![uniq](./op.img/uniq.png)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1095" height="616" alt="image" src="https://github.com/user-attachments/assets/276b25c1-61be-4199-a313-eb48f42012cc" />



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
<img width="918" height="609" alt="image" src="https://github.com/user-attachments/assets/6c7676dd-de89-4a22-9db3-ce304fd95c1f" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="844" height="614" alt="image" src="https://github.com/user-attachments/assets/bc9a8395-667f-48e2-a188-2c402480a90a" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1036" height="608" alt="image" src="https://github.com/user-attachments/assets/0d726a95-34bc-4d8b-8124-8ee31c086c2b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="937" height="611" alt="image" src="https://github.com/user-attachments/assets/04fba1a7-ebea-4013-9812-12bb6d4762cc" />


tar -xvf backup.tar
## OUTPUT
<img width="1092" height="608" alt="image" src="https://github.com/user-attachments/assets/7522150a-70f9-4651-87d5-47a2934e7eda" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="1062" height="609" alt="image" src="https://github.com/user-attachments/assets/4d150599-e46a-4b52-a870-99487b4f22b3" />

 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![h1](./op.img/h1.png)

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
![ch1](./op.img/ch1.png)
 
ls file1
## OUTPUT
![lsfile1](./op.img/lsfile1.png)

echo $?
## OUTPUT 
![echo](./op.img/echo.png)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
 ![echo2](./op.img/echo2.png)

abcd
 
echo $?
 ## OUTPUT

 
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
##OUTPUT

![strcomp](./op.img/strcomp.png)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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

![per](./op.img/per.png)

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

![iper](./op.img/iper.png)

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
<img width="1282" height="611" alt="image" src="https://github.com/user-attachments/assets/58f9eac1-7342-4b88-8bc4-c4f68469580c" />



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
<img width="1042" height="602" alt="image" src="https://github.com/user-attachments/assets/99378e10-841c-44ed-b4f0-5c74c627605e" />

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

![test](./op.img/test.png)

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

## output
![case](./op.img/case.png)
 
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
 
 ## output

 ![until](./op.img/until.png)
 
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
 
 ## output
 ![forin](./op.img/forin.png)

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
## output
<img width="865" height="617" alt="image" src="https://github.com/user-attachments/assets/cb489ac1-47e8-4d99-99b5-fff8cada7c39" />


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
 
 ## output
 <img width="930" height="600" alt="image" src="https://github.com/user-attachments/assets/92f3349d-3d22-40b1-8117-2a39aa88a1b2" />

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
<img width="942" height="623" alt="image" src="https://github.com/user-attachments/assets/76e21813-35d6-4a3f-bff1-34467f9d5f6a" />


cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
``` chmod 777 forinfile.sh
$
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="1076" height="603" alt="image" src="https://github.com/user-attachments/assets/f713b370-579e-40bb-961e-673e5f88ec20" />



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
<img width="951" height="611" alt="image" src="https://github.com/user-attachments/assets/2dbd17b0-9707-47dd-9966-66e325536df8" />



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
<img width="1255" height="601" alt="image" src="https://github.com/user-attachments/assets/f6bb92fb-ae16-4bdb-848f-83c6f2ca19c1" />


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
<img width="1054" height="606" alt="image" src="https://github.com/user-attachments/assets/811a81bc-1b2c-4b3f-a174-bdb1f6d34801" />

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


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
 ## output
 <img width="920" height="610" alt="image" src="https://github.com/user-attachments/assets/5123f994-c3a7-4b7c-ad3f-b2f19b40bb97" />

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
<img width="947" height="604" alt="image" src="https://github.com/user-attachments/assets/1adfddc0-f05a-4fa2-b73c-da5b4a75cd0b" />
 
 


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
<img width="1004" height="604" alt="image" src="https://github.com/user-attachments/assets/9a8979d7-7efe-4ddb-989e-610bf563fe9d" />

![exread](./op.img/exread.png)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 





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
<img width="876" height="608" alt="image" src="https://github.com/user-attachments/assets/091fd507-db02-4aa5-8555-60c10b76a583" />

 ./funcex.sh 
![funcex1](./op.img/funcex1.png)
 
 ![funcex2](./op.img/funcex2.png)

 
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
<img width="1022" height="599" alt="image" src="https://github.com/user-attachments/assets/6861a373-818f-46b5-811e-fcda60857de8" />


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
<img width="1020" height="602" alt="image" src="https://github.com/user-attachments/assets/34197cd7-d6af-43aa-9b78-0eade45b8970" />

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
<img width="1019" height="608" alt="image" src="https://github.com/user-attachments/assets/d17e9d77-9909-4bad-a19c-73eabc05b2da" />
<img width="988" height="605" alt="image" src="https://github.com/user-attachments/assets/065915c5-26c4-41fc-b599-f08be5a1f3bc" />


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
 <img width="925" height="601" alt="image" src="https://github.com/user-attachments/assets/a91072c8-82ba-4088-802a-08c830c18b34" />

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
<img width="1151" height="604" alt="image" src="https://github.com/user-attachments/assets/eee00afa-399f-43ca-bcf6-ad0676977579" />




# RESULT:
The Commands are executed successfully.
