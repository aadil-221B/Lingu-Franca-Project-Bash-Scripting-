🌍 Lingua Franca Bash Scripting Project
Welcome to the Lingua Franca project! This guide walks you through various tasks using Bash commands. You’ll navigate directories, manage files, and configure your environment as you work through the tasks.



🚀 Task Group 1: Navigating the File System

Task 1️⃣: Navigate to Project Directory
Use cd to navigate to the lingua-franca/ directory. The relative path depends on your current location in the file system.

Task 2️⃣: Print Current Working Directory

pwd

Task 3️⃣: List Directory Contents

ls

Task 4️⃣: Create a New Directory

mkdir world

Task 5️⃣: Create a File and List Contents
Create esperanto.txt inside world/ and list the contents:


touch world/esperanto.txt
ls world

🖥️ Task Group 2: Viewing and Changing the File System

Task 6️⃣: List Hidden Files in Long Format, Sorted by Time

ls -alt

Here, the world/ directory will be listed first.

Task 7️⃣: Move chinese.txt to asia/

mv europe/chinese.txt asia/

Task 8️⃣: Copy spanish.txt to Multiple Directories and Remove It

cp spanish.txt europe/
cp spanish.txt northamerica/
cp spanish.txt southamerica/
rm spanish.txt

Task 9️⃣: List the Contents of todo/

ls todo/*

🔄 Task Group 3: Redirecting Input and Output

Task 🔟: Copy Files from todo/ to Their Correct Locations

cp todo/africa/* africa/
cp todo/asia/* asia/
cp todo/europe/* europe/

Task 1️⃣1️⃣: Remove Contents of todo/

rm -r todo/*

Task 1️⃣2️⃣: List All Files in asia/ and Save to File

ls asia/* > todo/asian_language_files.txt

Task 1️⃣3️⃣: Echo a Welcome Message into a File

echo "Welkom by die Lingua Franca vertaaldienste." > africa/afrikaans.txt

Task 1️⃣4️⃣: Find and List Empty Files Across Directories

wc -l */*.txt | grep ' 0 ' > todo/empty_files.txt

OR

find . -type f -name "*.txt" -print0 | xargs -0 wc -w | awk '$1 == 0 {print $2}'

Task 1️⃣5️⃣: Display the Content of empty_files.txt

cat todo/empty_files.txt

Task 1️⃣6️⃣: Correct Typo in All .txt Files

Replace Lingua-Franca with Lingua Franca:


sed -i 's/Lingua-Franca/Lingua Franca/g' */*.txt
grep -Rl 'Lingua-Franca' */*.txt | wc -l
⚙️ Task Group 4: Configuring the Environment

Task 1️⃣7️⃣: Open and Edit Bash Profile

nano ~/.bash_profile

Task 1️⃣8️⃣: Add a Greeting in the Bash Profile

echo "Hello, Hola, Ni Hao, Bonjour, Kon'nichiwa! Welcome to Lingua Franca!"

Task 1️⃣9️⃣: Source the Bash Profile to Apply Changes

source ~/.bash_profile

Task 2️⃣0️⃣: Create Aliases in the Bash Profile

alias md="mkdir"
alias d="date"
alias hy="history"

Task 2️⃣1️⃣: Test the Aliases

md translations
ls translations
d
hy

🔧 Task Group 5: Customizing the Prompt

Task 2️⃣3️⃣: Set a Custom Prompt

export PS1="Lingua Franca > "

Task 2️⃣4️⃣: Source the Bash Profile and Test the New Prompt

source ~/.bash_profile

✅ Final Task: List All Environment Variables
To view all the environment variables, use:

env
