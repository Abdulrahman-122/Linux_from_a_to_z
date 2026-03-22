  1. the Bourne shell : /bin/sh
		- shell -> program for run commands on it
		- there are many shell related to each linux distribution but the default one : bash shell(/bin/sh)
		- there are many shells like : bash, Chsh, ask...
  	- after you open the shell
  		- it should ends with $ (mean you log as user) while that ends with # (mean you log as root)
    ----
 2.cat command;
    <img width="917" height="512" alt="image" src="https://github.com/user-attachments/assets/d9bdd68d-d2f2-4fcf-b3b9-3d0142fb9cd6" />
 - stdin -> standard input-> cat open an interactive shell for you to write anything + then it will repeat that
	- <img width="674" height="266" alt="image" src="https://github.com/user-attachments/assets/5c69e890-7d5c-44f7-b912-68350bf1b4ac" />
 - stdout->standard output -> cat open the content of the file to the terminal through standard output.
	 - <img width="925" height="503" alt="image" src="https://github.com/user-attachments/assets/167b019d-f84b-4e81-9684-e0fd5fa60a38" />
----
ls command
 - show you the list of your files that you made in the directory .
 - <img width="801" height="531" alt="image" src="https://github.com/user-attachments/assets/f834ddc2-d4f8-4221-a38f-92ada9fa9687" />
---
cp command;
	- copy the file to another file or other directory 
	cp file1 file2
	
----
 mv command 
	 - move the file to another directory ..
	 <img width="915" height="245" alt="image" src="https://github.com/user-attachments/assets/5234bcba-bdad-4979-a809-707e66052db6" />

----
touch
	- create new file 
	<img width="799" height="121" alt="image" src="https://github.com/user-attachments/assets/891fbfd3-784b-4640-9d32-a176605ec167" />

---
rm 
	- delete a file from the directory
	<img width="868" height="317" alt="image" src="https://github.com/user-attachments/assets/5b6474b7-e272-42e2-b10b-0a3ea2128307" />

---
echo 
	- show the output to the standard output;
	
----
cd command
	- is used to navigate through directories
	- there are absolute , relative path .
	- absolute path -> start with root or user directory that you want to navigate with
	<img width="938" height="121" alt="image" src="https://github.com/user-attachments/assets/d0674dd3-2509-4d1b-8e67-49d21ae84a23" />

---
rmdir,rm commands
- rmdir -> used to delete an empty directory
- rm -r -> delete directory that has some files in it.
<img width="909" height="367" alt="image" src="https://github.com/user-attachments/assets/77d9b5ab-8419-48c0-a7df-56f040f2adef" />

---
Shell Globbing characters -> *,? 
	- * -> match the whole files in the directory
	- ? -> match one character into the directory
	<img width="942" height="550" alt="image" src="https://github.com/user-attachments/assets/f6922007-cae0-4e1d-a930-a2c0935de063" />

---
grep command 
- matches a text or whatever from a file or a directorey using matching characters
- <img width="948" height="810" alt="image" src="https://github.com/user-attachments/assets/655c5e51-131b-4a1b-ae2b-220802643b3b" />

---
less command
	- divide the long files into smaller ones .
	- by print a short lines of the files at one page then press space to go to the other lines into new page
	<img width="958" height="921" alt="image" src="https://github.com/user-attachments/assets/634ed2d1-2709-4da0-bb52-56974dbbaa4b" />

-----
more command
	- an old one than less
	you can write this command ; cat * | more 
	<img width="911" height="900" alt="image" src="https://github.com/user-attachments/assets/35f3d039-85ad-4841-9429-1c4cd992a352" />

---
diff command
	- show you the difference between first file than second file 
	<img width="935" height="786" alt="image" src="https://github.com/user-attachments/assets/a129259d-ed61-4453-bb1a-942f95a908cf" />

---
file command
	- show you the format of the file
	<img width="773" height="62" alt="image" src="https://github.com/user-attachments/assets/9d5aaff5-511e-4bcc-9ea1-1eb5c3c55e09" />

-----

find command
	- find the file path into the device 
	<img width="821" height="61" alt="image" src="https://github.com/user-attachments/assets/db0f3205-68fc-4f91-8e05-b0a457b1314a" />

----
head,tail commands 
	- show the lines from the file
	- if you used head or tail without -n(num of lines to be rendered) then they will show the first,last 10 lines from this file
	
---
sort command
	-sort the lines of the file in alphanumeric orders
	- you can use ; -n(numeric order) or -r(reverse order)
<img width="939" height="745" alt="image" src="https://github.com/user-attachments/assets/a772e2a4-99c1-4db3-99c8-c7708b6cb520" />

----
passwd command 
	- change the password of the current user
	<img width="598" height="146" alt="image" src="https://github.com/user-attachments/assets/e43805d1-0cb1-4a5a-9d43-613048de707e" />

