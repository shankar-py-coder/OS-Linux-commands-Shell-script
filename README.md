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

<img width="580" height="410" alt="WhatsApp Image 2026-07-28 at 2 03 52 PM" src="https://github.com/user-attachments/assets/0395b48d-c5ed-4004-ae0a-5116e06e680c" />


cat < file2
## OUTPUT
<img width="780" height="484" alt="WhatsApp Image 2026-07-28 at 2 03 22 PM" src="https://github.com/user-attachments/assets/f091d35a-5733-4861-81da-0154ac593926" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="410" height="135" alt="image" src="https://github.com/user-attachments/assets/1d9d5e51-312d-4b19-97a2-e3e35a455c10" />

comm file1 file2
 ## OUTPUT
<img width="435" height="230" alt="image" src="https://github.com/user-attachments/assets/446dc81a-1360-4dcc-badf-528549a06878" />

 
diff file1 file2
## OUTPUT
<img width="484" height="276" alt="image" src="https://github.com/user-attachments/assets/5ef25c29-c0d8-40c3-8866-56c1e5008f59" />


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

<img width="536" height="592" alt="image" src="https://github.com/user-attachments/assets/0f38ac67-36fa-4e55-8ded-b40988756212" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="425" height="124" alt="image" src="https://github.com/user-attachments/assets/90186406-e4de-4851-a214-c9ee3268030c" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="514" height="124" alt="image" src="https://github.com/user-attachments/assets/066d532c-8174-4f0d-8739-d795dc1b30af" />


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
<img width="449" height="180" alt="image" src="https://github.com/user-attachments/assets/f3d63b5c-7a13-4ed8-adbc-81e44527a24b" />



grep hello newfile 
## OUTPUT
<img width="391" height="80" alt="image" src="https://github.com/user-attachments/assets/ff17d4cc-1e4c-43e8-9da4-7c6079bb574e" />




grep -v hello newfile 
## OUTPUT
<img width="346" height="85" alt="image" src="https://github.com/user-attachments/assets/5d5ec5a0-15a8-4c08-a503-e37f6b4a16bc" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="429" height="102" alt="image" src="https://github.com/user-attachments/assets/30955fd0-932a-4ffb-8e28-8b8a809cf013" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="439" height="71" alt="image" src="https://github.com/user-attachments/assets/4b041353-14f9-4263-b982-cc843ad414aa" />



grep -R ubuntu /etc
## OUTPUT
<img width="1496" height="723" alt="image" src="https://github.com/user-attachments/assets/99042700-b67a-4f22-82f7-9ee9dc14913d" />



grep -w -n world newfile   
## OUTPUT
<img width="360" height="77" alt="image" src="https://github.com/user-attachments/assets/297f4d77-d3d3-49ff-a5d9-9df03d42a347" />


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
<img width="501" height="278" alt="image" src="https://github.com/user-attachments/assets/77ace868-5294-4bbf-b55e-09c65ac4478e" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="392" height="104" alt="image" src="https://github.com/user-attachments/assets/79c915d2-012e-4f8b-b467-76cb8b42d260" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="464" height="103" alt="image" src="https://github.com/user-attachments/assets/2d68cd5c-7f25-4a97-a0fc-7f0d13629ee0" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="605" height="76" alt="image" src="https://github.com/user-attachments/assets/621aa70f-255b-472d-acfb-9b1da9508abb" />



egrep '(world$)' newfile 
## OUTPUT
<img width="450" height="73" alt="image" src="https://github.com/user-attachments/assets/5b2f7b34-3ea5-4aa8-a1e6-98583d2dfa5e" />



egrep '(World$)' newfile 
## OUTPUT
<img width="410" height="79" alt="image" src="https://github.com/user-attachments/assets/d6ded2ed-4263-41d3-892a-3f3140cf0ec6" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="377" height="96" alt="image" src="https://github.com/user-attachments/assets/984ff9c6-7e1c-429e-a00f-3b828c9dc17e" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="371" height="80" alt="image" src="https://github.com/user-attachments/assets/6436ba64-eb01-45a6-9e49-84f26c72008e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="446" height="72" alt="image" src="https://github.com/user-attachments/assets/026ef092-c787-4ff1-a533-a987b0e6f944" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="382" height="77" alt="image" src="https://github.com/user-attachments/assets/e4af012a-5992-417c-b5e5-ea77d1048e37" />


egrep l{2} newfile
## OUTPUT
<img width="332" height="91" alt="image" src="https://github.com/user-attachments/assets/42b56115-a1e6-477a-aa43-077132c78751" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="406" height="122" alt="image" src="https://github.com/user-attachments/assets/a957da1b-107f-4c6b-8dc8-6710530e485f" />


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

