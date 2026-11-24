# Experiment 7: String Operations Using Shell Script and C
This experiment demonstrates how to extract a substring, find string length, and observe program execution time using Bash and C.

# Programs
1. Bash: Extract Substring and Find Length
The shell script:
Accepts a string from the user.
Accepts a starting position and substring length.
Extracts the requested portion using cut -c.
Displays the string length using Bash's ${#str}.

2. C: Extract Substring and Find Length
The C program:
Reads a string.
Accepts a starting position (0-based) and substring length.
Prints the selected characters.
Displays the string length using strlen().
3. Compare Running Time
The experiment uses the time command to observe runtime:
time bash substring.sh

gcc substring.c -o substring
time ./substring
Requirements
Linux, WSL, or another Bash-compatible environment
GCC compiler for the C program
Running the Bash Program
bash substring.sh
Or:

chmod +x substring.sh
./substring.sh
Compiling and Running the C Program
gcc substring.c -o substring
./substring
Important Notes
Bash's cut -c positions begin at 1. The C program uses a 0-based starting position.
The C program uses scanf("%99s", str), so it reads a single word and does not accept spaces within the input string.
Enter non-negative start positions and lengths that fit the input string.
Run the timing commands more than once for a more useful observation. Results can vary with system load and timing overhead.
Learning Outcomes
Extract substrings using Bash and C.
Determine string length.
Use cut, strlen(), and Bash string-length expansion.
Use time to observe command execution duration.


flowchart 1: string operations using bash

<img width="227" height="916" alt="image" src="https://github.com/user-attachments/assets/56d0f003-2e3b-468a-8c45-c87994bef2ab" />


flowchart 2: string operations using C

<img width="406" height="805" alt="image" src="https://github.com/user-attachments/assets/537b95a5-1d52-42c0-ad89-e182ff5472e2" />


Result
Substring extraction, string-length calculation, and basic runtime observation using Bash and C were studied.
<img width="626" height="803" alt="image" src="https://github.com/user-attachments/assets/fc59c3d0-4d93-4407-9a9b-4dbe4227e6cc" />
<img width="835" height="345" alt="image" src="https://github.com/user-attachments/assets/f388fcc5-f5f8-4af5-8fc3-3f78c3a8eb57" />

