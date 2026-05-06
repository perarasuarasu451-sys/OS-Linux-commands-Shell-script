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
<img width="254" height="158" alt="image" src="https://github.com/user-attachments/assets/a8e8ffd7-c3b2-4e59-956b-c98906c7ed60" />



cat < file2
## OUTPUT
<img width="288" height="177" alt="image" src="https://github.com/user-attachments/assets/93c85763-9ef8-48d3-96c0-c7bf198a0ac4" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="351" height="82" alt="image" src="https://github.com/user-attachments/assets/2158fd00-d443-42de-b25e-19ce20528d57" />

comm file1 file2
 ## OUTPUT
<img width="308" height="228" alt="image" src="https://github.com/user-attachments/assets/0c27291d-7d4a-4734-92ba-44fa9663cd04" />

 
diff file1 file2
## OUTPUT
cle<img width="260" height="276" alt="image" src="https://github.com/user-attachments/assets/c68fb7bd-9111-4484-8dcb-53295d37e1ed" />


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
<img width="259" height="100" alt="image" src="https://github.com/user-attachments/assets/1caa0ad4-ad8a-4de1-be7f-2434e8b47dda" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="304" height="127" alt="image" src="https://github.com/user-attachments/assets/33f11280-0a25-4464-b1a2-4c8e554a4edf" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="296" height="127" alt="image" src="https://github.com/user-attachments/assets/fc0ea5b1-c9ac-4bfc-82a2-f92313bf8c83" />


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
<img width="268" height="78" alt="image" src="https://github.com/user-attachments/assets/4c8f851e-5590-4562-bffa-5f12c03f146d" />



grep hello newfile 
## OUTPUT
<img width="271" height="75" alt="image" src="https://github.com/user-attachments/assets/9ecf945f-9639-4291-b2d1-7220f6d555e4" />




grep -v hello newfile 
## OUTPUT
<img width="299" height="74" alt="image" src="https://github.com/user-attachments/assets/624ef299-30e5-4a62-85a7-6e78a2e3ecf1" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="361" height="101" alt="image" src="https://github.com/user-attachments/assets/ae8e3a3f-f261-472c-bdf7-72a04f74534d" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="393" height="83" alt="image" src="https://github.com/user-attachments/assets/6d69e740-f659-492d-aea5-0502363f7907" />




grep -R ubuntu /etc
## OUTPUT

<img width="508" height="372" alt="image" src="https://github.com/user-attachments/assets/6b7ceb80-af07-49a1-b4d7-dabb630ddae9" />


grep -w -n world newfile   
## OUTPUT
<img width="323" height="103" alt="image" src="https://github.com/user-attachments/assets/8a11eac0-0149-4944-b5c0-98fd015faf39" />


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
<img width="393" height="107" alt="image" src="https://github.com/user-attachments/assets/55eeafae-b684-49f7-b242-a27660f20aa1" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="350" height="96" alt="image" src="https://github.com/user-attachments/assets/baa93fb6-da81-4416-a837-0cee3f54f9f4" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="396" height="100" alt="image" src="https://github.com/user-attachments/assets/6256c544-8f73-47ce-93f9-46e514263e89" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="310" height="73" alt="image" src="https://github.com/user-attachments/assets/0cd0f395-b584-4a49-9929-ecf13abae256" />


egrep '(world$)' newfile 
## OUTPUT
<img width="320" height="103" alt="image" src="https://github.com/user-attachments/assets/23cddd3e-928d-448a-91ff-95f76b1e5b9b" />



egrep '(World$)' newfile 
## OUTPUT
<img width="316" height="82" alt="image" src="https://github.com/user-attachments/assets/15561012-61b7-4dc3-99e2-246cfff854cd" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="367" height="126" alt="image" src="https://github.com/user-attachments/assets/9e73a9fb-1816-49ed-81f8-d3a5d2de8e1d" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="287" height="75" alt="image" src="https://github.com/user-attachments/assets/263c8b78-d44a-4ef0-8f30-0c5cd3b64d91" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="361" height="83" alt="image" src="https://github.com/user-attachments/assets/f9f702d1-41ff-45b2-95da-2408a3247350" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="362" height="73" alt="image" src="https://github.com/user-attachments/assets/6ff520e8-78bb-499c-b916-3ce4746b4193" />


egrep l{2} newfile
## OUTPUT

<img width="257" height="104" alt="image" src="https://github.com/user-attachments/assets/4731d047-7b70-4aa5-9ae0-2605e27d3720" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="306" height="131" alt="image" src="https://github.com/user-attachments/assets/9e7810ca-c8e7-416b-8158-c1f5a1231979" />


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

