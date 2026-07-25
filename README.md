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

<img width="559" height="162" alt="image" src="https://github.com/user-attachments/assets/66ca514a-c1ae-4b36-a8fa-19220fd73055" />


cat < file2
## OUTPUT

<img width="567" height="173" alt="image" src="https://github.com/user-attachments/assets/a6d26583-1e57-4b7e-8da0-0dffb6168130" />



# Comparing Files
cmp file1 file2
## OUTPUT


<img width="562" height="80" alt="image" src="https://github.com/user-attachments/assets/621faf6d-2e81-4cd0-ae58-1fd4ca56c80d" />

 
comm file1 file2
 ## OUTPUT


<img width="560" height="227" alt="image" src="https://github.com/user-attachments/assets/f31c8501-53a3-4550-88ab-6093dd97b93b" />

 
diff file1 file2
## OUTPUT

<img width="565" height="280" alt="image" src="https://github.com/user-attachments/assets/c6d0e569-188b-4fc0-9597-20c3f495d150" />



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


<img width="564" height="101" alt="image" src="https://github.com/user-attachments/assets/638acbd0-64fd-4ce8-8b53-9306045d9b97" />


cut -d "|" -f 1 file22
## OUTPUT


<img width="559" height="133" alt="image" src="https://github.com/user-attachments/assets/4aaae441-4376-441c-9677-3644c95f3f53" />



cut -d "|" -f 2 file22
## OUTPUT


<img width="561" height="133" alt="image" src="https://github.com/user-attachments/assets/30ff4d5d-df24-4d9b-afda-911f7313b401" />




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


<img width="569" height="81" alt="image" src="https://github.com/user-attachments/assets/0a475804-1d3f-49f1-a72e-9b29a61da996" />



grep hello newfile 
## OUTPUT

<img width="567" height="70" alt="image" src="https://github.com/user-attachments/assets/0022b78f-b915-4e02-84d3-675a3e70fd6d" />




grep -v hello newfile 
## OUTPUT


<img width="561" height="85" alt="image" src="https://github.com/user-attachments/assets/3f2fca9f-53f2-4216-aace-0d7a45ff6e98" />



cat newfile | grep -i "hello"
## OUTPUT


<img width="568" height="95" alt="image" src="https://github.com/user-attachments/assets/7963284e-ec03-4958-bb7d-ee5ced63a9ad" />




cat newfile | grep -i -c "hello"
## OUTPUT


<img width="562" height="78" alt="image" src="https://github.com/user-attachments/assets/b0730e65-959c-4d95-b04a-5153a1a1adcc" />



grep -R ubuntu /etc
## OUTPUT



<img width="1332" height="561" alt="image" src="https://github.com/user-attachments/assets/86198060-d0f3-4a13-bc48-b9d468cfc74d" />


grep -w -n world newfile   
## OUTPUT

<img width="639" height="100" alt="image" src="https://github.com/user-attachments/assets/0d2241d7-e843-4e2c-8643-4c9b907a36e4" />



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


<img width="644" height="100" alt="image" src="https://github.com/user-attachments/assets/a1423bfe-d93f-4e21-a209-23e112768632" />




egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="645" height="96" alt="image" src="https://github.com/user-attachments/assets/5e4eb050-ab27-486e-b476-8117136b640f" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="648" height="96" alt="image" src="https://github.com/user-attachments/assets/da2a3f4f-b4e0-4c79-bd77-4e0846a904c2" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="655" height="72" alt="image" src="https://github.com/user-attachments/assets/19b7e5e7-9b65-4378-8961-fa4c7aa77f47" />



egrep '(world$)' newfile 
## OUTPUT


<img width="648" height="103" alt="image" src="https://github.com/user-attachments/assets/8770027a-2dec-4c87-a6be-df4c9a7d2334" />



egrep '(World$)' newfile 
## OUTPUT

<img width="647" height="85" alt="image" src="https://github.com/user-attachments/assets/ba8c7083-0d9c-4b72-89b5-eebcfb7b9ea2" />



egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="640" height="126" alt="image" src="https://github.com/user-attachments/assets/059e45ab-d2c2-4974-8b51-91131c383f70" />



egrep '[1-9]' newfile 
## OUTPUT



<img width="647" height="87" alt="image" src="https://github.com/user-attachments/assets/a5646d48-22a7-42f0-8071-cc5f347fee67" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="648" height="77" alt="image" src="https://github.com/user-attachments/assets/68779a5e-ee98-4cd9-befe-9eed0162e65c" />



egrep 'Linux.*World' newfile 
## OUTPUT


