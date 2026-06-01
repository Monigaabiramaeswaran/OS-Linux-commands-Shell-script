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

<img width="940" height="132" alt="image" src="https://github.com/user-attachments/assets/995b9ba5-363a-427b-8a7a-b90a7f4b4c42" />


cat < file2
## OUTPUT

<img width="940" height="73" alt="image" src="https://github.com/user-attachments/assets/2e8fed07-bd7e-4474-8a08-96acae440207" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="940" height="42" alt="image" src="https://github.com/user-attachments/assets/96aa6879-91af-4ff3-8198-42e212e95506" />

comm file1 file2
 ## OUTPUT
<img width="940" height="122" alt="image" src="https://github.com/user-attachments/assets/e4aa33ee-edaa-4187-9da5-5f10bb262e4c" />

 
diff file1 file2
## OUTPUT

<img width="940" height="122" alt="image" src="https://github.com/user-attachments/assets/78f92a78-1249-4eda-8256-edd1ae1b41ea" />

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

<img width="940" height="269" alt="image" src="https://github.com/user-attachments/assets/011431d2-2e07-4c1f-9284-0f4d3e9ce5e4" />



cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT


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

<img width="940" height="81" alt="image" src="https://github.com/user-attachments/assets/5516aa58-ceaa-4e87-80bb-c413f465f9e3" />


grep hello newfile 
## OUTPUT

<img width="940" height="81" alt="image" src="https://github.com/user-attachments/assets/17eec974-0437-4855-aad1-711948d1a487" />



grep -v hello newfile 
## OUTPUT

<img width="940" height="26" alt="image" src="https://github.com/user-attachments/assets/2a0ed1ee-481f-4bce-a510-5a6674c0ffa6" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="940" height="36" alt="image" src="https://github.com/user-attachments/assets/34046c1c-6c6c-4dc5-9185-f9d3cb280542" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="940" height="36" alt="image" src="https://github.com/user-attachments/assets/31082826-af80-4161-9647-5bd79f175408" />


grep -R ubuntu /etc
## OUTPUT

<img width="940" height="36" alt="image" src="https://github.com/user-attachments/assets/29cb5d22-1861-4ff0-8510-bda23db73c89" />


grep -w -n world newfile   
## OUTPUT
<img width="940" height="36" alt="image" src="https://github.com/user-attachments/assets/ef3c62ea-8c3b-498c-9132-107b1f17d9f1" />


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

<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/2fa5e890-5d6a-477e-9613-fc4f2cff80c0" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/82925e8c-ec19-4404-ab4e-79da240d6a55" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/3267b88a-48c9-4ecb-916e-64b254bad216" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/cd3853ca-c1f9-4c1a-bc33-22aca3f80ad6" />


egrep '(world$)' newfile 
## OUTPUT
<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/74e810da-19c6-46a2-8271-3a737a6dfdf3" />



egrep '(World$)' newfile 
## OUTPUT
<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/6b1332ae-ca7c-4bd1-91fc-5224d833b10b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/1b9bde2a-b873-43ee-b377-5eae8e408a51" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/91565986-067c-4181-b107-826521732ffb" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="940" height="26" alt="image" src="https://github.com/user-attachments/assets/ba26c68c-d77a-4c56-b5a2-ee2409d9e191" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/11790b90-a47d-481e-bd58-ec2c8e680b08" />


egrep l{2} newfile
## OUTPUT
<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/bd74efff-d66c-4e2c-98da-be2cd02a3a84" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/b0ecac2f-db1b-4ef2-92fa-d7aac05f4188" />


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

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/f0c5d3a0-1d24-40c6-897d-dd280c9d66b7" />


sed -n -e '$p' file23
## OUTPUT

