# CPU-Scheduler
I have designed a simulator to simulate various CPU scheduling algorithms. The simulator is implemented in C++. The following scheduling algorithms were implemented:
1) First-Come-First-Serve(FCFS)
2) Shortest-Remaining-Time-First(SRTF), with preemption
3) Round-Robin(RR)

Explanation of the code:

    1) Classes such as Process(which contains all the necessary information about the process), ProcessCreator(which assigned random burst and arrival times to the processes),  Scheduler(ReadyQueue is implemented as an array inside this class) and Simulator(which carried out the simulation) were created.
    
    2) Functions such as sort_array(which sorted array of processes according to their arrival time), sort_array_BT(which sorted array of processes according to their burst time), etc, were created. 
    
    3) After creating the array of processes using "process_creator" class, all the processes were sorted according to their arrival times using the function "sort_array". This  step was common in all scheduling algos. 
    
    4) In SRTF algo, processes present inside the ready queue were sorted according to their burst times using the function "sort_array_BT". 
    
    5) Timeslice in Round Robin algo is taken as an input from the user, so it can be varied. (It is preferred to use timeslice as <=10 since the randomly assigned arrival time  and burst time are of certain range, 31 seconds in case of arrival time and 71 seconds in case of burst time, which can be changed inside the fuction "process_creator"). 

I did most of the testing of my code keeping the total number of processes to be 10/12 and changing the arrival and burst times.

Readyqueue is taken to be of fixed size (5 in my code). 

A file named as processes.txt is created using file handling which contains a table with all the information about the processes after simulation (completion time, turnaround time, etc).
