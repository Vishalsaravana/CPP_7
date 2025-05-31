# QUEUE APPLICATION USING LINKED LIST

## PROGRAM STATEMENT:

To write a C++ program to implement FCFS algorithm(no of.process p1,p2 and p3 and its burst time are 10,5 & 8) find out waiting time of the process.

## ALGORITHM:  

1.	Start the program.
2.	Initialize Variables: Define arrays for burst time (bt), waiting time (wt), and turn-around time (tat).
3.	Input Burst Times: Set burst times for 3 processes (e.g., 10, 5, 8).
4.	Calculate Waiting Times: For each process (except the first), sum the burst times of the previous processes.
5.	Calculate Turnaround Times: Add burst time and waiting time for each process.
6.	Display Results: Print process number, burst time, and waiting time for each process.
7.	End the Program: No average calculation needed.

## PROGRAM:
```
#include<iostream> using namespace std; int main()
{
int bt[20],wt[20],tat[20],i,j,n,total=0;

n=3; bt[0]=10,bt[1]=5,bt[2]=8; wt[0]=0;
for(i=1;i<n;i++)
{
wt[i]=0; for(j=0;j<i;j++)
wt[i]+=bt[j]; total+=wt[i];
}

total=0;
cout<<"Processes BT time WT time"<<endl; for(i=0;i<n;i++)
{
tat[i]=bt[i]+wt[i]; total+=tat[i];
 
cout<<"	"<<i+1<<"	"<<bt[i]<<"	"<<wt[i]<<endl;
}
//avg_tat=(float)total/n;
// cout<<"Averagewaitingtime="<<avg_wt<<endl;
//cout<<"Averageturnaroundtime="<<avg_tat; return 0;
}
```
## OUTPUT :
![image](https://github.com/user-attachments/assets/ea782bed-92f3-4e46-a074-ba6a4f530dfd)

## RESULT:

Thus, the C++ program to implement FCFS algorithm(no of.process p1,p2 and p3 and its burst time are 10,5 & 8) find out waiting time of the process is created successfully.


