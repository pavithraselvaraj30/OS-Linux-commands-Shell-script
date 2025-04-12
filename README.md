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

cat < file2
## OUTPUT


![WhatsApp Image 2025-04-07 at 09 39 41_97605f01](https://github.com/user-attachments/assets/161c6fa3-3d46-46f9-bc19-b052848b4b7e)


# Comparing Files
cmp file1 file2
 
comm file1 file2
 
diff file1 file2
## OUTPUT

![WhatsApp Image 2025-04-07 at 09 41 33_de0410a0](https://github.com/user-attachments/assets/b3dd94f1-a9b8-49aa-b1c6-e8c556a5381f)


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

![WhatsApp Image 2025-04-07 at 09 43 27_d6f48155](https://github.com/user-attachments/assets/bca1143b-a14d-49e1-994c-8f732085c421)



cut -d "|" -f 1 file22
## OUTPUT

![WhatsApp Image 2025-04-07 at 09 45 34_116455f5](https://github.com/user-attachments/assets/89d804d2-28e5-4b50-ad86-b36c75185bee)


cut -d "|" -f 2 file22
## OUTPUT

![WhatsApp Image 2025-04-07 at 09 45 09_8a419224](https://github.com/user-attachments/assets/8798d865-a9d7-4d52-b150-643a8c4e08b4)


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

grep hello newfile 
## OUTPUT
![Screenshot 2025-04-12 060005](https://github.com/user-attachments/assets/5e09bd80-f1ed-43a8-938b-b59104b22cff)


grep -v hello newfile 
## OUTPUT

![Screenshot 2025-04-12 060237](https://github.com/user-attachments/assets/e48ce1fb-28aa-4439-bae3-03e1ffe62e77)


cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-04-12 061141](https://github.com/user-attachments/assets/f64621f3-3843-4c08-b523-a7e1e296ced5)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2025-04-12 061225](https://github.com/user-attachments/assets/2c5fd4d1-98a7-4433-9901-3214b600bdcc)




grep -R ubuntu /etc

grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-04-12 061343](https://github.com/user-attachments/assets/a3465197-9238-4ee7-b8b6-6f4439e522ea)



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

![WhatsApp Image 2025-04-08 at 08 10 41_f6977e9e](https://github.com/user-attachments/assets/b499fe65-f2eb-4a37-a74f-2af3027ed3bd)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 11 20_b47abca7](https://github.com/user-attachments/assets/eb7ac93e-47a4-4de5-8f1b-4372af79070a)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 11 37_54015bcf](https://github.com/user-attachments/assets/eea7e858-b138-4295-9ec7-61ae295f1204)



egrep '(^hello)' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 11 57_2b64bef1](https://github.com/user-attachments/assets/718fc23a-2dad-4c7b-b7d6-3a6189b4eadb)


egrep '(world$)' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 13 49_bb099aff](https://github.com/user-attachments/assets/86eb32a8-f700-4967-be9a-418cdbd94a2f)


egrep '(World$)' newfile 
## OUTPUT
![WhatsApp Image 2025-04-08 at 08 14 48_d57a1588](https://github.com/user-attachments/assets/0be5d7c9-51be-4390-a05e-254a04c28481)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 15 09_fe0354cf](https://github.com/user-attachments/assets/2b337831-6639-44ea-961a-7fad7e1d711b)


egrep '[1-9]' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 16 13_81b57138](https://github.com/user-attachments/assets/dacd0bf4-0869-4674-b2a7-1ea7d9211898)


egrep 'Linux.*world' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 22 01_51aa5ed5](https://github.com/user-attachments/assets/f7b83608-47e4-4aac-b4c9-949dcc477518)


egrep 'Linux.*World' newfile 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 23 22_304b6541](https://github.com/user-attachments/assets/4a24b55e-f55f-4809-aec7-866a14e9f00d)


egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 24 02_8e99308d](https://github.com/user-attachments/assets/ea9086d6-dc9e-4bdc-8aaf-8fd31bdc6189)


egrep 's{1,2}' newfile
## OUTPUT 

![WhatsApp Image 2025-04-08 at 08 25 33_306f88ba](https://github.com/user-attachments/assets/62c932fa-2249-481c-a8c8-958c916c043c)


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

![WhatsApp Image 2025-04-08 at 08 31 24_ea65b5a1](https://github.com/user-attachments/assets/fd95df73-5689-42d1-bba3-16a3ca06f822)


sed -n -e '$p' file23
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 31 47_7d947078](https://github.com/user-attachments/assets/531dd4c0-4eb1-4ffa-9a92-7420997ad59a)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 32 33_333fc2b8](https://github.com/user-attachments/assets/8524d56d-4cc6-4288-9082-c359bbd28fd4)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 32 10_076e6451](https://github.com/user-attachments/assets/a683b055-cb02-4726-8184-d12c8cbd217d)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 32 50_6711cd70](https://github.com/user-attachments/assets/6c002225-249b-4b2e-8315-88acc6feff1d)


sed -n -e '1,5p' file23
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 37 54_5c5c39f6](https://github.com/user-attachments/assets/5306a005-b389-48b8-9118-cd96e3906bcf)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 39 48_2176af98](https://github.com/user-attachments/assets/4727dec9-1ffa-4229-bab9-58ae2c1567a8)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 40 15_284dee42](https://github.com/user-attachments/assets/574ba3d2-119e-46a6-bfcf-30af8a67ad86)


seq 10 
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 41 03_e553fd49](https://github.com/user-attachments/assets/3b60cbcf-439d-4477-aaf1-21373d121154)


seq 10 | sed -n '4,6p'
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 41 41_5bf69e79](https://github.com/user-attachments/assets/39917015-355e-419c-afc0-caf5e6a8898c)


seq 10 | sed -n '2,~4p'
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 41 58_94b9e82d](https://github.com/user-attachments/assets/8582f81d-138e-4b72-b40d-fce5e2132f25)


seq 3 | sed '2a hello'
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 42 15_6122954f](https://github.com/user-attachments/assets/9959b05d-e92f-401b-b5c7-527b3e850382)


seq 2 | sed '2i hello'
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 43 21_d77c76a3](https://github.com/user-attachments/assets/7c4c6a34-e722-4efc-8bc0-41c601b49fb4)


seq 10 | sed '2,9c hello'
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 44 04_35f5a7a7](https://github.com/user-attachments/assets/9a6ff6e5-cbaa-4c23-8e63-9e9b6d761449)

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
![WhatsApp Image 2025-04-08 at 08 46 58_0a0814b0](https://github.com/user-attachments/assets/5c577ec8-7df1-4893-936a-87c5c6a4f0f7)

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

![WhatsApp Image 2025-04-08 at 08 47 34_f09a2404](https://github.com/user-attachments/assets/aa6edf91-baf0-43d9-a048-4e0ee30cdae1)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![WhatsApp Image 2025-04-08 at 08 48 11_55fded9d](https://github.com/user-attachments/assets/58086596-7123-44b6-a208-550113af1733)


#Backup commands
tar -cvf backup.tar *

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar

tar -xvf backup.tar

gzip backup.tar

ls .gz
## OUTPUT
 ![WhatsApp Image 2025-04-08 at 08 48 43_e91048d0](https://github.com/user-attachments/assets/fb688309-70a7-4a5b-908c-cdeeba77f951)

gunzip backup.tar.gz
## OUTPUT
![WhatsApp Image 2025-04-08 at 08 49 05_93eb5311](https://github.com/user-attachments/assets/11ae6ae1-7f8e-4a87-a1e1-7e5194d797cf)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![WhatsApp Image 2025-04-08 at 08 49 20_ee461175](https://github.com/user-attachments/assets/1e006602-7156-4149-b666-1c9a3ce57cf3)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![WhatsApp Image 2025-04-08 at 08 49 54_aa57fdfd](https://github.com/user-attachments/assets/768a0ee7-62eb-4bb9-883b-88689052af73)


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
