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
<img width="257" height="88" alt="Screenshot 2026-04-30 083837" src="https://github.com/user-attachments/assets/8a0f682a-ce3e-4d39-a812-16d0d9098dd6" />

cat < file2
## OUTPUT
<img width="251" height="108" alt="Screenshot 2026-04-30 083903" src="https://github.com/user-attachments/assets/b6550d27-cad1-4e7c-8679-d5aa1fdb1687" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="345" height="48" alt="Screenshot 2026-04-30 083914" src="https://github.com/user-attachments/assets/a570e001-9db1-4aa1-b17b-71417baa7eb6" />

comm file1 file2
 ## OUTPUT
<img width="314" height="137" alt="Screenshot 2026-04-30 083928" src="https://github.com/user-attachments/assets/ad04a594-27d0-4026-9e9b-b7052cb8cee4" />

 
diff file1 file2
## OUTPUT
<img width="300" height="166" alt="Screenshot 2026-04-30 083941" src="https://github.com/user-attachments/assets/af22ce48-dfbf-4ec8-93e5-2bf02af818c9" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
Screenshot 2026-04-30 091001
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
<img width="273" height="83" alt="Screenshot 2026-04-30 091010" src="https://github.com/user-attachments/assets/b17ee0be-2ab1-4cce-9ea6-e2c2dabac58d" />

