# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:
## Developed by :MANOJ K
## Register no :212222223001
## C Program to print process ID and parent Process ID using Linux API system calls


```
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{	//variable to store calling function's process id
	pid_t process_id;
	//variable to store parent function's process id
	pid_t p_process_id;
	//getpid() - will return process id of calling function
	process_id = getpid();
	//getppid() - will return process id of parent function
	p_process_id = getppid();
	//printing the process ids

//printing the process ids
	printf("The process id: %d\n",process_id);
	printf("The process id of parent function: %d\n",p_process_id);
	return 0; }
```












##OUTPUT





![Screenshot from 2024-04-25 15-47-15](https://github.com/Aaron-I/Linux-Process-API-fork-wait-exec/assets/139863034/1dc40bf2-ec80-40a9-b5e8-77240bc47982)









## C Program to create new process using Linux API system calls fork() and exit()

```
#include <stdio.h>
#include<stdlib.h>
int main()
{ int pid; 
pid=fork(); 
if(pid == 0) 
{ printf("Iam child my pid is %d\n",getpid()); 
printf("My parent pid is:%d\n",getppid()); 
exit(0); } 
else{ 
printf("I am parent, my pid is %d\n",getpid()); 
sleep(100); 
exit(0);} 
}
```









##OUTPUT






![Screenshot from 2024-04-25 15-56-24](https://github.com/Aaron-I/Linux-Process-API-fork-wait-exec/assets/139863034/54183136-0e0f-4462-99c5-c89d790770e2)


## C Program to execute Linux system commands using Linux API system calls exec() family

```
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
int main()
{
	printf("Running ps with execlp\n");
	execlp("ps", "ps", "ax", NULL);
	printf("Done.\n");
	exit(0);
}
```
























##OUTPUT




![Screenshot from 2024-04-25 16-03-19](https://github.com/Aaron-I/Linux-Process-API-fork-wait-exec/assets/139863034/f2267de0-50d9-48a0-814e-5d5ff8175b1d)


















# RESULT:
The programs are executed successfully.