<img width="427" height="345" alt="image" src="https://github.com/user-attachments/assets/cf49c781-73df-40b4-9634-db5a725cb4b5" />


sed -n -e '$p' file23
## OUTPUT

<img width="362" height="85" alt="image" src="https://github.com/user-attachments/assets/8edd2962-fe44-4f49-9930-71dc6f5adb8b" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="651" height="242" alt="image" src="https://github.com/user-attachments/assets/7bb9ee25-1477-451a-a595-a00995ae6a6e" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="472" height="271" alt="image" src="https://github.com/user-attachments/assets/b7653e40-f5df-427a-8e8e-e02be723b7f1" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="597" height="272" alt="image" src="https://github.com/user-attachments/assets/b1f162b9-9774-4b29-817a-e62de78f4d15" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="697" height="201" alt="image" src="https://github.com/user-attachments/assets/c54ea2a3-9c25-4381-8cc8-012b3ddaac4c" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="525" height="150" alt="image" src="https://github.com/user-attachments/assets/247febfd-91b3-47b1-a2b4-37b9a379bd8f" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="442" height="100" alt="image" src="https://github.com/user-attachments/assets/1e02a28e-bf8f-4b5d-bff8-dca3e2f37b12" />



seq 10 
## OUTPUT
<img width="581" height="297" alt="image" src="https://github.com/user-attachments/assets/091d52f0-ff7e-48e9-b5c1-4512aea1117e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="347" height="125" alt="image" src="https://github.com/user-attachments/assets/002c1d28-c3ee-4ea4-8bfe-004622a9ebde" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="366" height="142" alt="image" src="https://github.com/user-attachments/assets/b997aa20-b6c2-48c9-b1fe-c65eb135886f" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="531" height="146" alt="image" src="https://github.com/user-attachments/assets/b8832a25-ca23-42df-bf6e-1bd336450b7c" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="637" height="120" alt="image" src="https://github.com/user-attachments/assets/97f9e5f7-faeb-4215-8ae5-6ac39e77c743" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="427" height="122" alt="image" src="https://github.com/user-attachments/assets/05ce13f4-6034-4bba-abd0-1622436555db" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="511" height="156" alt="image" src="https://github.com/user-attachments/assets/6fd4696b-d677-41b3-b6b2-f31703330789" />



sed -n '2,4{s/$/*/;p}' file23

<img width="365" height="152" alt="image" src="https://github.com/user-attachments/assets/374d40c9-7033-4282-b08a-40a3ab774b32" />

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

<img width="467" height="347" alt="image" src="https://github.com/user-attachments/assets/ab6ac2ee-11f4-4347-b6ef-52f1a77eb24f" />

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
<img width="505" height="372" alt="image" src="https://github.com/user-attachments/assets/cf9cc3cd-d1ea-47f7-955e-7ee879da8284" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="462" height="280" alt="image" src="https://github.com/user-attachments/assets/67666762-8a81-400c-a33a-89424cb76165" />

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
<img width="412" height="122" alt="image" src="https://github.com/user-attachments/assets/caafc6e1-6c5a-4528-a19a-240eed72f83b" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="665" height="125" alt="image" src="https://github.com/user-attachments/assets/933867fc-8b8e-4be6-815b-1299c8a0c63b" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="457" height="270" alt="image" src="https://github.com/user-attachments/assets/4af98ea9-ab5c-4785-91e0-a1f36c831fe1" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="710" height="272" alt="image" src="https://github.com/user-attachments/assets/7e517607-bbe4-4731-86e4-d78d027892f4" />


tar -xvf backup.tar
## OUTPUT
<img width="472" height="272" alt="image" src="https://github.com/user-attachments/assets/7ec06f48-7b09-4bb7-abec-44df8ed43444" />

gzip backup.tar

ls .gz

gunzip backup.tar.gz
## OUTPUT
<img width="635" height="107" alt="image" src="https://github.com/user-attachments/assets/aa5917b2-1fdb-4291-adbc-e10d80ff7b55" />

 
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
<img width="527" height="332" alt="image" src="https://github.com/user-attachments/assets/be388338-8aeb-4f35-bef5-6b31afb049f6" />


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
<img width="637" height="405" alt="image" src="https://github.com/user-attachments/assets/4ea62d38-a09b-45c1-8dcc-d86c8d6f48d2" />

 
ls file1
## OUTPUT
<img width="462" height="80" alt="image" src="https://github.com/user-attachments/assets/9f095b72-4751-4c23-9df6-ee7b7ba58d13" />

