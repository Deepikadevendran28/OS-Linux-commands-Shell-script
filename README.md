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

<img width="393" height="133" alt="Screenshot 2026-07-26 142139" src="https://github.com/user-attachments/assets/c303f935-195a-4bfb-8d3f-02c39f5bf25b" />


cat < file2
## OUTPUT

<img width="394" height="159" alt="image" src="https://github.com/user-attachments/assets/74a256c1-e3ae-4289-94aa-84f076c1a03c" />



# Comparing Files
cmp file1 file2
## OUTPUT


<img width="418" height="66" alt="image" src="https://github.com/user-attachments/assets/78edec0e-3302-4ca0-9ac8-4a49c621fa5b" />

 
comm file1 file2
 ## OUTPUT


<img width="434" height="198" alt="image" src="https://github.com/user-attachments/assets/94eab58e-fa77-4167-b9b5-c8e6c559b01b" />


 
diff file1 file2
## OUTPUT


<img width="499" height="246" alt="image" src="https://github.com/user-attachments/assets/8ccdcf6e-b6e7-4b6a-89d2-3c25ddcbc011" />


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


<img width="386" height="87" alt="Screenshot 2026-07-26 142949" src="https://github.com/user-attachments/assets/f19bf3cf-1aa3-45dc-bd3c-d7e9e12feac9" />


cut -d "|" -f 1 file22
## OUTPUT


<img width="390" height="105" alt="image" src="https://github.com/user-attachments/assets/8fdf8059-d911-4ac3-8736-a1373b000183" />



cut -d "|" -f 2 file22
## OUTPUT



<img width="435" height="115" alt="image" src="https://github.com/user-attachments/assets/6a61bdaf-2a24-40a8-8f1b-24fa75fd7b18" />



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


<img width="366" height="72" alt="Screenshot 2026-07-26 154737" src="https://github.com/user-attachments/assets/a056c346-73de-4c3d-88dd-772f90bc803f" />



grep hello newfile 
## OUTPUT


<img width="421" height="79" alt="Screenshot 2026-07-26 154552" src="https://github.com/user-attachments/assets/c36c30e8-0353-4a02-a6e5-13f2c4dec10f" />



grep -v hello newfile 
## OUTPUT


<img width="377" height="76" alt="image" src="https://github.com/user-attachments/assets/dee8b31e-fe38-41fd-b940-1ac12d88a894" />



cat newfile | grep -i "hello"
## OUTPUT



<img width="392" height="93" alt="Screenshot 2026-07-26 154917" src="https://github.com/user-attachments/assets/589da4c1-b1c4-4897-8907-fb19059f4fe9" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="438" height="70" alt="image" src="https://github.com/user-attachments/assets/060e790e-fdb9-4af2-aa88-f97701f82525" />



grep -R ubuntu /etc
## OUTPUT


<img width="506" height="230" alt="image" src="https://github.com/user-attachments/assets/a705afcb-bf84-4a3b-8af4-171966b378d2" />



grep -w -n world newfile   
## OUTPUT

<img width="384" height="82" alt="Screenshot 2026-07-26 155325" src="https://github.com/user-attachments/assets/38ec2f14-f359-426f-a8f5-5f4b6f97a695" />



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


<img width="446" height="96" alt="image" src="https://github.com/user-attachments/assets/41cfbd47-b0bb-47bc-89e1-275575ea62b9" />




egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="439" height="74" alt="image" src="https://github.com/user-attachments/assets/5a7a8003-1ce1-44aa-acd5-d7f28e4691ed" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="482" height="99" alt="image" src="https://github.com/user-attachments/assets/95f046d3-066c-46bc-ae76-51ab9779181a" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="412" height="71" alt="image" src="https://github.com/user-attachments/assets/09de67cf-65c5-4708-b7d2-1206fef9bfbd" />



egrep '(world$)' newfile 
## OUTPUT


<img width="445" height="96" alt="image" src="https://github.com/user-attachments/assets/0f64500d-b897-4926-8469-149379200ff6" />



egrep '(World$)' newfile 
## OUTPUT