<img width="281" height="72" alt="image" src="https://github.com/user-attachments/assets/56d326d2-a9f0-474b-9680-415f49dcaf5b" />


sed -n -e '$p' file23
## OUTPUT

<img width="284" height="74" alt="image" src="https://github.com/user-attachments/assets/b3adbf04-b611-4ba8-9cb7-a1704ed8a835" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="356" height="254" alt="image" src="https://github.com/user-attachments/assets/9f567df5-9a76-4320-a3bf-0b1295904185" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="367" height="252" alt="image" src="https://github.com/user-attachments/assets/93536bc9-6e5d-433e-830a-a1911fbf64ee" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="386" height="258" alt="image" src="https://github.com/user-attachments/assets/1c7aa1bc-ae59-4130-b3da-9b2d8839def7" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="328" height="179" alt="image" src="https://github.com/user-attachments/assets/1586ee7d-57eb-47d7-904f-db2b72a12018" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="347" height="133" alt="image" src="https://github.com/user-attachments/assets/26a8ed43-5ee9-4f51-8298-c125aca6e8a1" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="395" height="103" alt="image" src="https://github.com/user-attachments/assets/95e6801f-cac3-4568-90a5-99cca02f690b" />


seq 10 
## OUTPUT
<img width="249" height="302" alt="image" src="https://github.com/user-attachments/assets/d8f42166-1d9e-4ebe-a543-1bce437b6af4" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="292" height="130" alt="image" src="https://github.com/user-attachments/assets/6ab5fab8-fc3f-4630-9985-809f91347bbe" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="305" height="127" alt="image" src="https://github.com/user-attachments/assets/558068de-bba7-450e-9805-8a6ff05db95b" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="292" height="148" alt="image" src="https://github.com/user-attachments/assets/381dfc7e-a84c-490a-afe2-5077e67a4f40" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="302" height="129" alt="image" src="https://github.com/user-attachments/assets/0a4196b3-3930-4746-9c95-52089121a979" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="327" height="129" alt="image" src="https://github.com/user-attachments/assets/e72bbec3-cc57-45c2-8e50-eea685d0e3cc" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="371" height="130" alt="image" src="https://github.com/user-attachments/assets/358400ad-d88d-4b6e-906d-7b57f64c2b20" />



sed -n '2,4{s/$/*/;p}' file23
<img width="363" height="131" alt="image" src="https://github.com/user-attachments/assets/40a532e3-2bf3-4de5-9928-a04ae8934eea" />


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
<img width="311" height="180" alt="image" src="https://github.com/user-attachments/assets/a459c0a4-42fc-4407-813c-ed80b4827884" />


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

<img width="319" height="178" alt="image" src="https://github.com/user-attachments/assets/f80459ee-3048-4afe-99a1-274233eb1340" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="431" height="250" alt="image" src="https://github.com/user-attachments/assets/7df28dfa-d6c2-427d-8d40-2c7c8e83fc65" />

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
<img width="338" height="123" alt="image" src="https://github.com/user-attachments/assets/e85682e6-e5ac-449c-8337-4455863707e3" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="471" height="127" alt="image" src="https://github.com/user-attachments/assets/83033c62-949a-4bbe-9215-5ec2dc3ca41c" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="330" height="777" alt="image" src="https://github.com/user-attachments/assets/ab9d4e69-e1a1-4b27-a270-bfa80da34af7" />
<img width="326" height="602" alt="image" src="https://github.com/user-attachments/assets/8c55069f-99a7-4be6-8c91-848ac358f597" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="806" height="779" alt="image" src="https://github.com/user-attachments/assets/c985f537-5764-41f2-b0a8-f263e169ea2e" />
<img width="868" height="607" alt="image" src="https://github.com/user-attachments/assets/856bd96f-373e-4fb7-bcd9-b9fd9c8031b7" />


tar -xvf backup.tar
## OUTPUT
<img width="357" height="782" alt="image" src="https://github.com/user-attachments/assets/17a2d260-e332-461e-8baf-9414059c46a1" />
<img width="336" height="601" alt="image" src="https://github.com/user-attachments/assets/daa6669e-ef52-4eb5-b6c7-f6aacb0336b4" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="533" height="131" alt="image" src="https://github.com/user-attachments/assets/73c28974-8918-48bd-9b0e-e65f2c86c78f" />

