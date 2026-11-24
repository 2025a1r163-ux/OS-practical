# Experiment 08 — Memory Allocation and Usage in C
# Objective
Allocate memory dynamically, observe process memory usage, and release the allocation with free.

# Setup
Ubuntu with GCC, a terminal, and top or ps. Start with a small allocation such as 16 MB that comfortably fits available memory.

# Practical work
Read memory-exercises.txt, then run the examples below from this lab folder.

## Programs
| File |	Purpose |
|:-----|:---------|
| 'memory-allocation.c' |	Validate a size, allocate and touch memory, wait for Enter, and release it.

'''bash 
gcc -std=c11 -Wall -Wextra -Wpedantic memory-allocation.c -o memory-allocation
./memory-allocation 16
# While the program waits, open a second terminal:
ps -C memory-allocation -o pid,comm,vsz,rss
# Or inspect the process interactively:
top
'''
The program uses 1 MB = 1024 × 1024 bytes (technically a MiB). It writes every byte before waiting so the allocation becomes resident. ps reports VSZ and RSS in KiB on Ubuntu; total usage also includes the program and libraries. Press Enter once in the first terminal to free memory and exit.

flowchart 1: dynamic memory allocation

<img width="460" height="938" alt="image" src="https://github.com/user-attachments/assets/77086104-bbd0-4325-be29-27b26988cc51" />

flowchart 2:

<img width="277" height="915" alt="image" src="https://github.com/user-attachments/assets/004de406-0dad-4891-a6d6-f37a9fb185ef" />

# Observations and result
Record the commands or steps you completed, the output you observed, and any difficulties. Add your own screenshots to screenshots/; useful evidence includes compilation, successful allocation, memory usage while waiting, and memory release.

Complete the result after performing the practical work.