<img width="643" height="75" alt="image" src="https://github.com/user-attachments/assets/b12f342e-0fe6-4866-a81c-46d0acb50a13" />



egrep l{2} newfile
## OUTPUT


<img width="640" height="109" alt="image" src="https://github.com/user-attachments/assets/af73e884-64aa-42e6-b51e-a8700f744339" />



egrep 's{1,2}' newfile
## OUTPUT 


<img width="639" height="122" alt="image" src="https://github.com/user-attachments/assets/5b317d08-4ccf-4139-aab9-bbb7db09bad9" />



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


<img width="641" height="77" alt="image" src="https://github.com/user-attachments/assets/34688c7e-a9e6-4a84-b4c9-5242f7d25e27" />




sed -n -e '$p' file23
## OUTPUT


<img width="648" height="75" alt="image" src="https://github.com/user-attachments/assets/32009848-7561-4f40-b8da-ccf047492beb" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT



<img width="649" height="262" alt="image" src="https://github.com/user-attachments/assets/778c5920-067a-4863-bb4a-dcb41a564671" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="646" height="258" alt="image" src="https://github.com/user-attachments/assets/678dfee9-e013-4477-842c-325d11a9fa89" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="644" height="250" alt="image" src="https://github.com/user-attachments/assets/97dce356-54ff-4396-aeac-f429fc550bb2" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="645" height="169" alt="image" src="https://github.com/user-attachments/assets/50620aed-7cf1-4a25-bc51-9a1fa37b8538" />




sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="648" height="126" alt="image" src="https://github.com/user-attachments/assets/ccf1a198-ef45-4065-bd5b-c7f7bcfe31c4" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="640" height="105" alt="image" src="https://github.com/user-attachments/assets/ef4dcc41-2912-4bd3-b3dd-16f2f70f563d" />



seq 10 
## OUTPUT

<img width="648" height="303" alt="image" src="https://github.com/user-attachments/assets/efe20ef3-1eb2-4423-9d1b-67f9692c7627" />




seq 10 | sed -n '4,6p'
## OUTPUT


<img width="647" height="134" alt="image" src="https://github.com/user-attachments/assets/7f3df09d-771d-4449-94aa-ed21d25fd9b3" />



seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="641" height="125" alt="image" src="https://github.com/user-attachments/assets/b3cef919-f7cc-4f99-b3d0-095ccb1e8df1" />



seq 3 | sed '2a hello'
## OUTPUT


<img width="643" height="160" alt="image" src="https://github.com/user-attachments/assets/ced63fb2-469a-4e47-8dbc-fe68bcf7db2c" />



seq 2 | sed '2i hello'
## OUTPUT


<img width="642" height="136" alt="image" src="https://github.com/user-attachments/assets/f6f763e5-f144-4def-b12e-4f02b9b95043" />



seq 10 | sed '2,9c hello'
## OUTPUT


<img width="644" height="132" alt="image" src="https://github.com/user-attachments/assets/b93aa233-5f1a-43dd-b2f6-62f6b9b439cf" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="643" height="128" alt="image" src="https://github.com/user-attachments/assets/91a4bf05-5e59-4e34-8bcd-394f270f9657" />




sed -n '2,4{s/$/*/;p}' file23


<img width="634" height="135" alt="image" src="https://github.com/user-attachments/assets/75dc66af-d551-4a49-b8b8-5e3f5dd2a310" />


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


<img width="647" height="182" alt="image" src="https://github.com/user-attachments/assets/0292b3b0-97a5-4bab-81ca-35325f0efc00" />




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


<img width="648" height="174" alt="image" src="https://github.com/user-attachments/assets/f92d2672-37d1-46c2-bc94-aed3712132f2" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT


<img width="646" height="253" alt="image" src="https://github.com/user-attachments/assets/dde5f54d-b8f9-4a33-b334-623a983ad98f" />




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

<img width="645" height="127" alt="image" src="https://github.com/user-attachments/assets/3b376ba2-54d0-4d35-ba67-732f9a3f8a3c" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



<img width="645" height="128" alt="image" src="https://github.com/user-attachments/assets/c28886fe-0b9b-4bb8-a42f-06b305f913de" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="647" height="253" alt="image" src="https://github.com/user-attachments/assets/4936cb1d-1c71-4ea4-8be8-ab76d4238abf" />




mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="641" height="410" alt="image" src="https://github.com/user-attachments/assets/58a39289-0f87-4048-adb7-48ba56cbe0c8" />





tar -xvf backup.tar
## OUTPUT

<img width="644" height="252" alt="image" src="https://github.com/user-attachments/assets/b9ae0ae8-7bc5-4614-aa99-4a9dd2e50dbc" />


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

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
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
