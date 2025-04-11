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

![Screenshot from 2025-04-11 22-00-04](https://github.com/user-attachments/assets/0f824de7-cf41-4a06-8687-231148159ab3)


cat < file2
## OUTPUT

![Screenshot from 2025-04-11 22-00-37](https://github.com/user-attachments/assets/97c2492d-f316-4332-9fa7-ff866cf80122)

# Comparing Files
cmp file1 file2
## OUTPUT

 ![Screenshot from 2025-04-11 22-01-11](https://github.com/user-attachments/assets/55ecf4d8-8d59-40c9-8596-ddaabc6a41d1)

comm file1 file2
 ## OUTPUT

![Screenshot from 2025-04-11 22-01-38](https://github.com/user-attachments/assets/ac24a5dc-437e-4bf8-be6f-091bb7b8b49c)

 
diff file1 file2
## OUTPUT

![Screenshot from 2025-04-11 22-02-32](https://github.com/user-attachments/assets/61bed82f-385c-4762-862d-444eec3431a2)

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

![Screenshot from 2025-04-11 22-03-19](https://github.com/user-attachments/assets/ba4274ab-8699-41da-a934-247b7b3ee057)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-04-11 22-03-46](https://github.com/user-attachments/assets/dfa7bf19-a4cc-46db-a5fb-199e897a20ef)



cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2025-04-11 22-04-13](https://github.com/user-attachments/assets/909c57a0-19a0-4a4e-9edc-1fbc32b3b106)


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

![Screenshot from 2025-03-06 01-51-33](https://github.com/user-attachments/assets/65d90a04-f613-4ef8-9f8b-9e93fc0bfe5f)



grep hello newfile 
## OUTPUT


![Screenshot from 2025-03-06 01-52-29](https://github.com/user-attachments/assets/e0c6fc9c-fa6b-4563-955b-7ae4e3c50bef)


grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-03-06 02-00-36](https://github.com/user-attachments/assets/64512127-c92d-40bf-9bcb-8774db8fac5c)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-06 02-02-04](https://github.com/user-attachments/assets/5657ef7f-e73b-4a45-b1d4-78a66654b891)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-03-06 02-03-02](https://github.com/user-attachments/assets/053739d4-37b4-45b5-a2cc-c374815b019f)



grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-04-11 23-39-05](https://github.com/user-attachments/assets/2d4a3a32-56af-49b9-a4ee-1eae2df07393)


grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-04-11 23-39-47](https://github.com/user-attachments/assets/032f4344-4d1e-4f7d-9c27-9f700333a7ea)

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

![Screenshot from 2025-04-11 23-17-14](https://github.com/user-attachments/assets/8b868692-ae47-4510-a965-e5764fefc92f)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-13-24](https://github.com/user-attachments/assets/c25f2472-4964-466b-84fb-fc54c26344d0)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-16-28](https://github.com/user-attachments/assets/e2f2464b-74f0-4a9c-acf7-134d35afa2e1)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-17-46](https://github.com/user-attachments/assets/a9785526-3c14-4b81-a24c-ea80f3ccb32a)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-19-49](https://github.com/user-attachments/assets/3b7f4d7d-cfba-4099-a252-0b89362c8958)


egrep '(World$)' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-20-51](https://github.com/user-attachments/assets/4e949855-b1cc-4747-a099-dfec73894759)


egrep '((W|w)orld$)' newfile 
## OUTPUT


![Screenshot from 2025-04-11 23-28-22](https://github.com/user-attachments/assets/5ca20f77-9b20-4f47-a56e-3185f468793f)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-29-01](https://github.com/user-attachments/assets/f55999e3-73cf-44e1-bb2f-af64868624b0)


egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-29-58](https://github.com/user-attachments/assets/c309d840-83fc-4a60-aaa2-8d230a191944)

egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-04-11 23-30-20](https://github.com/user-attachments/assets/b460ab66-da7d-4c77-ab90-ec049c9cb3d2)

egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-04-11 23-30-48](https://github.com/user-attachments/assets/2a04000d-c04e-475c-9e9c-01b175598a45)


egrep 's{1,2}' newfile
##OUTPUT 

![Screenshot from 2025-04-11 23-31-13](https://github.com/user-attachments/assets/56a89783-32b5-4074-a843-bfc80c24ed38)



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

![Screenshot from 2025-04-11 23-44-59](https://github.com/user-attachments/assets/c5962ad0-846b-4a08-9a82-adcea772f417)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-04-11 23-45-24](https://github.com/user-attachments/assets/f712f8c8-8bf6-42f2-b398-74afa1af47ce)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-11 23-45-48](https://github.com/user-attachments/assets/72819ea5-e473-410b-a932-45f13e8c95b4)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-11 23-46-11](https://github.com/user-attachments/assets/7fb191c1-c8bb-4833-ad43-47220cdefa50)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-04-11 23-46-37](https://github.com/user-attachments/assets/fa329079-4d55-4e0e-bd00-24f26d72c29c)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-04-11 23-47-14](https://github.com/user-attachments/assets/4898e27b-4008-4443-801f-cf5cfb05b451)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot from 2025-04-11 23-49-28](https://github.com/user-attachments/assets/dfc22380-246a-4a35-bf2e-638dd2ba040a)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-11 23-48-42](https://github.com/user-attachments/assets/e01f1aaa-bbbd-4571-88fd-251075093e6d)


seq 10 
## OUTPUT

![Screenshot from 2025-04-11 23-49-53](https://github.com/user-attachments/assets/95a340fb-adf6-41bd-995f-5e85cc73c6ec)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-04-11 23-50-17](https://github.com/user-attachments/assets/c8af202d-4d67-43ec-bde6-465d1b21fa9b)



seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-04-11 23-51-43](https://github.com/user-attachments/assets/fd83b652-e7e0-4fd4-ab22-c8a50b3b4a94)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-04-11 23-52-11](https://github.com/user-attachments/assets/f7b9e285-3e31-48e7-9430-d65760b28d33)


seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-04-11 23-52-34](https://github.com/user-attachments/assets/64604e29-a30b-40b1-af76-ab48f888de81)

seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-04-11 23-53-05](https://github.com/user-attachments/assets/ae2737c3-9ba4-4c8b-93ab-c002f1f4d3ba)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-04-11 23-53-27](https://github.com/user-attachments/assets/16fa4822-b82f-407a-944c-42a624e1a301)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![Screenshot from 2025-04-11 23-53-43](https://github.com/user-attachments/assets/6e33c17c-fc96-4ab4-9774-230b1d0f2646)


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

![Screenshot from 2025-04-12 00-18-24](https://github.com/user-attachments/assets/70f5fbbf-dd36-493f-82bc-a6d6618db2d3)


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

![Screenshot from 2025-04-12 00-19-25](https://github.com/user-attachments/assets/ed0e9e13-2e7c-4e39-9200-45b4f1433db6)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![Screenshot from 2025-04-12 00-20-11](https://github.com/user-attachments/assets/6c826001-a5d5-4d8f-8563-be7595a3d551)

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

![Screenshot from 2025-04-12 00-26-36](https://github.com/user-attachments/assets/c39c17c8-8ef0-4095-8ad9-231d8b8709d7)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-04-12 00-26-59](https://github.com/user-attachments/assets/4929346c-cd4b-4ad0-8e9f-41959c682d25)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot from 2025-04-12 00-27-28](https://github.com/user-attachments/assets/2a31ccaf-fb47-4405-a056-fc1100a7820d)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![Screenshot from 2025-04-12 00-36-31](https://github.com/user-attachments/assets/138dba8e-2b56-40f9-8f78-375c6c9576c5)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot from 2025-04-12 00-37-35](https://github.com/user-attachments/assets/f4a3d6f0-c1ce-4e75-8afe-cdf7c4c55e44)


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

 ![Screenshot from 2025-04-12 00-41-12](https://github.com/user-attachments/assets/9d15d8ec-0971-4f5c-855e-d51669936edd)

ls file1
## OUTPUT
![Screenshot from 2025-04-12 00-43-08](https://github.com/user-attachments/assets/b97da5f4-b150-4853-a09f-abf02d4c0318)

echo $?
## OUTPUT

![Screenshot from 2025-04-12 00-43-30](https://github.com/user-attachments/assets/6592b615-a22d-4769-bc45-342e89ffad98)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![Screenshot from 2025-04-12 00-44-22](https://github.com/user-attachments/assets/01b7a530-237f-4cdb-818d-016ca861463f)

abcd
 
echo $?
 ## OUTPUT

![Screenshot from 2025-04-12 00-45-26](https://github.com/user-attachments/assets/da53be04-fb28-41d7-9cc7-910bd6e138af)

 
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

![Screenshot from 2025-04-12 00-47-15](https://github.com/user-attachments/assets/7354947d-c203-4236-90ab-a9f9e4c38d50)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot from 2025-04-12 00-48-09](https://github.com/user-attachments/assets/448bbf7e-26f0-4a7a-a36b-15d83df13a62)


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

![Screenshot from 2025-04-12 00-50-04](https://github.com/user-attachments/assets/0b75304d-082b-44dd-8324-167497048d25)

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

![Screenshot from 2025-04-12 00-51-42](https://github.com/user-attachments/assets/36868439-5a4f-4a21-8b7a-5286ce6e38b0)


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

![Screenshot from 2025-04-12 00-55-25](https://github.com/user-attachments/assets/b25f59c7-4820-4b73-8db3-1e79a87efc3d)


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

![Screenshot from 2025-04-12 00-56-33](https://github.com/user-attachments/assets/0b1c119b-a6e3-40cd-ae01-e577217213f5)



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

![Screenshot from 2025-04-12 00-58-03](https://github.com/user-attachments/assets/466ffbf6-2b4a-4052-b492-651b0fbd2b18)


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

![Screenshot from 2025-04-12 00-59-20](https://github.com/user-attachments/assets/eb80541f-1ffc-42f6-a0c5-a649c46d9878)

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
##OUTPUT

![Screenshot from 2025-04-12 01-00-50](https://github.com/user-attachments/assets/4d4fc667-d7ec-4f24-8be3-ecd5ee0cff83)


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
##OUTPUT

![Screenshot from 2025-04-12 01-02-37](https://github.com/user-attachments/assets/888902d2-4647-4c48-ae64-70355d792f6c)


 
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
##OUTPUT

![Screenshot from 2025-04-12 01-04-30](https://github.com/user-attachments/assets/adea169a-fc23-4965-8121-364117dcfe67)

 
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
##OUTPUT


 ![image](https://github.com/user-attachments/assets/50aed5d3-e65b-48b9-b4f3-e81ca61a1ead)

 
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
#OUTPUT

 ![image](https://github.com/user-attachments/assets/7fd1e62b-9828-4df9-b22e-809be92fb2e2)

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

![image](https://github.com/user-attachments/assets/cebe74ab-c39a-48db-822c-30e771c38787)

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

![image](https://github.com/user-attachments/assets/c024d124-3cb1-4ccb-bb21-9314ad050651)

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
![image](https://github.com/user-attachments/assets/9316db71-cd4c-445a-94f7-670684b0b52e)

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
 
![image](https://github.com/user-attachments/assets/6563f69e-faa2-43d9-9fa5-db4fcec57071)

 
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

![image](https://github.com/user-attachments/assets/a5a95049-b953-48a0-b68f-67e53cb40164)

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

 ![image](https://github.com/user-attachments/assets/267cbbea-6274-4e92-b5bf-3b74b4938423)

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

![image](https://github.com/user-attachments/assets/f9fa8fdd-243a-498d-b7ab-df642a08bbbc)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/ff579d2a-a8ae-473a-8d66-fb6f99f3dfae)


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
./funcex.sh 

 
 ./funcex.sh 1 2

## OUTPUT

![image](https://github.com/user-attachments/assets/d66ebc4a-4bf5-493c-b006-c78a27429dd2)

 
 
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

![image](https://github.com/user-attachments/assets/6d0c2d86-4862-41a9-9584-581feb41c8d0)



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

 ![image](https://github.com/user-attachments/assets/0e9cac0e-3327-4181-a97f-518dbac4c8da)

 
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

 ![image](https://github.com/user-attachments/assets/fa8d3419-2510-4d47-b890-b4c985ae00e6)

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

![image](https://github.com/user-attachments/assets/9da1f97b-8a3f-4477-8f61-33a8af258ff2)


# RESULT:
The Commands are executed successfully.