<img width="469" height="72" alt="image" src="https://github.com/user-attachments/assets/4cd9e7de-fafe-4725-a64d-ade8e9eb7f89" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="427" height="120" alt="Screenshot 2026-07-26 160041" src="https://github.com/user-attachments/assets/d9f56e84-fbfc-4ce4-a272-6ffb5f79990a" />



egrep '[1-9]' newfile 
## OUTPUT


<img width="427" height="73" alt="image" src="https://github.com/user-attachments/assets/4b0fbe70-7196-4179-bb30-f12c50928cdd" />



egrep 'Linux.*world' newfile 
## OUTPUT


<img width="440" height="74" alt="image" src="https://github.com/user-attachments/assets/c095ba2d-7eb1-4bb0-ac90-d04af7f2bdeb" />



egrep 'Linux.*World' newfile 
## OUTPUT


<img width="436" height="76" alt="image" src="https://github.com/user-attachments/assets/a377f0ec-ec3d-4d9d-b171-28e65bc9eec8" />



egrep l{2} newfile
## OUTPUT


<img width="436" height="93" alt="Screenshot 2026-07-26 160320" src="https://github.com/user-attachments/assets/9fabca2c-e28c-432b-b747-0a9b9433d576" />



egrep 's{1,2}' newfile
## OUTPUT 


<img width="423" height="115" alt="image" src="https://github.com/user-attachments/assets/8d1de8c8-8762-43a8-bce4-9af3e6a21dc0" />



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



<img width="556" height="338" alt="Screenshot 2026-07-29 140329" src="https://github.com/user-attachments/assets/01a372c0-f6e7-4862-873c-062e6119bc60" />



sed -n -e '$p' file23
## OUTPUT



<img width="493" height="85" alt="Screenshot 2026-07-29 140409" src="https://github.com/user-attachments/assets/bc4147a4-6cee-4243-a0c3-aba8a1dd3335" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="678" height="268" alt="Screenshot 2026-07-29 140450" src="https://github.com/user-attachments/assets/8210a372-547c-4819-b4bf-7bbb9f29553d" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="618" height="257" alt="Screenshot 2026-07-29 140612" src="https://github.com/user-attachments/assets/bf3669e9-ce3e-4cca-8261-042922db3102" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT



<img width="587" height="258" alt="Screenshot 2026-07-29 140633" src="https://github.com/user-attachments/assets/ca6de836-35bb-46d4-9da2-32b30728e0db" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="561" height="176" alt="Screenshot 2026-07-29 140648" src="https://github.com/user-attachments/assets/69c2215a-64d3-4ea9-9f4e-90e24f589206" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="541" height="130" alt="Screenshot 2026-07-29 140715" src="https://github.com/user-attachments/assets/0f0bb3f2-3187-43a6-b3f4-bd94097ba40e" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="608" height="102" alt="image" src="https://github.com/user-attachments/assets/8bfdb214-b2cf-43e7-a5cc-ba618826a789" />



seq 10 
## OUTPUT


<img width="533" height="309" alt="Screenshot 2026-07-29 141038" src="https://github.com/user-attachments/assets/4a702fdf-7416-4358-ba3e-523749586966" />



seq 10 | sed -n '4,6p'
## OUTPUT


<img width="464" height="133" alt="Screenshot 2026-07-29 141107" src="https://github.com/user-attachments/assets/ae5338f9-ae37-4c9d-a74f-3ec7f1c9ab32" />



seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="504" height="132" alt="Screenshot 2026-07-29 141130" src="https://github.com/user-attachments/assets/ce809b7a-d95a-412f-8993-87d4c4be3a22" />



seq 3 | sed '2a hello'
## OUTPUT


<img width="532" height="157" alt="Screenshot 2026-07-29 141159" src="https://github.com/user-attachments/assets/c01935c7-f5df-4dbb-81c7-65f478a4b674" />




seq 2 | sed '2i hello'
## OUTPUT


<img width="600" height="132" alt="Screenshot 2026-07-29 141233" src="https://github.com/user-attachments/assets/ff39fb03-e738-4038-81ec-f16cd8412c38" />



seq 10 | sed '2,9c hello'
## OUTPUT

<img width="497" height="134" alt="Screenshot 2026-07-29 141413" src="https://github.com/user-attachments/assets/984cb065-9ba3-4441-9035-3e1da21b37cf" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT





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






#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT






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