<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/edc27fec-6d2c-4bf0-a028-55d6e9934636" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/23fd64cd-3431-4827-be05-b03a279d53cb" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/efc80a64-3dac-4423-8d1c-387a06ebc9fd" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="940" height="72" alt="image" src="https://github.com/user-attachments/assets/246d9ef0-7f12-4e1c-a526-d0f581121951" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/b982752a-58d4-4f03-b91b-c917d6819b28" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="940" height="38" alt="image" src="https://github.com/user-attachments/assets/7c2427b1-b546-437a-b5be-d276f672694b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="940" height="38" alt="image" src="https://github.com/user-attachments/assets/f40cb0b3-c232-474d-8c74-60b2bb45a224" />


seq 10 
## OUTPUT

<img width="940" height="126" alt="image" src="https://github.com/user-attachments/assets/fa76561a-553c-4055-83d4-9df68e2f7060" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/1deae505-d59f-467e-94f2-212731873b8f" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/7e68f693-6850-4386-93e0-c6b69066fa3a" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="940" height="58" alt="image" src="https://github.com/user-attachments/assets/b01ae5d9-bf76-4f26-ac95-02b15e9e0179" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/4acee2cc-3e96-4baf-9f47-fcd1c2e5a602" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/5492efe7-b6a3-44dd-a05c-911903857ba4" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/52d59b14-b0c3-4d2a-95fa-bf16200d1259" />


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

<img width="940" height="102" alt="image" src="https://github.com/user-attachments/assets/3520c7a4-11c9-41f0-86b6-403444b35309" />

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

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/15e6bd8a-bbab-4ee8-9291-053037613585" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/7aa5f682-aff8-43fe-9e43-0366da2174d1" />

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
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
<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/d11740fb-4b1d-4b4e-8287-6d858d820ddb" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="940" height="103" alt="image" src="https://github.com/user-attachments/assets/747ccc83-d3ca-4860-acd0-9085a62ad561" />

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

 
ls file1
## OUTPUT
<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/1a9a3923-6cb6-45d8-9a40-3df85ceaaf7e" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/cfe27a10-7b2e-49bc-b648-0240ecf440a7" />

echo $?
## OUTPUT 
 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/5d20e925-15e1-401e-b50e-45b99d6c6828" />

abcd
 
echo $?
 ## OUTPUT

<img width="940" height="112" alt="image" src="https://github.com/user-attachments/assets/b38c1b55-54e3-415c-8139-4b53a4b1678c" />

 
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

<img width="940" height="26" alt="image" src="https://github.com/user-attachments/assets/69e43e5f-163c-41a6-bb48-7d9ad1a88dc6" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="940" height="117" alt="image" src="https://github.com/user-attachments/assets/e8877d4e-bb08-4d4d-8653-70f6342d4f0e" />

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
<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/87001e95-c4af-4cf3-8521-79fa677ca7d4" />

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
<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/3c0d030b-197b-46f1-9d53-23325d76b6f7" />

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
<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/a37b3b41-8180-40ef-abd0-7157d539855a" />

 
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
<img width="940" height="192" alt="image" src="https://github.com/user-attachments/assets/f8af1750-24ad-4a54-ab04-9cf30c6b6e47" />

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
<img width="940" height="118" alt="image" src="https://github.com/user-attachments/assets/666886f7-7be0-406e-90eb-df946c53061e" />


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
<img width="966" height="214" alt="image" src="https://github.com/user-attachments/assets/b3fa026c-fb8a-435b-a5af-9bc61133665f" />

 
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
<img width="940" height="48" alt="image" src="https://github.com/user-attachments/assets/d5950114-8e1f-47e5-b729-5914e2bef5c2" />
 
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
 <img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/bee65c3c-2164-4fa2-823b-9543b644d0e2" />

 
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
 <img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/3570ecd8-b5fe-4a5c-b2dd-35035b1a3833" />

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
<img width="940" height="343" alt="image" src="https://github.com/user-attachments/assets/62d9f700-3b26-40e2-9305-b4af16092c87" />


# RESULT:
The Commands are executed successfully.
