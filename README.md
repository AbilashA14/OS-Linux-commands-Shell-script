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

![360943994-40e6f5fa-a4f3-4c0f-a66a-e9981c4505a1](https://github.com/user-attachments/assets/650d4ad5-ed03-4213-ac87-b29a444eb10a)


cat < file2 
## OUTPUT

![360944149-5ebe1cb7-db88-4e8a-98fc-c93dfe3efffb](https://github.com/user-attachments/assets/817b61e7-1855-47f8-b18b-fd8619f6d452)


# Comparing Files
cmp file1 file2
## OUTPUT 

 ![360944188-1dd302e8-8015-4dd8-b4f4-f738df5b0339](https://github.com/user-attachments/assets/0df1e500-788a-4148-8fe9-20f28443b35d)

comm file1 file2
 ## OUTPUT

![360944265-c807df21-856f-4f95-b63a-89ebc2be45f8](https://github.com/user-attachments/assets/5160cef7-88b2-414f-883e-08ffc05ec2eb)

diff file1 file2
## OUTPUT

![360944316-1fdb9bb5-fdb7-48d2-9ddb-fe0ccc0942f2](https://github.com/user-attachments/assets/0aa4f81e-2fd6-4c5b-85a6-a8327a5479b8)


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

![360944409-54e50794-9ec8-4d96-b430-9023cd15c386](https://github.com/user-attachments/assets/b508d219-d7b6-41bb-9edf-d0cda24de41a)



cut -d "|" -f 1 file22
## OUTPUT

![360944445-33b0903d-0a95-46b7-a4ed-b7e8241cb1b9](https://github.com/user-attachments/assets/064eb015-9f16-49b1-9e01-8dde73b1798a)


cut -d "|" -f 2 file22
## OUTPUT

![360944504-08154368-4ff3-4257-9ecc-9395b5d3fb85](https://github.com/user-attachments/assets/fe1f9c7d-8875-417e-863b-cbd75723104c)


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

![360944564-86a71d8d-0203-4a32-9614-5e2262cfca7a](https://github.com/user-attachments/assets/65273ced-0109-4d3e-a65b-8a264e5d4523)


grep hello newfile 
## OUTPUT


![360944645-55da10fa-a0c3-4f70-a6f2-5f65f44715c5](https://github.com/user-attachments/assets/0af1d228-3a8b-4882-8a1f-62816c04403c)


grep -v hello newfile 
## OUTPUT

![360944670-9d50d0d6-b957-4713-892f-d1bd08efe073](https://github.com/user-attachments/assets/5a5964e2-0d8a-4a7e-9cb1-707da5012f31)


cat newfile | grep -i "hello"
## OUTPUT

![360944726-0f67ab3d-fe1e-4ae1-833f-53bfdcb40d4f](https://github.com/user-attachments/assets/38ff92b5-40a6-424e-a813-478a9789b780)



cat newfile | grep -i -c "hello"
## OUTPUT

![360944787-71168c8f-570c-454f-9342-9c1817d46a6a](https://github.com/user-attachments/assets/d5a0a503-30f5-4a49-8de4-80b6760fe784)



grep -R ubuntu /etc
## OUTPUT


![360944830-533ef281-c0d7-4d85-b359-b5f97f51f822](https://github.com/user-attachments/assets/e752ae41-257b-449f-be51-6aa3237439ab)

grep -w -n world newfile   
## OUTPUT

![360944957-ce4536ce-e38c-4b1d-97d0-7606e9b196d5](https://github.com/user-attachments/assets/731d2a0e-b333-4a52-ac01-c891b3084e61)


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

![360945026-38200c42-1076-4eee-be92-ceab9fbd2182](https://github.com/user-attachments/assets/e65a76c3-5876-4f19-bb40-61b7de056746)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![360945061-8ed4973c-f772-4f44-a7e8-b2ed46e16547](https://github.com/user-attachments/assets/fcac6006-2b8a-4256-9e63-78d468752923)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![360945080-021b37ef-adb4-4362-a71e-bf2c5c1f03aa](https://github.com/user-attachments/assets/e854d1ca-48e3-4331-8976-164923012d6e)


egrep '(^hello)' newfile 
## OUTPUT

![360945226-b5f9b4e5-bbcc-4673-be81-43ac2a2802ae](https://github.com/user-attachments/assets/ade352c2-57de-4ce2-b8f0-90373a95da46)



egrep '(world$)' newfile 
## OUTPUT

![360945271-7febb670-6206-499c-97ad-901e628f18c5](https://github.com/user-attachments/assets/fd53d896-fe3e-4346-8bf3-6d7f724d59b0)


egrep '(World$)' newfile 
## OUTPUT

![360945300-e469480d-0756-4e8f-932e-a14a2c6c3b46](https://github.com/user-attachments/assets/2e469c3f-63c7-44f5-8b71-7dfc5bdd035e)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![360945421-a2e758d2-a29b-49af-b188-07ee6192f577](https://github.com/user-attachments/assets/1d90e5dd-0f11-48af-b27b-35f37170552b)


egrep '[1-9]' newfile 
## OUTPUT

![360945478-061da7e0-46bf-4cd3-855f-1d7330198c75](https://github.com/user-attachments/assets/50937ca7-e446-4c75-b4ce-77b346337a72)


egrep 'Linux.*world' newfile 
## OUTPUT

![360945652-4dab6534-851b-4443-ac25-cee47eee13e8](https://github.com/user-attachments/assets/081bf381-6e9f-4386-899b-073b8e7d0716)

egrep 'Linux.*World' newfile 
## OUTPUT

![360945673-acdc9de9-0cde-4264-9f40-e159e243ab7c](https://github.com/user-attachments/assets/a1fede0f-bf6f-43c4-bdb3-5b783d714ef6)


egrep l{2} newfile
## OUTPUT


![360945697-91a4f569-d546-43d6-ac4e-0e2a0ceb2b69](https://github.com/user-attachments/assets/63697ec7-7927-48ba-8879-5dee36b4026d)

egrep 's{1,2}' newfile
## OUTPUT 

![360945744-8512a714-94c0-4ca6-a048-0efb0049fb75](https://github.com/user-attachments/assets/97c3655b-b103-4cf8-ab1e-4ad69f75c35f)


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

![360945859-4c4e38ed-8912-4c87-af1b-ef438a7c4ccb](https://github.com/user-attachments/assets/5f0e2502-d4d9-4c55-8bc3-65f341fe6e5d)


sed -n -e '$p' file23
## OUTPUT


![360945905-1b76ec00-7f64-4c96-811d-20865d193162](https://github.com/user-attachments/assets/5cb944e4-1fd8-42c2-b5c4-8a0908bd6363)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![360945943-d6845d48-f9cb-4fe5-bab5-fa2d2841a06c](https://github.com/user-attachments/assets/a4f4ac10-6a8c-47f0-9bb7-e1531a4ba161)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![360946036-60551625-d7f3-44ff-902f-8c3bd65d9b67](https://github.com/user-attachments/assets/d66ba1d3-0675-47e8-8af7-4df9da61ef03)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![360946074-7f49f457-5de4-4314-ad39-67ac016f58ac](https://github.com/user-attachments/assets/56240eb5-760f-46e5-8880-8ce7953d6a05)


sed -n -e '1,5p' file23
## OUTPUT

![360946111-5a3d48e5-911b-4b2a-a285-101a5851b3b6](https://github.com/user-attachments/assets/2e8cf5df-7441-4e58-85e9-7089621f2f56)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![360946173-63f18d81-e155-42b6-94c5-6e039216033a](https://github.com/user-attachments/assets/2d676b9d-e78e-4295-ad04-8122463a9f30)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![360946199-87346f54-c25b-46f1-87fc-f2846c9e00d0](https://github.com/user-attachments/assets/cd1da025-9792-4423-834a-24c074111d85)


seq 10 
## OUTPUT

![360946245-4dfe0af0-d189-4d5f-853b-1ea04ce72d61](https://github.com/user-attachments/assets/4ab22473-6ab4-4108-a895-cdd028eccb8e)


seq 10 | sed -n '4,6p'
## OUTPUT

![360946290-ab792785-d5f9-484c-a381-cae83c3bf461](https://github.com/user-attachments/assets/70c7842c-0713-4457-b9e3-c8f8995f5059)


seq 10 | sed -n '2,~4p'
## OUTPUT


![360946347-fcb332d4-4f03-4888-9335-d40ab3206f96](https://github.com/user-attachments/assets/e7e87e22-e64e-430c-896a-7426ebeb82bd)

seq 3 | sed '2a hello'
## OUTPUT

![360946480-06a0aba8-b26c-4535-b6f6-cc4d5ef85522](https://github.com/user-attachments/assets/88166fe9-8a6a-4291-bd25-506a37f44185)


seq 2 | sed '2i hello'
## OUTPUT

![360946517-322ea214-7ac6-4970-8bab-e33cd0f7fa3c](https://github.com/user-attachments/assets/23554152-1a0d-4988-9425-f910b0aaaade)


seq 10 | sed '2,9c hello'
## OUTPUT

![360946555-e846f591-117b-4b70-93ae-1b62f957a819](https://github.com/user-attachments/assets/e24ac769-b067-4832-a93e-6055db42a59b)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![360946555-e846f591-117b-4b70-93ae-1b62f957a819](https://github.com/user-attachments/assets/9abd0a61-6253-4921-919f-711c90821e20)


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

![360946621-8c59beaa-10d2-4126-a3d6-8f8110e01819](https://github.com/user-attachments/assets/c9a8cf0d-9dee-4ccf-ac77-8c41afcac5b4)

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

![360946691-d46f54c3-e9a5-4a9d-b939-b0c67c7df97d](https://github.com/user-attachments/assets/2357806a-1803-4205-9231-f885ae2d9895)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![360946845-f4a4cd3b-3189-41d7-8748-3eae9727ab17](https://github.com/user-attachments/assets/005f0209-ddd8-4851-84f6-4ef8207d0923)


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

![360946949-fe1fb5c8-0d86-4e53-b041-ed34ff42a59a](https://github.com/user-attachments/assets/e5225d94-9eb2-48de-a9b6-e7efe01d3d3c)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![360947000-08b1633c-2238-4556-81cf-2b6ddea314b1](https://github.com/user-attachments/assets/42dc80f0-4651-4523-8787-63574de1fa47)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![360947054-f991f1e6-571e-4eeb-93d4-ba3017e4a5fe](https://github.com/user-attachments/assets/24e242e0-fd01-461f-a6d9-56c1d2d89a64)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![360947108-0e84e156-e3e6-4e87-9891-095deee205a3](https://github.com/user-attachments/assets/da4ad4fe-07f0-4b40-904b-6709eacb061d)


tar -xvf backup.tar
## OUTPUT

![360947161-b2174362-fb53-4e4a-b6ea-168b5104f8aa](https://github.com/user-attachments/assets/5098bba1-4bfe-40be-8c4d-e03de6c5e6b2)
gzip backup.tar

ls .gz
## OUTPUT

 ![360947297-a1df8f02-49e0-4357-ac3c-aa8f43383e05](https://github.com/user-attachments/assets/48b8d251-9449-484d-8c46-8efae0785582)

gunzip backup.tar.gz
## OUTPUT

 ![360947329-134e6655-9b8b-45fb-8a1e-ce4c9f07f4bb](https://github.com/user-attachments/assets/2ddc44af-2ae2-47e4-967f-55916663a6d7)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![360947421-98dba1e9-1cbe-4f70-83d1-8897562a91ee](https://github.com/user-attachments/assets/e05bafa6-da9c-474d-a4ec-08b51473a462)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![360947500-2c42990b-fc7b-411f-8a38-334b5e691bac](https://github.com/user-attachments/assets/cd357656-4256-4dd4-9efa-e51606d4302f)


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

![360947551-1a4b902c-d88b-403f-9b42-dbf075d70264](https://github.com/user-attachments/assets/6ec6c3fd-33d0-4aab-b964-bb9b4d646548)

 
ls file1
## OUTPUT

![360947603-7ea4c54c-bacf-49ac-a433-694ba5c1b286](https://github.com/user-attachments/assets/6bdfd928-ed5f-4d2e-aace-195e4e8c591f)


echo $?
## OUTPUT 


![360947671-403f62bc-dfc9-4da3-b99b-0621acd17571](https://github.com/user-attachments/assets/6b354831-2f3b-43d6-9dc7-9d4585dc229e)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 


![360947671-403f62bc-dfc9-4da3-b99b-0621acd17571](https://github.com/user-attachments/assets/0bf6456d-6d9e-47c7-88fa-eb50f7b6d986)

 
abcd
 
echo $?
 ## OUTPUT

![360947716-8b288ef9-fe00-41a9-8845-9e9730f26b29](https://github.com/user-attachments/assets/1fcf3480-19c1-469e-8810-10c18c32020b)

 
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

![360947760-3df7ed21-c154-4cd3-89a6-285ead81b28b](https://github.com/user-attachments/assets/19d432a4-a6ed-4c2e-85a6-f5b0125c990a)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![360947805-1045ad7d-9745-4464-82e3-d76012b3e761](https://github.com/user-attachments/assets/28f20152-483c-468f-901d-73148787ca13)

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

![360947858-4b930435-4abb-40cd-a088-f4cab02bad4c](https://github.com/user-attachments/assets/62184b0d-4f58-4716-a270-dd9d09241553)


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

![360947904-24322a45-c048-4a66-bd8d-ea749c611486](https://github.com/user-attachments/assets/dfb973ab-eb2e-4568-870f-d1b6f126ac13)


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

![360947994-b24eb56c-c19f-4e02-bc45-11f20f5cbede](https://github.com/user-attachments/assets/ad6f0890-5451-48ea-ab6b-0cce625a8f17)

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

![360948254-b01445b3-9206-4083-af24-4d1cfc2502d4](https://github.com/user-attachments/assets/2ba436f0-a8a4-4ba8-ba5e-6b481307943b)


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
![360948318-cd1aa62a-067f-459c-81be-39919a9daa1a](https://github.com/user-attachments/assets/02505663-543b-42ae-b978-ffaf43e879c0)


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

![360948454-2a35a23e-6e64-4fc6-b959-f377b66acf25](https://github.com/user-attachments/assets/e8f2dc5e-e21a-43b4-aa50-31959dfcba50)


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

## OUTPUT

![360948737-620b3c00-a8a5-4ccd-9989-b1b2fe27f4dd](https://github.com/user-attachments/assets/98ad3690-b4da-45a7-97b3-1548fb2d3ecd)


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

 ## OUTPUT

 
 ![360948818-eb20e411-016f-4f6f-baef-16787a7d30f7](https://github.com/user-attachments/assets/8e6510a0-5883-4132-90b9-a23e9dee90b2)

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
 
 ## OUTPUT

 ![360948873-ef4144dc-a5c2-46f1-b799-40cb12073d3e](https://github.com/user-attachments/assets/d4219975-39e6-4b11-b616-b77a7029603d)

 
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

 ## OUTPUT
 
![360949009-4e76d522-4f16-454a-954d-f796f775aaa3](https://github.com/user-attachments/assets/d3185076-dd07-446b-b3c0-c724fa26cddc)

 
 
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

## OUTPUT

![360949326-a6b24ec4-7bb2-4bde-a721-c597ef75f674](https://github.com/user-attachments/assets/4d43eb26-b126-4cbf-a1b9-ddb62ac1e34b)

 
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
![360950137-6e44d87a-137a-4d79-9cc2-6e7ef6011eaf](https://github.com/user-attachments/assets/95d6ae0c-0560-4a3d-ae20-4d840cc79d3c)


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

![360950249-7934026f-f4b3-449f-91ee-247abb2eff01](https://github.com/user-attachments/assets/2aca72dc-9d1a-4448-8835-61d506ae9f29)

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

![360951117-78654c91-5e21-4518-89c0-b1a3e2696fd5](https://github.com/user-attachments/assets/51e07bf8-a425-4c87-a5e2-a1fe54461a29)


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


![360951033-cc0f4d8d-faf2-4639-9394-481d65f8213f](https://github.com/user-attachments/assets/cdaee156-47a9-4487-917f-c0169e8d7451)

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

 ![360950620-d08497a9-2281-4004-8b91-2de581c7c0b3](https://github.com/user-attachments/assets/c622c43f-f8ed-43b8-b925-3013bddc665b)

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
![360951270-dba1e608-c664-454e-bfbe-2eb9e1a01ec4](https://github.com/user-attachments/assets/1b3809cb-4f2e-41cb-8c1f-cac075da51b2)



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

![360951370-39ac29cf-8e3b-4e71-bc7b-fb80c44561b9](https://github.com/user-attachments/assets/fe0985a7-4251-4ce9-9ba8-ac9579917bb5)

 
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

![360951568-78d106b5-349f-41b9-be1c-7b423b660559](https://github.com/user-attachments/assets/7bcc1843-71b0-4dde-aaeb-03e240728abc)




 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![360951370-39ac29cf-8e3b-4e71-bc7b-fb80c44561b9](https://github.com/user-attachments/assets/dc0fcffa-68f9-4ce0-94e9-b26f1b1e2a85)


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

![360951568-78d106b5-349f-41b9-be1c-7b423b660559](https://github.com/user-attachments/assets/42a16419-e03e-45dc-b118-72e69227ce33)

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
![360951870-6bbf25ff-deed-4b7a-9b0b-6337b956e486](https://github.com/user-attachments/assets/df907ef4-4e20-4c0f-911b-a21a48610a3d)


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
![360952103-1838e628-eff1-489a-8332-f70bb34bf5fe](https://github.com/user-attachments/assets/6ae7b68b-4040-4569-b3d5-915a28e4da5a)

 
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

![360952177-22c0ccff-9fde-4e3a-a259-da97c8afbd71](https://github.com/user-attachments/assets/a14fa77d-d277-49fe-acb7-e7d8e3b12ddb)


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

![360952296-72da8202-017c-4613-88b0-d0aa3f4a390b](https://github.com/user-attachments/assets/0827f5fd-9846-42ed-a37b-14af09905411)

 
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
![360952338-1977daeb-d020-43ab-8768-4342aaf122fd](https://github.com/user-attachments/assets/bc5442d8-0cff-4ab6-be57-6c65003c278a)


# RESULT:
The Commands are executed successfully.
