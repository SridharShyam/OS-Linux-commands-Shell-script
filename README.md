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

<img width="262" height="117" alt="image" src="https://github.com/user-attachments/assets/585cb375-d3aa-4e47-aa10-9f9c63bbfd90" />

cat < file2
## OUTPUT

<img width="248" height="132" alt="image" src="https://github.com/user-attachments/assets/d14b3f24-a7c1-44fb-a5e2-36be2b7423f2" />

# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="342" height="65" alt="image" src="https://github.com/user-attachments/assets/c45d4e32-e0fc-46ce-917d-a74b677545a2" />

comm file1 file2
 ## OUTPUT

<img width="260" height="151" alt="image" src="https://github.com/user-attachments/assets/f92aff55-1c2b-4517-9880-80fb83dbed68" />

diff file1 file2
## OUTPUT

<img width="231" height="188" alt="image" src="https://github.com/user-attachments/assets/dbaed6b6-983b-41fd-b8ab-82308c32f779" />

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

<img width="227" height="72" alt="image" src="https://github.com/user-attachments/assets/805fcea7-9045-470f-af36-762af8c5e0b3" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="243" height="98" alt="image" src="https://github.com/user-attachments/assets/033d78d3-1cfe-4a5c-86fc-5a75bb76c1d5" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="245" height="95" alt="image" src="https://github.com/user-attachments/assets/f4fa6b83-8463-4f85-a3e8-41d42dec9f89" />

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

<img width="238" height="67" alt="image" src="https://github.com/user-attachments/assets/10da68ff-8c46-4120-b713-5af90c5eafbe" />

grep hello newfile 
## OUTPUT

<img width="237" height="65" alt="image" src="https://github.com/user-attachments/assets/dbc336b1-eb1c-4da0-b199-c15eec02863e" />

grep -v hello newfile 
## OUTPUT

<img width="233" height="67" alt="image" src="https://github.com/user-attachments/assets/5b1b1234-c818-408f-a32f-6e2d0da40509" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="288" height="92" alt="image" src="https://github.com/user-attachments/assets/af7d9654-c5aa-47f9-a19e-43b54b9f4fc1" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="317" height="67" alt="image" src="https://github.com/user-attachments/assets/4cc72153-3a1a-4a45-92dd-7c71824a3c3c" />

grep -R ubuntu /etc
## OUTPUT

<img width="675" height="552" alt="image" src="https://github.com/user-attachments/assets/8da89824-bfd0-4710-9bf8-6bcd97d9c722" />

grep -w -n world newfile   
## OUTPUT

<img width="302" height="78" alt="image" src="https://github.com/user-attachments/assets/b156ffe0-9083-43c4-aec8-dac47ab45a73" />

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

<img width="307" height="78" alt="image" src="https://github.com/user-attachments/assets/2a33d0de-b518-41e9-bf64-09b757569192" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="296" height="87" alt="image" src="https://github.com/user-attachments/assets/6616fbc1-eada-4b74-a76e-a10a33e1d2ca" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="310" height="76" alt="image" src="https://github.com/user-attachments/assets/549a3263-175b-4542-8980-49827a706518" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="252" height="73" alt="image" src="https://github.com/user-attachments/assets/bdc2dd72-dc37-4f2a-a590-5a6f7fe15222" />

egrep '(world$)' newfile 
## OUTPUT

<img width="267" height="90" alt="image" src="https://github.com/user-attachments/assets/898f7559-7744-476d-93b8-37548491d35f" />

egrep '(World$)' newfile 
## OUTPUT

<img width="288" height="53" alt="image" src="https://github.com/user-attachments/assets/d7d99a88-2894-48a5-9ecc-dafe38a96289" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="282" height="96" alt="image" src="https://github.com/user-attachments/assets/87b1f5ed-97af-4faa-bf5c-69355e6a46ca" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="237" height="67" alt="image" src="https://github.com/user-attachments/assets/1c9996ab-c1f1-48c5-8178-88a3511ec7f7" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="342" height="80" alt="image" src="https://github.com/user-attachments/assets/143396f6-4941-4fe1-9110-2736b278188c" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="317" height="45" alt="image" src="https://github.com/user-attachments/assets/05701dad-70c9-4b10-8ebd-3818ae0141d3" />

egrep l{2} newfile
## OUTPUT

<img width="277" height="66" alt="image" src="https://github.com/user-attachments/assets/c2af5a0a-d2f6-4ea0-90fe-6cb27148e54d" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="262" height="93" alt="image" src="https://github.com/user-attachments/assets/2da172ec-929c-4412-a3dc-e25573fad5b9" />

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

<img width="285" height="77" alt="image" src="https://github.com/user-attachments/assets/860e8707-bb4f-44f3-a5bd-8e5f5c2ef0c3" />

sed -n -e '$p' file23
## OUTPUT

<img width="257" height="62" alt="image" src="https://github.com/user-attachments/assets/8d67930f-672b-4adc-8508-aa4afdb37a0f" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="295" height="172" alt="image" src="https://github.com/user-attachments/assets/ddb097a1-cb11-4c6f-ae95-208ea63fb8fb" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="267" height="177" alt="image" src="https://github.com/user-attachments/assets/6f69d926-6e9c-4b9d-8ae0-63f25d3ae2a6" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="315" height="175" alt="image" src="https://github.com/user-attachments/assets/2620806f-a618-4c84-baa3-56b2b5663d4e" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="276" height="133" alt="image" src="https://github.com/user-attachments/assets/4d14a47f-29c5-40e9-8caf-f26556c12256" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="308" height="98" alt="image" src="https://github.com/user-attachments/assets/330c7623-387a-4871-8e6d-efd2b74f97ab" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="297" height="85" alt="image" src="https://github.com/user-attachments/assets/404a6ad8-fe3b-4c41-bf07-2fd426a8716a" />

