# CommandChallenge
My learn Command Challenge

19. Count the number of files in the current working directory. Print the number of files as a single integer.
find -L . -type f | wc -l

20. Print the contents of access.log sorted.
sort access.log

21. Print the number of lines in access.log that contain the string "GET".
grep -wc "GET" access.log

22. The file split-me.txt contains a list of numbers separated by a ; character.
Split the numbers on the ; character, one number per line.
sed '/s/\;/\n/g' split-me.txt

23. Print the numbers 1 to 100 separated by spaces.
24. echo {1..100}

24. This challenge has text files (with a .txt extension) that contain the phrase "challenges are difficult". Delete this phrase from all text files recursively.
Note that some files are in subdirectories so you will need to search for them.
sed -i "challenges are difficult" **/*txt




