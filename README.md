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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/1646b2f9-4943-421b-8abe-b6a61902db40" />



cat < file2
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/65a98579-a960-43fb-98f6-ee94b546f1bf" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/2a3d9e5e-58e7-4053-a480-1c8255162fc9" />

comm file1 file2
 ## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/41bfbad9-e082-4323-9b62-f1dbdf5bf892" />
 
diff file1 file2
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/2782f945-084d-46be-aeab-ab85356df733" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/01f6cb16-bdc5-43b6-9f8f-273b3736b525" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a74e6094-f35b-4f90-b709-593bac8a0e0b" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9ada3a8e-a865-44db-9ca6-41b347df9020" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/dd5650e5-9034-4ac3-9574-4fa28621aaa3" />


grep hello newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/260622b8-2ed8-4873-8e05-1b48343d13a9" />



grep -v hello newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9fb54f4f-18ef-4dcf-9923-579af760ca18" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c150c195-e707-47ab-8e9f-b39b2abd8157" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/08c42433-3d4e-47eb-89de-e6a36c2e0de7" />



grep -R ubuntu /etc
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d9f2c299-4e8c-4bc9-96fb-990fbf2fccf5" />


grep -w -n world newfile   
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c9012d35-35e4-4579-8a2a-8e079230ddab" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/e2fd2647-d1e7-4f85-b72d-13dd5fa2cd1c" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/82c65fba-e906-43e8-93d9-56420f1d0a70" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/7d828bf9-c8ee-49b3-a051-1495bf19fbe9" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a721ebf3-dfc6-4228-8e72-48d89588c0bc" />


egrep '(world$)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/241a84c0-0b90-46b4-b5b3-9d3e991144b0" />


egrep '(World$)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/af055646-2e7f-42cf-bbd9-a28b6122b7e7" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/19baf005-a9f3-4e34-bd0a-753384f9bc6e" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d7492dc8-093b-4803-8faf-101de5c225e8" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/ac43640b-a0b7-4b21-8cbb-b2814f0794ff" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/2e068d3e-7f1e-4853-b6ef-efc310806d9c" />

egrep l{2} newfile
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fdb9b531-33f8-4a23-bfc8-377bc72463ce" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/70f2c30d-606e-4685-b748-de8ce6c787b4" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/0d863285-b995-4b2f-ba0c-f9b6bc71511e" />


sed -n -e '$p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/8ccb1243-fd75-4af8-ab86-3f7981f8aea8" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c5c74ab9-6c01-4f80-900f-748a56a2cbf3" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/893f06ab-a529-4405-9e17-3af4534ca6af" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/b1f85def-d866-4257-8cc4-45a32aac9331" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/84bd186a-8bb4-4259-823f-8edc39eba32c" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4c9be418-bbc4-46f3-8d84-d02594fadd00" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/23b8c6c9-58fe-4df5-b4ee-17320d247b5d" />


seq 10 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a490c29b-810b-4d4f-a781-075f223caa0e" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d370815f-bcca-4e5b-a21d-50d2c45a1cc9" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/bc3e949e-b06d-4b2b-bd95-075894fee37f" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d3eddb56-4536-417b-8158-440bf7192ea7" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/54ef59e7-b99c-484b-ae3a-ad4c1daddadc" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fe95adda-686f-4ca9-ab09-da2ec431ab53" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/dfec85c5-737a-4dd6-b1d9-689b91cefcd6" />


sed -n '2,4{s/$/*/;p}' file23
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9ab09eed-70ef-4efd-a3a5-e7d03e63194b" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/026cc08b-01e8-4480-81b9-01f86179a093" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a543f2c8-113f-4e2e-ab63-40826f34bc07" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/e1740cb3-ed91-4f57-a23c-945af6085a88" />
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d7fd15d2-4493-418f-ab53-adeded97772d" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/3e68a8e7-31ca-461d-abe7-70549a4fbd43" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6563f803-567d-46d7-afb7-fcab8dfd50d4" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/58320c46-d228-42ad-a44c-aeaf8b5d572d" />

tar -xvf backup.tar
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/1e81082b-d5c4-46df-acfa-26d7c313a30f" />
gzip backup.tar

ls .gz
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/8d406817-42b3-40c0-9697-5329d6ee58de" />
gunzip backup.tar.gz
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/2409a0e1-cb52-414f-991e-90e2f6d50682" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/842af01d-bd8f-49cd-ba60-c655698c1c83" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4b0a5759-e792-40a5-a174-1146f1de8de2" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/f1f4f4ce-f32f-4bc1-8a0a-c6eef6ea29e5" />
 
ls file1
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/734eb545-2de0-4b05-81bf-96b8991da775" />
echo $?
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/07dab902-33fb-42ca-ae38-d6489c2954ed" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/ac933555-2252-4a1a-86a4-e169d00d70ff" />

abcd
 
echo $?
 ## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/bd36174c-601a-403c-9a5f-bc8c9c055804" />

 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/802a793e-d59d-4fc1-8309-e237fd1bb252" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/2298a256-fbfe-48aa-9b9b-764e5468b4f0" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/b6e1a23a-111e-4d98-bacb-828eb9e4e351" />
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/bcde7269-41ec-485a-aed4-57fae364fd96" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d2d7c374-f670-4a92-b1e3-da1f73e77c36" />
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/69e3fbf7-09f7-48e0-8f09-21b0b95f28a4" />
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/494774a0-23e3-4032-b9c8-eb197929e182" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/95d9039a-569a-4035-bf39-d18266c1c486" />
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/7a7c3688-4fe5-493b-a1cf-286af82c4d35" />

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
## Output

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9c82063d-88e8-438b-99ca-0793b3f7e2ce" />


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

## Output

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6d054e5d-1fcd-4e16-b1af-5fd67f17dbbc" />
 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/388a0bb2-23e0-4dd5-9641-d25160829bee" />
 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/f9e6d22f-226e-4f97-843a-2c2697fc28e3" />

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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4eba88c3-213a-4b95-8490-b84304dc5bee" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/acb52847-4860-4c5d-b8b4-d4b24de1b640" />

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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9f14f92b-330b-4d3d-acd9-de53d493f3fb" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c7d94493-1a36-4155-8287-4f9527a841a3" />




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
 <img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/36c808c5-ccd8-4110-95f4-bf1556dff739" />


 
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
![Alt text](op-img/79.png)

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/0dd3991b-df77-4984-a329-814689820362" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/7fb776ca-21ff-4c54-8642-2d991eef781a" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/f8cd1748-ef05-4cae-9b5e-3c379c1537db" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/40140f6f-aacb-450c-bde0-ca76f191d057" />
 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/5df21699-ada1-4ca6-9c98-b7fc7d0feb37" />

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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/efc7cc5f-de0d-46d8-8d77-d2cfb04baac2" />

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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/cb83f848-76ab-4724-a83e-7e233456479a" />
 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/617681b6-a3d8-4fae-afe4-16f2eb24e7e0" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/f5b9de81-bca2-4419-81c2-ab31b365db01" />

# RESULT:
The Commands are executed successfully.
