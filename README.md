cat > file1# OS-Linux-commands-Shell-scripting
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
<img width="451" height="153" alt="image" src="https://github.com/user-attachments/assets/5681b5ef-f3f2-4744-897f-b30b53ff5647" />



cat < file2
## OUTPUT
<img width="425" height="180" alt="image" src="https://github.com/user-attachments/assets/ccda2229-3f60-458f-b919-8f3be00c98ca" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="388" height="73" alt="image" src="https://github.com/user-attachments/assets/9af7a23a-a162-4426-be25-7f586ff830e9" />

comm file1 file2
 ## OUTPUT
<img width="497" height="222" alt="image" src="https://github.com/user-attachments/assets/f0061d0e-805e-4a97-8e4e-4f36f3301dbb" />

 
diff file1 file2
## OUTPUT

<img width="520" height="277" alt="image" src="https://github.com/user-attachments/assets/2304ad7c-4f23-459d-a63c-0ca4ac4fc950" />

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
<img width="352" height="97" alt="image" src="https://github.com/user-attachments/assets/8f659e2c-584e-4eb2-ae96-34c1a987e950" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="380" height="125" alt="image" src="https://github.com/user-attachments/assets/3ac7405e-0341-4c14-a164-47d0988e487f" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="420" height="128" alt="image" src="https://github.com/user-attachments/assets/11d27dc3-258e-4edd-b8e0-925c02cfc2ea" />


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
<img width="320" height="77" alt="image" src="https://github.com/user-attachments/assets/ff2cc154-736a-403a-9c73-55137ea65f87" />



grep hello newfile 
## OUTPUT
<img width="312" height="80" alt="image" src="https://github.com/user-attachments/assets/f5f91824-8735-4b13-ac01-8d4b191b4afa" />




grep -v hello newfile 
## OUTPUT
<img width="425" height="77" alt="image" src="https://github.com/user-attachments/assets/1fbdf766-37d7-45bb-a5a3-d8a94f4a557d" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="502" height="98" alt="image" src="https://github.com/user-attachments/assets/d4769ccc-8e3c-4887-b3a6-a7228352c4ac" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="432" height="75" alt="image" src="https://github.com/user-attachments/assets/453fe52e-e7eb-41a8-845c-c438934e5f82" />



grep -R ubuntu /etc
## OUTPUT
<img width="808" height="575" alt="image" src="https://github.com/user-attachments/assets/b0d82e91-9e46-4c4d-a88e-f3b7d2ee14cd" />



grep -w -n world newfile   
## OUTPUT
<img width="392" height="97" alt="image" src="https://github.com/user-attachments/assets/931a1e31-9775-4039-b867-b6d37ae78e1a" />


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
<img width="415" height="103" alt="image" src="https://github.com/user-attachments/assets/f57ba203-01f3-4c48-8d45-4136cdefcd64" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="415" height="102" alt="image" src="https://github.com/user-attachments/assets/6e69eb99-6818-40e8-a8a7-37359812f55d" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="450" height="101" alt="image" src="https://github.com/user-attachments/assets/25b650cd-228b-4b1c-8cbd-e8ec6d90e082" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="405" height="77" alt="image" src="https://github.com/user-attachments/assets/26fc5c7e-810e-4408-ad19-44a2749eed55" />



egrep '(world$)' newfile 
## OUTPUT
<img width="420" height="101" alt="image" src="https://github.com/user-attachments/assets/03346422-0120-4fc9-9d8f-eedf9cc352b8" />



egrep '(World$)' newfile 
## OUTPUT
<img width="387" height="75" alt="image" src="https://github.com/user-attachments/assets/fd21730d-fc38-4887-a76e-8f7108dcb614" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="390" height="123" alt="image" src="https://github.com/user-attachments/assets/dd08e746-e5a0-4568-a5fa-e02c7c888067" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="317" height="72" alt="image" src="https://github.com/user-attachments/assets/d670b50f-8c81-4a3a-aa5a-176044f90377" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="486" height="75" alt="image" src="https://github.com/user-attachments/assets/2c3655dd-a8dd-40c4-b577-414199674b4d" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="421" height="77" alt="image" src="https://github.com/user-attachments/assets/6a93e744-fe7a-4f4b-87de-3867fa8823ba" />


egrep l{2} newfile
## OUTPUT
<img width="327" height="105" alt="image" src="https://github.com/user-attachments/assets/d85960f9-4575-49fc-99b1-c0b221886ace" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="350" height="120" alt="image" src="https://github.com/user-attachments/assets/124e308d-a40f-464c-970e-457a51746dd2" />


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
<img width="342" height="68" alt="image" src="https://github.com/user-attachments/assets/199874ca-9098-4fd4-9016-0f879f9b730a" />