gunzip backup.tar.gz
## OUTPUT
<img width="385" height="54" alt="image" src="https://github.com/user-attachments/assets/e6a06a93-18b6-4e62-95bf-2f8d2f025529" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="718" height="125" alt="image" src="https://github.com/user-attachments/assets/f80c9dbd-b663-4964-ab54-181cc9995073" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="349" height="300" alt="image" src="https://github.com/user-attachments/assets/943d82cc-bbeb-4cd6-bdbd-33a8fb16d777" />


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
<img width="649" height="504" alt="image" src="https://github.com/user-attachments/assets/72622252-24e8-4f97-aabc-bba051650cab" />

 
ls file1
## OUTPUT
<img width="292" height="75" alt="image" src="https://github.com/user-attachments/assets/d18dbbb5-4e8d-4f2c-90b1-69ed404974de" />

echo $?
## OUTPUT 

<img width="251" height="77" alt="image" src="https://github.com/user-attachments/assets/bc421874-4e2d-488e-bbbd-9dea93fd82e8" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="313" height="75" alt="image" src="https://github.com/user-attachments/assets/e4f2f577-9e9f-4182-9968-b652ef978982" />
 
abcd
 
echo $?
 ## OUTPUT

<img width="256" height="77" alt="image" src="https://github.com/user-attachments/assets/8f0eafd1-018e-4385-99cc-2764d43625b6" />

 
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
##OUTPUT:
<img width="361" height="279" alt="image" src="https://github.com/user-attachments/assets/098ec815-9c37-4463-8f90-b68c6e90b347" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="644" height="100" alt="image" src="https://github.com/user-attachments/assets/fb814e55-9e6b-41aa-a5eb-edd4ab95e2c4" />


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
<img width="428" height="74" alt="image" src="https://github.com/user-attachments/assets/7dacae2e-e597-4601-8b2c-cb8d5c1a759c" />

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

<img width="394" height="74" alt="image" src="https://github.com/user-attachments/assets/a1c0f2f3-b751-45b0-a9a6-63b2e4be91e9" />


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
<img width="474" height="383" alt="image" src="https://github.com/user-attachments/assets/f08774ab-b493-4e0a-bb86-05dc64aaf728" />

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
<img width="600" height="108" alt="image" src="https://github.com/user-attachments/assets/2ed63158-4fcb-46bf-bc77-7414e387230e" />

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
<img width="637" height="61" alt="image" src="https://github.com/user-attachments/assets/fa619055-0b91-4762-8979-610a761511ae" />


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
<img width="622" height="53" alt="image" src="https://github.com/user-attachments/assets/cbb39a5c-b04e-4ef4-b350-0ca075183df7" />

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
<img width="211" height="131" alt="image" src="https://github.com/user-attachments/assets/6e5fa880-8df9-4629-866b-01256f508639" />

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
<img width="65" height="131" alt="image" src="https://github.com/user-attachments/assets/28a649bb-b2c0-4dbc-ae6a-774860d2d8ef" />

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
<img width="166" height="307" alt="image" src="https://github.com/user-attachments/assets/c84f1a1d-11ab-468f-8423-da1224b04b48" />

 
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
<img width="687" height="80" alt="image" src="https://github.com/user-attachments/assets/af16f9f8-45e3-472f-bba2-bb52e7e3258c" />

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
 <img width="216" height="103" alt="image" src="https://github.com/user-attachments/assets/3596ef7b-63e7-4329-8d98-e557e45e11b0" />

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
<img width="246" height="77" alt="image" src="https://github.com/user-attachments/assets/48e95434-e1b9-4767-a085-c1e1da2dbc6d" />

 
 ./funcex.sh 1 2
<img width="275" height="81" alt="image" src="https://github.com/user-attachments/assets/6473fddc-f770-40de-ab2c-7b33c9af1e04" />

 
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
<img width="26" height="81" alt="image" src="https://github.com/user-attachments/assets/c152774c-5b53-4165-921a-43f71bcf85f2" />

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
 <img width="41" height="88" alt="image" src="https://github.com/user-attachments/assets/f16e9e7f-bcbc-4a2e-b936-2346236dc4a3" />

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
 <img width="293" height="408" alt="image" src="https://github.com/user-attachments/assets/be0b3184-a958-410c-8fef-b396d8ea95e2" />

 
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
 <img width="857" height="375" alt="image" src="https://github.com/user-attachments/assets/02bb2d86-4ec6-4958-864e-c12b924847ea" />

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
<img width="232" height="82" alt="image" src="https://github.com/user-attachments/assets/30ae6e4d-63cd-4303-81ee-5df06157d11f" />


# RESULT:
The Commands are executed successfully.
