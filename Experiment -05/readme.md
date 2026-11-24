# Experiment 05: Shell Scripts Using Command-Line Arguments and Filename Manipulation
# Aim
To write and execute shell scripts that use command-line arguments to identify files and directories and perform filename manipulation.

# Requirements
Ubuntu Linux or another Linux distribution
Bash shell
A terminal or command-line interface
# Programs included
identify_path.sh — accepts a path as an argument and identifies whether it is a regular file, directory, or another type of path.
file_manipulator.sh — accepts an operation and filenames as arguments to rename, copy, or change a file's extension.
# flowchart 1:
<img width="333" height="788" alt="image" src="https://github.com/user-attachments/assets/d46900e1-fc05-4180-9e62-e9697b68d02b" />

# flowchart 2:
<img width="451" height="662" alt="image" src="https://github.com/user-attachments/assets/c7a615a6-9095-4b05-9994-3e306a3140eb" />

▶️ 7. Execution Procedure in Ubuntu Linux
## How to run
Open a terminal in this folder and make the scripts executable:
'''bash
chmod +x identify_path.sh
file_manipulator.sh
'''

Run the path-identification script:

./identify_path.sh notes.txt
./identify_path.sh Documents
'''

Run the filename-manipulation script:
'''bash
./file_manipulator.sh rename old.txt new.txt
./file_manipulator.sh copy notes.txt notes_backup.txt
./file_manipulator.sh ext report.txt md
'''
The 'ext' operation changes 'report.txt' to 'report.md'. Supply the new extension without a leading dot.

# Safety notes
Run these examples in a practice directory, not on important files.
The script checks that source files exist and asks before overwriting a destination.
Changing an extension changes the filename only; it does not convert the file's contents.
# Result
After running the scripts successfully, record the observed output and add your own terminal screenshots to the screenshots/ folder.
<img width="1197" height="857" alt="image" src="https://github.com/user-attachments/assets/2e20608e-6d44-4b98-beef-8a449bb1713e" />
<img width="1192" height="878" alt="image" src="https://github.com/user-attachments/assets/0974f663-8249-4a0e-aa3d-e63bfef406b2" />
<img width="930" height="956" alt="image" src="https://github.com/user-attachments/assets/b1cfe536-fe32-4f9d-88e3-0b2f808dcaf8" />