echo $?
## OUTPUT 
<img width="386" height="72" alt="image" src="https://github.com/user-attachments/assets/e90620e7-97f0-4a50-bf5e-a1953b383449" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="416" height="76" alt="image" src="https://github.com/user-attachments/assets/8e282845-f59b-423b-9c68-ba7ceec9bdc6" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="416" height="76" alt="image" src="https://github.com/user-attachments/assets/80e5d3db-8f8c-4c47-8843-73dda963e177" />


 
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
<img width="632" height="562" alt="image" src="https://github.com/user-attachments/assets/fff60417-c62c-4755-8e47-a4a782ed9ea7" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="672" height="167" alt="image" src="https://github.com/user-attachments/assets/f52c9073-ef9a-4ca6-aca4-67dbd4654f9d" />


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
<img width="425" height="85" alt="image" src="https://github.com/user-attachments/assets/da0ddfe8-0c17-4a92-8be0-1fd3860643d3" />

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
<img width="480" height="70" alt="image" src="https://github.com/user-attachments/assets/e4c9b7bd-60a5-424f-91b7-1605bee8b2eb" />



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
<img width="282" height="77" alt="image" src="https://github.com/user-attachments/assets/ef51e50c-c1d6-4d9f-9570-e07d32e22a3d" />


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
## OUTPUT
<img width="397" height="187" alt="image" src="https://github.com/user-attachments/assets/f1799cfc-bcd1-4826-bba6-bd6cd1db0d59" />

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
<img width="672" height="102" alt="image" src="https://github.com/user-attachments/assets/a7e475b2-539c-4ee3-a011-4d2c7decbe07" />

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
<img width="357" height="80" alt="image" src="https://github.com/user-attachments/assets/e8070dfd-bc65-4bc7-b9f5-78d04218a107" />
 
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
<img width="491" height="292" alt="image" src="https://github.com/user-attachments/assets/92ef8695-4f01-4b1f-bd26-c9ca920c8345" />
 
 
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
<img width="696" height="190" alt="image" src="https://github.com/user-attachments/assets/82a269e0-9c54-4b50-9837-4dfc5fef56a5" />
 
 
 
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
 
 <img width="811" height="267" alt="image" src="https://github.com/user-attachments/assets/43b4c67a-6eb3-42c0-b2f0-a9b658d45413" />

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
<img width="753" height="188" alt="image" src="https://github.com/user-attachments/assets/40135eca-2d66-4297-b7b7-3ccfc26c71ce" />
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
<img width="753" height="188" alt="image" src="https://github.com/user-attachments/assets/40135eca-2d66-4297-b7b7-3ccfc26c71ce" />

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

<img width="753" height="188" alt="image" src="https://github.com/user-attachments/assets/40135eca-2d66-4297-b7b7-3ccfc26c71ce" />

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
<img width="375" height="212" alt="image" src="https://github.com/user-attachments/assets/2dbb00e4-0d35-40f7-b6be-db5fb3f54d54" />

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
<img width="427" height="183" alt="image" src="https://github.com/user-attachments/assets/aefb6960-2c85-44ae-9b0f-84d9bfe02afc" />

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
<img width="401" height="177" alt="image" src="https://github.com/user-attachments/assets/a98465f5-f251-4679-96e6-e7f0beb12b24" />

 
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
<img width="681" height="410" alt="image" src="https://github.com/user-attachments/assets/64051ba7-2f02-48fa-b476-0f87ffe80d9c" />

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
 <img width="307" height="95" alt="image" src="https://github.com/user-attachments/assets/a16fdd68-fb58-46a3-ac6e-9c2e849d659a" />

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
<img width="307" height="95" alt="image" src="https://github.com/user-attachments/assets/37522372-30f2-4875-a758-1caedb3f83fb" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

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
<img width="801" height="86" alt="image" src="https://github.com/user-attachments/assets/cdf9aba3-d429-4222-9c47-fd0a84a65a5f" />

 
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
 <img width="645" height="137" alt="image" src="https://github.com/user-attachments/assets/9458aeee-c3e1-4857-9b11-1630bab84451" />

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
<img width="637" height="136" alt="image" src="https://github.com/user-attachments/assets/5a9a062d-4e7c-4821-91f0-ff9493466dc8" />
 
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
 <img width="887" height="472" alt="image" src="https://github.com/user-attachments/assets/cfff3970-77d0-46c5-abd8-6255ca2f8c4c" />

 
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
<img width="725" height="472" alt="image" src="https://github.com/user-attachments/assets/e15de244-71f7-485e-befb-5f321be0b3d0" />
 
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
<img width="357" height="123" alt="image" src="https://github.com/user-attachments/assets/fe8688d5-3735-46a0-a6fc-fd3640b42de1" />


# RESULT:
The Commands are executed successfully.