sed -n -e '$p' file23
## OUTPUT
<img width="330" height="80" alt="image" src="https://github.com/user-attachments/assets/8306679a-6c3d-46ec-9225-11530151e1b5" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="541" height="253" alt="image" src="https://github.com/user-attachments/assets/9abc3a65-d9dc-455c-a550-da439c9013db" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="470" height="255" alt="image" src="https://github.com/user-attachments/assets/f3bdba6d-a2e7-4884-84d3-03f99f1c814a" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="438" height="256" alt="image" src="https://github.com/user-attachments/assets/51e407b2-bb53-4b03-bb83-bc594e296dd2" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="371" height="176" alt="image" src="https://github.com/user-attachments/assets/6180e2a6-3fe8-439b-a8ee-e2b0ce7b4d85" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="467" height="126" alt="image" src="https://github.com/user-attachments/assets/d78869f0-08b7-4ce4-8b57-c2e3c2eb4510" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="485" height="103" alt="image" src="https://github.com/user-attachments/assets/010fd30f-09bb-4ba5-9923-f800fb657324" />



seq 10 
## OUTPUT
<img width="390" height="305" alt="image" src="https://github.com/user-attachments/assets/c6580866-3bb4-47f7-a3c3-d65fa97ade2c" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="362" height="125" alt="image" src="https://github.com/user-attachments/assets/73383e83-aabe-4dd4-995d-b9387c4fab3b" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="330" height="127" alt="image" src="https://github.com/user-attachments/assets/287a1bb5-67d3-4fa6-91d6-3e73bef9c558" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="325" height="150" alt="image" src="https://github.com/user-attachments/assets/d89be5a4-d224-4c6e-9a25-b7a845a1824c" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="390" height="122" alt="image" src="https://github.com/user-attachments/assets/3965c3e0-77f5-44d4-b4e4-009bafa80d30" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="388" height="120" alt="image" src="https://github.com/user-attachments/assets/ddc84aca-b303-4ff2-b20e-3587511953df" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="435" height="122" alt="image" src="https://github.com/user-attachments/assets/91d640bd-5c54-4c96-a506-54585e328940" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="457" height="122" alt="image" src="https://github.com/user-attachments/assets/203d2088-1eb7-4b9d-8108-f28d14dfd266" />


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
<img width="407" height="172" alt="image" src="https://github.com/user-attachments/assets/f9645e0a-bb87-4f26-bb19-19c987fe33ae" />


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
<img width="427" height="176" alt="image" src="https://github.com/user-attachments/assets/e7e72ed9-e8d4-4a6b-9a22-e1438571abd5" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="675" height="243" alt="image" src="https://github.com/user-attachments/assets/ad3a2e75-169a-440b-8a16-11ea6cefeccf" />

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
<img width="402" height="120" alt="image" src="https://github.com/user-attachments/assets/301175cb-d0fd-4805-8af4-9c768cf725d3" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="485" height="122" alt="image" src="https://github.com/user-attachments/assets/5512fc18-8050-4c08-8245-d057fd2bf2d3" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="805" height="577" alt="image" src="https://github.com/user-attachments/assets/0eb9ff53-c2fb-4534-8e61-b87e8d222aa4" />


tar -xvf backup.tar
## OUTPUT
<img width="658" height="605" alt="image" src="https://github.com/user-attachments/assets/bc7e05d4-b21a-47d9-8101-845f24ef81df" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="338" height="80" alt="image" src="https://github.com/user-attachments/assets/a972fd6d-64f6-430f-a88e-688abe150e97" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="362" height="121" alt="image" src="https://github.com/user-attachments/assets/2b3273ee-5625-43aa-9afa-24c61d2c6f21" />


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
<img width="668" height="395" alt="image" src="https://github.com/user-attachments/assets/86722e2b-7329-4570-9c69-4c56af60a1e6" />

 
ls file1
## OUTPUT
<img width="310" height="75" alt="image" src="https://github.com/user-attachments/assets/bd7b00d5-af0c-4962-b7e8-6e36e774a3b9" />

echo $?
## OUTPUT 
<img width="242" height="75" alt="image" src="https://github.com/user-attachments/assets/7b15adbd-1049-4fd3-a8e6-5095f6dfc1de" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="351" height="77" alt="image" src="https://github.com/user-attachments/assets/4db12780-60ec-43af-997a-cde1860e3fd2" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="326" height="147" alt="image" src="https://github.com/user-attachments/assets/6d88f051-c09c-4a29-ad31-2d813a3b73da" />


 
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

<img width="457" height="277" alt="image" src="https://github.com/user-attachments/assets/729c2f6d-5857-4f9a-80d0-ad1b3bc520c7" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="330" height="95" alt="image" src="https://github.com/user-attachments/assets/86252ea0-d546-446f-9891-398afb69c0f0" />


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
<img width="462" height="81" alt="image" src="https://github.com/user-attachments/assets/f327c726-c64f-43da-9571-80d2ce8be2eb" />

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

<img width="455" height="72" alt="image" src="https://github.com/user-attachments/assets/49486e58-b8be-401a-8ede-087a97f85fa0" />


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
<img width="527" height="101" alt="image" src="https://github.com/user-attachments/assets/843059a9-bfd3-4dd8-92e6-0edf44014ee0" />

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
