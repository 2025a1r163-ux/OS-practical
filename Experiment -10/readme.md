# 🚀 EXPERIMENT 10 — PROCESS CREATION AND TERMINATION USING C

# 📌 ABOUT THE EXPERIMENT
This experiment demonstrates the creation and termination of processes in the Linux operating system using C programming.


It explains how a parent process creates a child process using the fork() system call, how the child performs its execution, and how the parent waits for the child to terminate using wait().


The program also demonstrates process identification using getpid(), execution delay using sleep(), and process termination using exit().

# ⚡ Key Concepts
1.Process Creation

2.Parent and Child Processes

3.Process Identification (PID)

4.Process Synchronization

5.Process Termination

6.Linux System Calls


# 🎯 01. AIM

To write and execute a C program that creates a child process using the fork() system call, waits for its termination using wait(), and displays the Process ID (PID)
of the terminated child process.

# 🎯 02. OBJECTIVES

The main objectives of this experiment are:

To understand the concept of process creation in Linux.

To create a child process using the fork() system call.

To understand the difference between parent and child processes.

To use the wait() system call to synchronize parent and child processes.

To display the Process ID (PID) of the child process.

To understand process termination using exit().

To understand how Linux manages multiple processes during program execution.


# 💻 03. SOFTWARE REQUIREMENTS

The following software and tools are required to perform this experiment.

| Component |	Specification |
|:----------|:--------------|
| Operating System	| Ubuntu Linux |
| Virtualization Software |	Oracle VirtualBox |
| Programming Language |	C |
| Compiler |	GCC |
|Text Editor |	GNU Nano |
|Terminal |	Linux Terminal |
| File Extension |	.c |

# 📚 04. THEORY

## What is a Process?

A process is a program that is currently being executed by the operating system.

Every process has a unique Process ID (PID), which helps the operating system identify and manage it.

A process requires system resources such as CPU time, memory and other resources during execution.

## What is Process Creation?
Process creation is the process of creating a new process during program execution.

In Linux, a process can create another process using the fork() system call.

The process that creates another process is called the Parent Process, while the newly created process is called the Child Process.

## Parent Process
A parent process is the original process that creates another process using fork().

## Child Process
A child process is a newly created process that executes independently from its parent process.

## Process ID (PID)
A Process ID is a unique numerical identifier assigned to each process by the operating system.

It is used to identify and manage processes.

## Process Synchronization
Process synchronization is the coordination of multiple processes to ensure that they execute in the required order.

In this experiment, the wait() system call makes the parent process wait until its child process terminates.

# SYSTEM CALLS USED
This experiment uses five important Linux functions.

|Function |	Purpose |
|:--------|:--------|
| fork() |	Creates a new child process |
| getpid() |	Returns the PID of the currently executing process. |
| sleep() |	Suspends execution for a specified number of seconds. |
| wait() |	Makes the parent wait for a child process to terminate. |
| exit() |	Terminates the calling process. |


## 1. fork()

The fork() system call creates a new child process.

Return values:

0 – Returned to the child process.

Positive value – Returns the child's PID to the parent.

-1 – Indicates process creation failure.

## 2. getpid()

The getpid() function returns the Process ID of the currently executing process.

It helps identify the child process.

## 3. sleep()
The sleep() function suspends the execution of the calling process for a specified number of seconds.

In this experiment:

sleep(2);
The child process pauses for two seconds.

## 4. wait()
The wait() system call makes the parent process wait until one of its child processes terminates.

It returns the PID of the terminated child process.

It also collects the child's termination status, preventing the terminated child from remaining as a zombie process.

## 5. exit()
The exit() function terminates the calling process.

exit(0);
Here, 0 indicates successful termination.


 OUTPUT AND EXPLANATION
Expected Terminal Output
Parent Waiting for child to terminate...
Child Running with PID: 4402
Child Exiting...
Parent Terminated Child PID: 4402
Note: The PID 4402 is an example. The actual PID may change every time the program is executed.

# Output Explanation

| Terminal | Output	Explanation |
|:---------|:-------------------|
| Parent Waiting for child to terminate... |	The parent displays this message before calling wait(). |
| Child Running with PID: | 4402	The child displays its unique PID using getpid(). |
| Child Exiting... |	The child displays this message before terminating. |
| Parent Terminated Child PID: | 4402	The parent displays the PID returned by wait(). |


# Important Output Observation

The wait() system call prevents the parent from continuing beyond the waiting statement until a child process terminates.

The parent then resumes execution and displays the terminated child's PID.

Important: Process scheduling is controlled by the operating system, so the relative order of parent and child output before synchronization is not guaranteed to be identical on every execution.





# Process execution Flowchart


<img width="457" height="986" alt="image" src="https://github.com/user-attachments/assets/37066d6a-9294-4437-b511-62d5e3587162" />


# Process Execution Explanation

The execution of the program takes place in the following order:

The program starts and calls fork().

The operating system creates a child process.

The child and parent execute their respective code blocks.

The child displays its PID and sleeps for two seconds.

The parent calls wait() and waits for the child.

The child displays its termination message and exits.

The parent resumes execution.

The parent displays the PID returned by wait().

The program ends


#  Parent and Child Process Comparison

| Parent Process |	Child Process |
|:---------------|:---------------|
| Creates the child using fork(). |	Created by the parent process. |
| Receives the child's PID from fork(). 	Receives 0 from fork(). |
| Calls wait(NULL). |	Executes sleep(2). |
| Waits for child termination. |	Terminates using exit(0). |
| Displays the terminated child's PID. |	Displays its own PID. 


#  IMPORTANT OBSERVATIONS
The fork() system call successfully creates a child process.

The parent and child processes have different PIDs.

Both processes execute independently after fork().

The child process takes approximately two seconds to complete its simulated work.

The parent process waits until the child terminates.

The PID returned by wait() matches the PID displayed by the child.

The parent resumes execution after the child terminates.

The wait() system call collects the child's termination status and prevents it from remaining as a zombie process.

⚠️ #  PRECAUTIONS
Include all the necessary header files.

Use the correct syntax for the fork() system call.

Check the return value of fork() for errors.

Compile the program before executing it.

Use wait() to synchronize the parent and child processes.

Make sure the source filename matches the filename used during compilation.

Check for errors during compilation and execution.

Use the correct Linux terminal commands.

# 🏆 15. RESULT

The C program for process creation and termination was successfully written, compiled and executed in Ubuntu Linux using Oracle VirtualBox.

The fork() system call successfully created a child process, while the wait() system call made the parent process wait for the child's termination.

The getpid() function successfully displayed the child process ID, and the parent process displayed the PID of the terminated child.

Hence, the experiment was successfully completed.

<img width="1141" height="853" alt="image" src="https://github.com/user-attachments/assets/8a1047dc-bb18-4c2d-9857-232fb66539bf" />


<img width="846" height="577" alt="image" src="https://github.com/user-attachments/assets/324ce787-3bb1-4512-957a-26e49411a2fd" />
