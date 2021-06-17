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
echo {1..100}

24. This challenge has text files (with a .txt extension) that contain the phrase "challenges are difficult". Delete this phrase from all text files recursively.
Note that some files are in subdirectories so you will need to search for them.

sed -i "challenges are difficult" **/*txt

25. The file sum-me.txt has a list of numbers, one per line. Print the sum of these numbers.
awk '{a+=$0}END{print a}' *

26. Print all files in the current directory recursively without the leading directory path.
ls -R | grep [a-z]

27. Rename all files removing the extension from them in the current directory recursively.
mv * .*
rename 's/\.//' **
find . -type f | rename 's/\.//' **

28. The files in this challenge contain spaces. List all of the files (filenames only) in the current directory but replace all spaces with a '.' character.
ls | sed 's/ /./g'
find * -type f | sed 's/\ /\./g'

29. In this challenge there are some directories containing files with different extensions. Print all directories, one per line without duplicates that contain one or more files with a ".tf" extension.
find -name *.tf -printf '%h\n' | sort -u

30. There are a mix of files in this directory that start with letters and numbers. Print the filenames (just the filenames) of all files that start with a number recursively in the current directory.





