# Write-a-C-program-to-display-PID-and-PPID-using-system-calls-getpid-and-getppid-.-CODE-Wait-NULL
#include<stdio.h>
#include<sys/types.h>
#include<unistd.h>
#include<sys/wait.h>
void main()
{
int pid;
pid=fork();
if (!pid)
{
printf("child process..");
printf("\n\n Child PID :%d",getpid());
printf("\nParent PID :%d",getppid());
printf("\n\nFinished with child\n");
}
else
{
wait(NULL);
printf("\nParent process");
printf("\nParent PID :%d",getpid());
printf("\nchild PID:%d",pid)
}}
Wait(NULL) in the end of else statement.
#include<stdio.h>
#include<sys/types.h>
#include<unistd.h>
#include<sys/wait.h>
void main()
{
int pid;
pid=fork();
if (!pid)
{
printf("child process..");
printf("\n\n Child PID :%d",getpid());
printf("\nParent PID :%d",getppid());
printf("\n\nFinished with child\n");
}
else
{
printf("\nParent process");
printf("\nParent PID :%d",getpid());
printf("\nchild PID:%d",pid);
wait(NULL);
}}
Wait(NULL) in the start of if statement.
#include<stdio.h>
#include<sys/types.h>
#include<unistd.h>
#include<sys/wait.h>
void main()
{
int pid;
pid=fork();
if (!pid)
{
wait(NULL);
printf("child process..");
printf("\n\n Child PID :%d",getpid());
printf("\nParent PID :%d",getppid());
printf("\n\nFinished with child\n");
}
else
{
printf("\nParent process");
printf("\nParent PID :%d",getpid());
printf("\nchild PID:%d",pid);
}}
