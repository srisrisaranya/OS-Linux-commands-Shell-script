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



cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/2e200674-8737-4403-afde-af24cfe60def)

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/949d02b3-62c2-4b47-8942-bd2ae7f9806c)

 

comm file1 file2
 ## OUTPUT

![image](https://github.com/user-attachments/assets/8e4f7599-a29c-4188-92ec-0b006d1fc68f)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/485903ca-7e6e-4315-a79d-44435e8d48aa)


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
![image](https://github.com/user-attachments/assets/de5a890d-956d-44db-82bb-1ee1d9aa1b41)




cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/e8b17852-1305-4f4a-87c4-3d8a8ede3bec)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/f60d48ce-1174-415f-99f8-12d6c452753c)


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
![image](https://github.com/user-attachments/assets/3ec2fb10-117e-4eeb-9b27-9a2c9c92ced1)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2ffed174-668b-40ae-b71c-38d1ab204706)




grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e29768f7-1410-412b-bc1c-8aadc2f9a715)


cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/12c24152-926e-4cf3-8f3c-9c403796ad6a)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/477c3457-963f-45b6-a90f-a189e186c1ff)



grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/e3b2f2b8-abec-48f9-b1e8-9850c15bc34c)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/cb4f72d5-bca0-4f48-b419-ad93972f9113)


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

![image](https://github.com/user-attachments/assets/efc2440a-7906-43e6-9a32-f40764974210)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/969f9d7b-99c3-4965-ad4d-a7f6296e0769)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/bc8929f5-2e75-4518-adf0-b1e07eae7659)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f301d437-1a29-4e08-aa54-1d5878e7937f)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a6fc0140-6de8-45cd-be8d-6d08f2904a01)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8f455549-5a89-4185-9e29-38cc0cbcac95)



egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/cc2eb447-aedd-4006-b912-0ae622e2edee)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a055fc37-59dc-4df3-9a9e-8524ca69df66)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/1fe79544-f47e-4821-9068-06cc67bc32e3)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/1a67bcd8-9b96-4b96-a409-8024a6668088)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/730ae74b-f369-444c-b8ca-b0f978892a24)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/1fbae31e-f8d1-4166-beeb-bdb1c021b226)


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

![image](https://github.com/user-attachments/assets/4bed3849-58fc-49d8-8e44-fad58b077334)


sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/9b0959b9-c5da-42e2-8a51-1a19d4de3f83)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/3ef5bf6e-7aeb-4cf5-8f11-8929137c5024)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2096d4c2-9f64-49d2-920c-3ab21806aad6)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/378f17d7-8b01-4f3c-b69d-ae7fcde61823)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/97563b14-8c4c-493f-80e5-49e3c5e62725)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5faa3761-2b06-4eee-8e2d-90cd23667921)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/b1637c1c-162c-4e8a-a0db-8ba4dde8f992)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/dc825557-826f-4f2b-9e09-f8fe6945515c)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/c5b4cb76-5675-4bc0-8c07-643bf74ba87f)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/009fa8ee-7583-4aa0-bb7b-3b2c8de05d91)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/484e7474-8752-4e99-ab7f-ead041d77450)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/1800eae4-9b78-4707-8f7d-3eb9dd149ba1)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/327a2375-1c7b-45c1-8e61-807851bfd870)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/622cdd2c-6313-453d-94ea-9ed908cc865c)



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
![image](https://github.com/user-attachments/assets/b539491b-fc4c-4230-9801-746ab17b12ce)


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
![image](https://github.com/user-attachments/assets/44523abc-7712-4247-bcca-506d2e7c41c3)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/a1560fd5-d340-476b-b33d-73e49951d2f4)

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

![image](https://github.com/user-attachments/assets/e537f241-a54a-46ea-bd94-b2c9f2d29263)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/7a3e9b80-d6aa-4b7f-a6fd-a09c28428985)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
bench.py file1 file11 file2 file21 file22 file23 hello.c hello.js newfile readme.txt urllist.txt

mkdir backupdir

mv backup.tar backupdir

tar -tvf backup.tar

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/ -rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt -rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt

tar -xvf backup.tar

tar -xvf backup.tar
## OUTPUT
x file1.txt x directory1/ x directory1/file2.txt x directory1/file3.txt

gzip backup.tar

ls .gz
gzip backup.tar

ls .gz
## OUTPUT
backup.tar.gz

gunzip backup.tar.gz

## OUTPUT
backup.tar
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image](https://github.com/user-attachments/assets/539c0212-5fa0-44a2-ba82-3bc45d19ee0f)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/a4e57021-5ea5-4818-886c-de457da95a81)

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
File name is ./scriptest.sh File name is scriptest.sh First arg. is 1 Second arg. is 2 Third arg. is 3 Fourth arg. is The 
@
i
s
1
2
3
T
h
e
# is
```
$#
The $
```

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/75419d9e-7454-4f55-98f3-f1de8df5e205)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/d1e573b4-a94a-43d2-affc-b21abe16a80a)

echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
1

 
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

![image](https://github.com/user-attachments/assets/b4ba1f10-7187-421e-9db8-0c1286be5a98)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
baseball is less than hockey

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
You are the owner of the /etc/passwd file
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
![image](https://github.com/user-attachments/assets/270d3971-b70f-4819-8baa-e7fe0d7f93e8)



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
![image](https://github.com/user-attachments/assets/c67ef1c2-20ec-4d0a-8ff3-f30ac685c99c)


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
![image](https://github.com/user-attachments/assets/3b001935-76c4-4595-be04-cf33cd5c21bc)

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
Welcome Ram Please enjoy your visit Welcome Rahim Please enjoy your visit Special testing account gganesh, Do not forget to logout when you're done Sorry, you are not allowed here

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
![image](https://github.com/user-attachments/assets/f9ad4310-dbd4-4773-a6d4-209ca0c1e216)

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
###OUTPUT
10 9 8 7 6 5 4 3 2 1
 
 
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
word:I word:don't word:know word:if word:this'll word:work
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
The value of i is 1 The value of i is 2 The value of i is 3 The value of i is 4 The value of i is 5
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
1 - 5 2 - 4 3 - 3 4 - 2 5 - 1
 
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
Iteration number: 1 Iteration number: 2 The for loop is completed
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
Iteration number: 1 Iteration number: 2 Iteration number: 4 Iteration number: 5 The for loop is completed
 
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

Enter your name: John Hello John, welcome to my program.
 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
Enter your name: John Hello John, welcome to my program.


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
 $ bash script.sh 1 2 The result is 2
 
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
1 2 3
$ ./argshift.sh 1 2 3
 (( 0 ))
set +x
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
 (( 0 ))
set +x
 
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
 total characters 75 Number of Lines are 10 No of Words count: 10
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
Enter the number 121 Number is palindrome Enter the number 69 Number is NOT palindrome

# RESULT:
The Commands are executed successfully.


