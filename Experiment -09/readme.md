# 🖥️ EXPERIMENT NO. 9
# CPU-BOUND AND I/O-BOUND PROCESSES
# 📌 AIM
To study and compare CPU-bound and I/O bound processes in an operating system by executing C programs ,monitoring their resource usage using top command and examining
their memory maps using pmap command.

# REQUIREMENTS:
1. linux or Ubuntu
2.  GCC Compiler

# 🎯 OBJECTIVES

To understand the concept of CPU-bound processes.
To understand the concept of I/O-bound processes.
To implement a CPU-bound program using repeated calculations.
To implement an I/O-bound program using file operations.
To compile and execute C programs using GCC.
To monitor process activity using the top command.
To examine process memory information using the pmap command.
To compare CPU-intensive and input/output-intensive activities.

# 🛠️ SOFTWARE REQUIREMENTS
| Component |	Description |
|:----------|:------------|
| Operating System |	Ubuntu Linux |
| Virtualization Software |	Oracle VirtualBox |
| Programming Language |	C |
| Compiler |	GCC |
| Editor | GNU Nano |
| Terminal	| Linux Terminal |
| Monitoring Commands |	top, pmap, ps |

# 📖 THEORY
1. Process in Operating System:
A process is a program that is currently being executed by the operating system.
A process requires system resources such as:
CPU time.
Main memory.
Input/output devices.
Files and other system resources.
The operating system manages processes and allocates resources to them.

2. CPU-Bound Process:
A CPU-bound process is a process that spends most of its execution time performing calculations and using the CPU.
It requires more processing power than input/output operations.
Examples:
Mathematical calculations.
Image processing.
Video encoding.
Scientific simulations.
Complex numerical computations.


flowchart 1:
<img width="537" height="885" alt="image" src="https://github.com/user-attachments/assets/2017d891-0521-423b-a9eb-b59e4f4ad95f" />


# Characteristics:

Performs repeated calculations.

Requires significant CPU processing time.

Often has high CPU utilization while running.

Performance depends heavily on processor speed and available CPU cores.


3. I/O-Bound Process:
An I/O-bound process is a process that spends a significant amount of time performing input/output operations rather than calculations.
It may interact with files, disks, keyboards, networks, and other input/output devices.
Examples:
Reading data from files.
Writing data to files.
Database operations.
Network communication.
File transfer operations.

flowchart 2: 

<img width="402" height="837" alt="image" src="https://github.com/user-attachments/assets/906c1f9b-87a7-4736-af99-a6a03687d767" />


# Characteristics:

Performs frequent input/output operations.

May spend time waiting for I/O completion.

CPU utilization can be lower than that of a CPU-bound process.

Performance depends on the speed of the input/output device and system resources.

# Concepts Demonstrated
Process: A running instance of a program.

PID: A unique process ID assigned by the operating system.

fork(): Creates a child process. It returns 0 in the child and the child's PID in the parent. A negative value indicates failure.

getpid(): Returns the PID of the calling process.

getppid(): Returns the PID of the parent process.

wait(NULL): Makes the parent wait for a child to terminate and collects the child's termination status.

# Expected Output

The exact PID values will differ each time you run the program. The output order is controlled so that the parent reports the child's termination after the child has finished.

Parent Waiting for child to terminate...

Child Running with PID: <child_pid>

Child Exiting...

Parent Terminated Child PID: <child_pid>

The first two lines may appear in a different order because the operating system schedules the parent and child independently.

# Note
This program follows the complete classroom implementation in the supplied Experiment 9 PDF, with an additional check for fork() and wait() errors.

<img width="1057" height="762" alt="image" src="https://github.com/user-attachments/assets/f11059b1-86a9-46ea-a685-1a19137b8b08" />

<img width="1020" height="767" alt="image" src="https://github.com/user-attachments/assets/c76b7027-300c-43c9-87ba-8d3380ad2130" />

<img width="1045" height="697" alt="image" src="https://github.com/user-attachments/assets/8f56f5ed-ea2e-4d38-9acf-071035226079" />


<img width="1031" height="712" alt="image" src="https://github.com/user-attachments/assets/ba1b3208-2095-4e24-a20d-05afe1a22a72" />


<img width="1057" height="666" alt="image" src="https://github.com/user-attachments/assets/18abae9f-cae5-4d01-8f7b-91795c897590" />