seq 10 
## OUTPUT

<img width="233" height="211" alt="image" src="https://github.com/user-attachments/assets/1b55e5df-58d6-4627-b918-8186d86ae344" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="237" height="86" alt="image" src="https://github.com/user-attachments/assets/274b19d4-3ef8-4358-a45b-35d74b22b747" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="247" height="103" alt="image" src="https://github.com/user-attachments/assets/9fa2cd82-272c-4572-a594-896fc5a5d437" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="277" height="116" alt="image" src="https://github.com/user-attachments/assets/b7d7d6f1-4398-4b6c-b03b-ae2649f98f20" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="232" height="96" alt="image" src="https://github.com/user-attachments/assets/63d767cc-40d5-47d5-ad32-8b945eb11c80" />

seq 10 | sed '2,9c hello'e
## OUTPUT

<img width="261" height="96" alt="image" src="https://github.com/user-attachments/assets/f39dd031-d8c2-4be3-b55f-5872cd54410d" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="321" height="98" alt="image" src="https://github.com/user-attachments/assets/70eb3a68-50cd-4096-bc2c-4960d3344ba5" />

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="291" height="100" alt="image" src="https://github.com/user-attachments/assets/8fd178eb-0b37-4b90-84b2-906ccfbaf02c" />

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

<img width="258" height="127" alt="image" src="https://github.com/user-attachments/assets/3ae0bc58-a15a-4354-801c-67628e39bf14" />

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

<img width="252" height="127" alt="image" src="https://github.com/user-attachments/assets/e2c0e9c0-af93-4229-8b7c-66fff8a1ed96" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT

<img width="335" height="172" alt="image" src="https://github.com/user-attachments/assets/c7a4a7bd-21a7-4c0b-ab63-ecc8f9bfb438" />

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

<img width="272" height="98" alt="image" src="https://github.com/user-attachments/assets/721d028b-1713-4f41-a687-79b383ba0244" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="357" height="100" alt="image" src="https://github.com/user-attachments/assets/4eb5050f-182f-4eb0-a29f-f507f6f94779" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="266" height="167" alt="image" src="https://github.com/user-attachments/assets/698a40b9-69bc-4ea0-810d-ade5025e9daa" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="518" height="178" alt="image" src="https://github.com/user-attachments/assets/44681e65-faf6-437b-9d1a-acb1dfa5d80f" />

tar -xvf backup.tar
## OUTPUT

<img width="346" height="168" alt="image" src="https://github.com/user-attachments/assets/c80a3927-9f73-468c-84c8-30d60fdf7933" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="392" height="58" alt="image" src="https://github.com/user-attachments/assets/c8c15a60-b59f-446e-bfca-0018a7c06928" />

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

<img width="372" height="85" alt="image" src="https://github.com/user-attachments/assets/77eebfa7-5022-4fe9-830e-df3afd44a6b2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="358" height="97" alt="image" src="https://github.com/user-attachments/assets/6a1fc74e-3e17-4e3e-b6a4-5137561f85d5" />

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

<img width="343" height="265" alt="image" src="https://github.com/user-attachments/assets/9bdfb5c7-f11c-4082-973d-32bc547efea4" />

 
ls file1
## OUTPUT

<img width="342" height="66" alt="image" src="https://github.com/user-attachments/assets/0eae745b-a524-4868-b5cd-eda485e73254" />

echo $?
## OUTPUT 

<img width="338" height="67" alt="image" src="https://github.com/user-attachments/assets/bc3a2e5c-6c70-48fc-8387-b48ed92c5389" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="347" height="66" alt="image" src="https://github.com/user-attachments/assets/27d7d6b1-3d0f-4a88-879b-c1f6a1c74988" />

abcd
 
echo $?
## OUTPUT

<img width="347" height="66" alt="image" src="https://github.com/user-attachments/assets/63f1866e-4c2b-4293-b9ff-e053949eb157" />

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

<img width="321" height="197" alt="image" src="https://github.com/user-attachments/assets/015c230c-ea77-415c-af07-3806907ca244" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="347" height="86" alt="image" src="https://github.com/user-attachments/assets/7f1882c8-d2a8-4065-96f9-8ec457025eae" />

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

<img width="541" height="162" alt="image" src="https://github.com/user-attachments/assets/3be3fbd9-cbcd-42dc-be25-ff5a3232ae66" />

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

<img width="407" height="332" alt="image" src="https://github.com/user-attachments/assets/41f0ecf2-ea47-4360-98f1-3996c390f467" />

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
## OUTPUT

<img width="366" height="97" alt="image" src="https://github.com/user-attachments/assets/631d6699-ceaf-47e1-913c-8ae44ac75d78" />

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
## OUTPUT

<img width="467" height="98" alt="image" src="https://github.com/user-attachments/assets/65e46c44-ce69-4f07-a689-fa13cb99d626" />

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

<img width="422" height="83" alt="image" src="https://github.com/user-attachments/assets/7006051d-b8b1-4a37-a778-f26d330f0ebb" />

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

# using the case command
cat > casecheck.sh 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.