---
ls -la 
	- show the hidden files like configuration or dot files inside the directory
	<img width="682" height="523" alt="image" src="https://github.com/user-attachments/assets/3fe242aa-750d-45fa-a907-688a5deba051" />

----

Shell variable vs environement variable 
	-shell variables
		-it's a variables that can't be shared as child processes.
		to make a shell variable 
		they are local to the current shell session
		<img width="664" height="95" alt="image" src="https://github.com/user-attachments/assets/8eb980d7-d80b-45e0-856e-7762ecc04f36" />
	- environment variables;
		- it's a list of directories that system uses to search for a command or whatever
		<img width="940" height="154" alt="image" src="https://github.com/user-attachments/assets/4a802d75-7585-4ba6-bccc-d666c66e4070" />
 to see the entire environemtal variables;
	 -hit; env

----
some commands you must know ;
<img width="593" height="295" alt="image" src="https://github.com/user-attachments/assets/43f73927-a998-4f6c-8360-5e1e3bdec3e3" />

----
man command
	-  show you the manual page of the command
	- there are punch of pages for the command 
	- man 1 ls .....
		<img width="608" height="277" alt="image" src="https://github.com/user-attachments/assets/efb5204d-a2d8-40b0-9685-0ad0d0766709" />

you can use ; info command .

----
redirection sign
1. standard output redirection > 
<img width="678" height="507" alt="image" src="https://github.com/user-attachments/assets/8ea3c47a-e289-4997-9ddb-66098f902f97" />

<img width="921" height="620" alt="image" src="https://github.com/user-attachments/assets/30ddb0c5-7191-43e4-b237-33c517cf509b" />

2. standard input redirection <
	-show the input lines to the input redirection.
<img width="849" height="313" alt="image" src="https://github.com/user-attachments/assets/dfd1da96-2ca7-4982-8673-71ae957cfbad" />

---
there are bunch of errors that render when you write wrong commands ex;
some errors
		- file not exist
		- not a directory
		- you are out of space disk
		- operation not permitted
		- segmentation error , bus error
			- if program access to a memory that invalid for it to have -> OS kill it 
			- bus error -> the program trying to access some memory that it shouldn't have.

----
ps command
	- show all the processes on the system .
	<img width="832" height="754" alt="image" src="https://github.com/user-attachments/assets/f47618ae-d603-4e9f-9153-6c776fa3d189" />
		- pid -> show the process ID for the commands
		- TTY -> show the state of the process whether it Running,Starts
		- Time -> time cpu took to run the instructions of the process
		- see some options with ps;
			<img width="565" height="127" alt="image" src="https://github.com/user-attachments/assets/a0e21541-c566-49d2-a710-f7fa374b7a72" />

----------------

kill command
	- terminate the process by using it's ID
	- kill pid or ctrl+C

------
to see the jobs in the system + modify it as background or foreground;
<img width="872" height="292" alt="image" src="https://github.com/user-attachments/assets/2bc62be5-7d16-4788-9c20-53f9c085d06f" />

----

File Modes,Permissions?
	- <img width="438" height="154" alt="image" src="https://github.com/user-attachments/assets/22687639-c758-4a80-9371-72d4c8df9192" />
	- <img width="702" height="114" alt="image" src="https://github.com/user-attachments/assets/f8286d78-9392-476d-b6bb-3c69d5d33137" />
	-<img width="748" height="248" alt="image" src="https://github.com/user-attachments/assets/ee0918f4-99b1-48c7-8376-e3d579a77a68" />
	- <img width="717" height="319" alt="image" src="https://github.com/user-attachments/assets/15cffb75-4216-4879-8dd3-4700344ef157" />
	- you can modify permissions using some numbers;
		- <img width="1069" height="559" alt="image" src="https://github.com/user-attachments/assets/8072d467-2a98-4095-920c-dcf117e75c9e" />
	- <img width="749" height="755" alt="image" src="https://github.com/user-attachments/assets/e2136ace-735d-4d8d-b528-8a5b65f0bb32" />

----
Symbolic vs Hard link;
	- it's a links that indicate to another file into the directory
	- but if you removed the original file the symbolic link will be deleted also
	- while the hard link still there contain the contents of the file .
	why this happen?
	<img width="1117" height="643" alt="image" src="https://github.com/user-attachments/assets/6fca698f-258b-413a-a3f0-33b91d1fa54a" />
because ; soft link points to the original file so when removing the original file -> soft link that you created will be broke down as you will see in the image below
while hard indicate to the hard disk so when removing the original file => hard one will stay safe.
<img width="944" height="412" alt="image" src="https://github.com/user-attachments/assets/47fe471c-1c8d-49b3-a901-c14308ac98ca" />
<img width="657" height="252" alt="image" src="https://github.com/user-attachments/assets/7c88d1ce-18ca-4015-83b4-7721f0dfe79e" />

----