```


cut -c1-3 file11
## OUTPUT

<img width="241" height="58" alt="Screenshot 2026-04-30 091020" src="https://github.com/user-attachments/assets/4a8b4d53-1039-4326-a72b-777e580caef6" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="288" height="57" alt="Screenshot 2026-04-30 091029" src="https://github.com/user-attachments/assets/d219463f-f177-44d9-a1ab-31e3f1a17514" />


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
<img width="240" height="42" alt="Screenshot 2026-04-30 091308" src="https://github.com/user-attachments/assets/b214fe0c-2be1-4574-a32d-43f6d734643c" />



grep hello newfile 
## OUTPUT


<img width="275" height="45" alt="Screenshot 2026-04-30 091333" src="https://github.com/user-attachments/assets/73edccc2-98ee-49f7-825c-db6cb4d728b5" />




grep -v hello newfile 
## OUTPUT
<img width="275" height="45" alt="Screenshot 2026-04-30 091333" src="https://github.com/user-attachments/assets/4b74dd88-85f3-43de-a7f1-5a53a7a6ecf3" /><img width="331" height="60" alt="Screenshot 2026-04-30 091344" src="https://github.com/user-attachments/assets/8b6bef38-345b-447a-8da2-72175e6884e9" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="331" height="60" alt="Screenshot 2026-04-30 091344" src="https://github.com/user-attachments/assets/19a65e4b-e3a5-4914-8edd-4b0e938ef627" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="337" height="48" alt="Screenshot 2026-04-30 091355" src="https://github.com/user-attachments/assets/22240c0e-c3a1-458e-b0c5-3031056a70dc" />



grep -R ubuntu /etc
## OUTPUT
<img width="886" height="552" alt="Screenshot 2026-04-30 091435" src="https://github.com/user-attachments/assets/4894474c-f998-43bf-9101-2c657f27e3c9" />



grep -w -n world newfile   
## OUTPUT
<img width="314" height="59" alt="Screenshot 2026-04-30 091756" src="https://github.com/user-attachments/assets/73be95f3-ce78-40d3-90fd-f571a6cc87a3" />


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

<img width="329" height="62" alt="Screenshot 2026-04-30 092354" src="https://github.com/user-attachments/assets/ee2e832b-8271-4cac-987b-d8c22e52ee18" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="350" height="60" alt="Screenshot 2026-04-30 092403" src="https://github.com/user-attachments/assets/95b93a6e-64cd-4a29-95f3-4e85319727a2" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="350" height="60" alt="Screenshot 2026-04-30 092403" src="https://github.com/user-attachments/assets/8ca3d89c-5e5a-45c3-ae5e-1e75b12d4dfa" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="312" height="48" alt="Screenshot 2026-04-30 092411" src="https://github.com/user-attachments/assets/7bb871fa-b27f-48c0-a484-959e94b1147d" />



egrep '(world$)' newfile 
## OUTPUT
<img width="292" height="61" alt="Screenshot 2026-04-30 092420" src="https://github.com/user-attachments/assets/92a17361-3d83-489c-be86-55b4da53b30b" />



egrep '(World$)' newfile 
## OUTPUT
<img width="292" height="61" alt="Screenshot 2026-04-30 092420" src="https://github.com/user-attachments/assets/b7c5972f-dbbd-4c46-ae3d-2182c259e4f7" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="313" height="73" alt="Screenshot 2026-04-30 092429" src="https://github.com/user-attachments/assets/294fb172-befa-40ac-9cdb-965e018073bc" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="289" height="51" alt="Screenshot 2026-04-30 092442" src="https://github.com/user-attachments/assets/3716eb91-f601-40bb-8e0d-736ae34cec1c" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="327" height="45" alt="Screenshot 2026-04-30 092449" src="https://github.com/user-attachments/assets/bca4f832-b5d9-41c0-ad4d-5075423cd9a0" />
egrep 'Linux.*World' newfile 
## OUTPUT
<img width="350" height="48" alt="Screenshot 2026-04-30 092755" src="https://github.com/user-attachments/assets/50ad21b7-dca0-45af-b621-1e1335f93280" />

egrep l{2} newfile
## OUTPUT
<img width="247" height="61" alt="Screenshot 2026-04-30 092801" src="https://github.com/user-attachments/assets/251c5ca6-9dd5-4f2d-80f8-dac66b695913" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="277" height="78" alt="Screenshot 2026-04-30 092808" src="https://github.com/user-attachments/assets/ded7df37-fd37-4b3c-a97c-38dac4b9ecf8" />


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
<img width="320" height="160" alt="Screenshot 2026-04-30 092834" src="https://github.com/user-attachments/assets/dfdb0dc2-2adc-48c8-9554-9ec0020864c9" />


sed -n -e '3p' file23
## OUTPUT

<img width="308" height="47" alt="Screenshot 2026-04-30 092841" src="https://github.com/user-attachments/assets/deec5f30-d15e-4678-8e39-1135f08cb129" />


sed -n -e '$p' file23
## OUTPUT
<img width="286" height="49" alt="Screenshot 2026-04-30 092942" src="https://github.com/user-attachments/assets/b3e8c0fb-6fae-42a5-97b3-0cdd0c1e0eb4" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="346" height="148" alt="Screenshot 2026-04-30 092951" src="https://github.com/user-attachments/assets/6de8c5af-110c-4be8-9d40-8df0ba7b9450" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

  <img width="319" height="151" alt="Screenshot 2026-04-30 092958" src="https://github.com/user-attachments/assets/ca9a29be-3f83-4fb8-bffa-0d42da272ae2" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="329" height="154" alt="Screenshot 2026-04-30 093047" src="https://github.com/user-attachments/assets/750d39de-e34d-406b-96f7-463ef9538946" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="344" height="105" alt="Screenshot 2026-04-30 093057" src="https://github.com/user-attachments/assets/8875e4bf-26d3-416d-b70d-a472be001735" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

  <img width="304" height="75" alt="Screenshot 2026-04-30 093213" src="https://github.com/user-attachments/assets/201d0590-12a2-4034-9526-6c8fc919aa89" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="333" height="61" alt="Screenshot 2026-04-30 093226" src="https://github.com/user-attachments/assets/b9270021-eef6-41af-a8eb-7d06067242b2" />



seq 10 
## OUTPUT

<img width="241" height="180" alt="Screenshot 2026-04-30 093235" src="https://github.com/user-attachments/assets/03068731-51e8-456e-acef-f4c36980a273" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="261" height="75" alt="Screenshot 2026-04-30 093346" src="https://github.com/user-attachments/assets/e50329d6-ece6-4221-92e4-1b93b5e085fc" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="276" height="77" alt="Screenshot 2026-04-30 093354" src="https://github.com/user-attachments/assets/6172ba60-e4a2-49f9-a549-a2275d3e5335" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="261" height="93" alt="Screenshot 2026-04-30 093401" src="https://github.com/user-attachments/assets/f54ab558-a231-4ab3-b87e-54d01d33a810" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="294" height="77" alt="Screenshot 2026-04-30 093407" src="https://github.com/user-attachments/assets/6c7671cc-0a40-4312-8ecf-f8e24c8a7028" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="290" height="76" alt="Screenshot 2026-04-30 093416" src="https://github.com/user-attachments/assets/b2a023aa-7bb6-4a93-ba27-30e899eaca6b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="340" height="77" alt="Screenshot 2026-04-30 093457" src="https://github.com/user-attachments/assets/d2c155d8-73ea-461c-bada-f624fec6d62b" />


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
<img width="265" height="105" alt="Screenshot 2026-04-30 093644" src="https://github.com/user-attachments/assets/ee9ba9f5-97c4-40d1-b296-2a5bd9befd13" />


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
<img width="249" height="121" alt="Screenshot 2026-04-30 093721" src="https://github.com/user-attachments/assets/92fe1a7d-c72d-4f2a-bd4e-a4404960622c" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="325" height="75" alt="Screenshot 2026-04-30 093505" src="https://github.com/user-attachments/assets/ec3e3f8f-0027-49d7-9aae-da499250269a" />

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

<img width="313" height="79" alt="Screenshot 2026-04-30 094412" src="https://github.com/user-attachments/assets/b7ac0300-6f7d-4125-b728-0d66077e43ad" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="366" height="79" alt="Screenshot 2026-04-30 094421" src="https://github.com/user-attachments/assets/965fac3e-8cfd-42a6-8250-4d4cac7da93d" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="472" height="558" alt="Screenshot 2026-04-30 094456" src="https://github.com/user-attachments/assets/32d370ae-15ab-45bb-a289-863ec0999499" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="830" height="601" alt="Screenshot 2026-04-30 100836" src="https://github.com/user-attachments/assets/ce8fefb8-6e79-414b-96cf-84a14cefee0d" />

tar -xvf backup.tar
## OUTPUT
<img width="564" height="606" alt="Screenshot 2026-04-30 101039" src="https://github.com/user-attachments/assets/b195e702-54da-4954-a586-32c7a421acca" />

gzip backup.tar
ls .gz
## OUTPUT
 <img width="286" height="36" alt="Screenshot 2026-04-30 101213" src="https://github.com/user-attachments/assets/553abc91-4300-46a3-8f2f-0a9da83cedfe" />

gunzip backup.tar.gz
## OUTPUT

 <img width="286" height="36" alt="Screenshot 2026-04-30 101213" src="https://github.com/user-attachments/assets/7d8bc3d2-c222-4912-8821-55a4a99fa94b" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="505" height="168" alt="Screenshot 2026-04-30 101743" src="https://github.com/user-attachments/assets/90f1afce-3b7f-462f-8c64-9e7d39960937" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="302" height="93" alt="Screenshot 2026-04-30 101842" src="https://github.com/user-attachments/assets/d18af258-4e8c-4426-9e17-0b12c371c8f4" />


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
<img width="341" height="452" alt="Screenshot 2026-04-30 101942" src="https://github.com/user-attachments/assets/f0eee15e-d6b0-482f-a80e-776da8433f24" />

 
ls file1
## OUTPUT
<img width="257" height="44" alt="Screenshot 2026-04-30 102042" src="https://github.com/user-attachments/assets/1c2eef2b-1246-4985-8028-8736c85578a5" />

echo $?
## OUTPUT 
<img width="197" height="44" alt="Screenshot 2026-04-30 102049" src="https://github.com/user-attachments/assets/6a2d0e75-9217-48d2-8a3c-156239af4272" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="197" height="44" alt="Screenshot 2026-04-30 102049" src="https://github.com/user-attachments/assets/1ecd559f-b2f4-49d1-be4d-e33defe4a9a6" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="273" height="94" alt="Screenshot 2026-04-30 102057" src="https://github.com/user-attachments/assets/179976ba-79e2-496d-b0f5-0faf31f6cf73" />


 
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
<img width="307" height="168" alt="Screenshot 2026-04-30 102137" src="https://github.com/user-attachments/assets/7cce507c-c421-4578-8e48-a4321b9e4d58" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="263" height="31" alt="Screenshot 2026-04-30 102252" src="https://github.com/user-attachments/assets/e7858db8-33b9-4611-9d79-4fcb93849117" />



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
<img width="483" height="176" alt="Screenshot 2026-04-30 102311" src="https://github.com/user-attachments/assets/a7398961-ca5e-41e7-b077-7c922d4445e0" />

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
<img width="431" height="286" alt="Screenshot 2026-04-30 102511" src="https://github.com/user-attachments/assets/69cb2d1b-9579-4392-9ee8-819e79b52ee5" />



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
<img width="528" height="61" alt="Screenshot 2026-04-30 103502" src="https://github.com/user-attachments/assets/8d940217-96a5-43ce-a116-e4ad1b669138" />


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
<img width="339" height="42" alt="Screenshot 2026-04-30 103606" src="https://github.com/user-attachments/assets/34261e81-2c0b-4f10-856e-ae8c8d1d99c7" />

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
<img width="506" height="155" alt="Screenshot 2026-04-30 104500" src="https://github.com/user-attachments/assets/f00018fb-60fc-4145-a265-eb2e2ecc43a5" />

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
<img width="506" height="155" alt="Screenshot 2026-04-30 104500" src="https://github.com/user-attachments/assets/b10e3d08-4449-4cbf-85cd-d902d06c4e0a" />


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
<img width="287" height="111" alt="Screenshot 2026-04-30 105052" src="https://github.com/user-attachments/assets/6b9865ce-a79b-47a3-a888-b617d8c8df66" />

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
<img width="267" height="110" alt="Screenshot 2026-04-30 105259" src="https://github.com/user-attachments/assets/6591e198-8bf9-456e-94f5-9b2eec088947" />

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
<img width="284" height="220" alt="Screenshot 2026-04-30 105352" src="https://github.com/user-attachments/assets/2a15b488-28e5-4360-b053-447a0b1c2019" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
 <img width="293" height="77" alt="Screenshot 2026-04-30 105444" src="https://github.com/user-attachments/assets/98c16279-2051-42ab-86a4-82424872a4da" />

 
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
<img width="286" height="88" alt="Screenshot 2026-04-30 105527" src="https://github.com/user-attachments/assets/4156e917-7f4b-4277-bc8b-8eecf0f03319" />
 
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
<img width="323" height="68" alt="Screenshot 2026-04-30 105626" src="https://github.com/user-attachments/assets/002bc1e1-b3a6-4dbd-a8f0-92606c3c0307" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="324" height="63" alt="Screenshot 2026-04-30 105749" src="https://github.com/user-attachments/assets/020f8704-e7d2-4ac4-81a0-6ffa91460770" />



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
<img width="210" height="48" alt="Screenshot 2026-04-30 105845" src="https://github.com/user-attachments/assets/bc9eecb9-64ce-4a73-bfbe-89e3de2fcd9a" />

 
 ./funcex.sh 1 2
<img width="212" height="45" alt="Screenshot 2026-04-30 105907" src="https://github.com/user-attachments/assets/fe155a20-b0b7-4503-a751-4c062f3a286f" />

 
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
 <img width="238" height="78" alt="Screenshot 2026-04-30 105945" src="https://github.com/user-attachments/assets/19103728-00b0-4e1e-a0eb-3a3c2e55166c" />

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
 <img width="245" height="73" alt="Screenshot 2026-04-30 110113" src="https://github.com/user-attachments/assets/a7752777-85ce-4dfd-bce3-fa53cf37baf3" />

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
 <img width="245" height="243" alt="Screenshot 2026-04-30 110213" src="https://github.com/user-attachments/assets/c05fb33f-1af6-42ea-b2c4-095965cad8e8" />

 
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
<img width="252" height="220" alt="Screenshot 2026-04-30 110348" src="https://github.com/user-attachments/assets/22e06866-8484-4560-8b3f-e45ad66711d9" />

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
<img width="255" height="79" alt="Screenshot 2026-04-30 110607" src="https://github.com/user-attachments/assets/203a218b-5304-4495-af20-f1d2f8093a38" />


# RESULT:
The Commands are executed successfully.
