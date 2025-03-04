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
![c1](https://github.com/user-attachments/assets/561f8ed3-889c-4c6f-b4e1-cfeb55fc7f78)



cat < file2
## OUTPUT
![c2](https://github.com/user-attachments/assets/5a3afaf4-b315-4db4-8a10-1851ffabca45)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![c3](https://github.com/user-attachments/assets/dd5f3697-6d0e-4b42-a35a-f3fa11941322)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-03-04 13-43-01](https://github.com/user-attachments/assets/ad43d4ed-ca09-4013-a094-88520d2175be)

 
diff file1 file2
## OUTPUT
![c4](https://github.com/user-attachments/assets/fa5fa424-d694-4e99-a947-902d4520a6f8)


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
![Screenshot from 2025-03-04 13-18-03](https://github.com/user-attachments/assets/54c97368-3472-433b-bcf7-f05f0e1136fd)




cut -d "|" -f 1 file22
## OUTPUT
![c6](https://github.com/user-attachments/assets/63e03928-ba13-4792-87e6-a39f76d0d15d)



cut -d "|" -f 2 file22
## OUTPUT
![c7](https://github.com/user-attachments/assets/d343079c-3a5b-4f4d-9318-774eab17c11e)


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

![Screenshot from 2025-03-04 13-18-52](https://github.com/user-attachments/assets/71525343-a241-4ad4-8a75-ac32c86fc964)



grep hello newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-19-20](https://github.com/user-attachments/assets/6ce15001-d7bb-4787-b7f4-c8a63e4c5313)



grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-19-20](https://github.com/user-attachments/assets/f3848def-ed5f-47e4-b836-b2df206442e4)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-04 13-19-56](https://github.com/user-attachments/assets/0adc969b-2edb-4dd4-9df5-dfd2d8c2ece8)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-03-04 13-20-19](https://github.com/user-attachments/assets/072f8b97-8e69-493c-8614-a7d4db1bb772)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-04 13-20-45](https://github.com/user-attachments/assets/4768896f-1f51-489c-8b0d-ccb31998863b)


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

![Screenshot from 2025-03-04 13-30-59](https://github.com/user-attachments/assets/e8220b47-6cfc-4f12-93db-66f40db1375a)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-31-26](https://github.com/user-attachments/assets/059eb248-c4d2-468d-abe2-bfe31fd66eb1)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-32-08](https://github.com/user-attachments/assets/5efe1321-5a86-423f-9d6f-20a56ce437f3)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-32-36](https://github.com/user-attachments/assets/2b6534e9-5ed1-452a-9c58-2cf23fc7c386)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-32-55](https://github.com/user-attachments/assets/c50fc3a9-482f-46ed-b7b1-fec5c5e68e97)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-04 13-33-15](https://github.com/user-attachments/assets/4c995d18-d881-46bf-9fce-eeaa2024d570)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-33-39](https://github.com/user-attachments/assets/15f875b7-05c3-4dc7-b0eb-8ae73772d699)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-03-04 13-34-09](https://github.com/user-attachments/assets/1f6e9a6b-4c93-4933-8db3-14f273e1a4fe)


egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-04 13-34-49](https://github.com/user-attachments/assets/5de0eb21-b806-4a5f-bfcc-63383ff9689b)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-04 13-35-06](https://github.com/user-attachments/assets/b8141e7c-83cb-4b28-8de0-04a87218fa61)


egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-03-04 13-35-25](https://github.com/user-attachments/assets/3c946b95-7f10-486f-bcc6-011ec2aea52e)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-04 13-35-48](https://github.com/user-attachments/assets/37979431-a9b3-4809-8e27-4ad241fe8d25)


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

![Screenshot from 2025-02-28 09-21-50](https://github.com/user-attachments/assets/27194f81-dfda-4201-a341-7803c7db4785)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-02-28 09-22-22](https://github.com/user-attachments/assets/99b5a9c6-b1dc-46b6-a323-5cc6e8d921d2)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-02-28 09-22-42](https://github.com/user-attachments/assets/375ccd58-0218-4c4a-904f-0d1d54479c9f)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-02-28 09-23-17](https://github.com/user-attachments/assets/3e9267b8-c457-4cf1-ba97-4a38947720d9)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-02-28 09-25-37](https://github.com/user-attachments/assets/62401cdc-4f1b-42d0-9dff-f206fafed090)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-02-28 09-25-54](https://github.com/user-attachments/assets/dd55b5ec-b6d3-4944-a4c0-997703a9c02a)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-02-28 09-26-13](https://github.com/user-attachments/assets/fd7d74d4-f73e-449a-b81d-157e9020813c)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-02-28 09-26-37](https://github.com/user-attachments/assets/38f4ef2a-696b-43af-a877-73f246368057)


seq 10 
## OUTPUT

![Screenshot from 2025-02-28 09-27-08](https://github.com/user-attachments/assets/60ffa229-d5d6-4500-b03c-bb145c389380)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-02-28 09-27-46](https://github.com/user-attachments/assets/c37fc5da-5aff-44a4-885a-d879ed3c95ca)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-02-28 09-28-06](https://github.com/user-attachments/assets/e57cbf32-fb08-4fc4-8b00-399077b27e52)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-02-28 09-28-48](https://github.com/user-attachments/assets/9f2b7a7f-ca2f-4995-bb31-0d8f0e522823)


seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-02-28 09-29-10](https://github.com/user-attachments/assets/b42eb735-c9e3-4810-988f-06bdcf3c025c)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-02-28 09-29-34](https://github.com/user-attachments/assets/be16c546-f9f6-4729-9c87-1731c31c1105)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-02-28 09-30-03](https://github.com/user-attachments/assets/b0ac11e4-9616-4b4e-8c55-a41c6fb22e32)


sed -n '2,4{s/$/*/;p}' file23
![Screenshot from 2025-02-28 09-30-27](https://github.com/user-attachments/assets/7d3d73bf-e5c0-4c81-846f-92e5fcecb7b2)


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
![Screenshot from 2025-02-28 09-30-50](https://github.com/user-attachments/assets/b7f1302d-3785-45fa-8d61-a44cb2a91c1f)


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

![Screenshot from 2025-02-28 09-31-16](https://github.com/user-attachments/assets/bc1f11ff-3139-401c-885e-d824c2b9d73f)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-02-28 19-46-00](https://github.com/user-attachments/assets/c8630a3d-9edb-4db3-86c2-0ff558d28222)

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

![Screenshot from 2025-02-28 19-46-57](https://github.com/user-attachments/assets/d90dcc09-a99d-4460-a26d-fd4e8fc09b57)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-02-28 19-47-19](https://github.com/user-attachments/assets/78ec60bb-5b8f-4037-8a5a-b11ac901594e)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-02-28 19-48-36](https://github.com/user-attachments/assets/e5eb0b30-80c8-4ece-96c2-864ea847ddd4)

mkdir backupdir
 
mv backup.tar backupdir
 
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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-02-28 20-14-23](https://github.com/user-attachments/assets/c58f6025-2f07-4e0c-83c6-2e2a5e257c7b)


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
![Screenshot from 2025-03-04 14-00-02](https://github.com/user-attachments/assets/e2f94055-2198-4138-ac9d-6f318e04f9bc)

 
ls file1
## OUTPUT
![Screenshot from 2025-03-04 14-02-49](https://github.com/user-attachments/assets/a0594c8c-1e3b-4379-b7e3-b1d54af25151)

echo $?
## OUTPUT 
![Screenshot from 2025-03-04 14-03-07](https://github.com/user-attachments/assets/e13004fe-a094-42e0-84ba-ad7ebca62482)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![Screenshot from 2025-03-04 14-07-21](https://github.com/user-attachments/assets/f1222355-2304-4b8b-ac6c-96592c5f9290)

abcd
 
echo $?
 ## OUTPUT

![Screenshot from 2025-03-04 14-03-55](https://github.com/user-attachments/assets/19408170-b702-4464-a70b-a4e1f2bb5247)

 
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
