>>whatis "command"

//Outputs description about the "command"

>>man "command"

//Shows mannual infomation about "command"

>>apropos -a "key phrases"

//Searches through mannual information for "key phrases"

>>pwd

//Current path

>>ls

//List files
//"-a" list hidden files.
//"-l" list permissions of files.

>>clear

//Clear the terminal

>>find "path"+"possible_dir_name"

//Searches "possible_dir_name" in "path"

>>find "path"+"possible_dir_name" -name "possible_file_name" 

//Searches "possible_file_name".(This file name MUST be inputed inside "")
//"*" on either OR both sides of the possible_file_name indicates unknown characters
//Ex: find "path"+"possible_dir_name" -name "*team*"
//This Ex searches for files name with "team" in the middle.
//find "path"+"dir_name" -mtime "number_of_days"
//Searches for all files in directory that is modified within the "number_of_day"
//"-tmin" searches for modifications done within how many minutes.

>>cp "file" "copyFileName" 

//Creates a copy of "file" with "copyFileName"

>>mv "file" "newDirectoryPath"

//Move "file" to a new location

//If "newDirectoryPath" is one dir before the current dir, uses ../"path"

//OR mv "file" "newFileName" - renames "file"

>>cd "file"

//Connect to file

>>cd ../

//Connect one directory before current directory

>>rm "file"

//Delete "file"

>>rm -r "file"

//Remove "file" with force

>>touch "path"/"file"

//Create and navigate "file" in "path"

>>mkdir

//Create directory

>>rmdir "name"

//Remove directory by name

>>echo "message" > "file"

//Print/write "message" into "file"

//">" does overwrite/append

>>echo "hell world" >> "file"

//">>" does append the content

>>cat "file" > "file2"

//Read/write "file" content into "file2"

>>echo "content ${another command}" 

//${} allows a command inside another command.

>>expr "calculation"

//Expression allows calculation

//Notice that all elements should separated by spaces.

//Example: expr 1 + 1 NOT expr 1+1

>>sudo apt install "software name"

//Install a software

>>sudo apt remove "software name"

//Uninstall a software

>>apt list --installed

//List the installed softwares

>>head

//Displays just the beginning of a file, by default 10 lines.

//Change the lines of display: -n "number of lines"

//Exmaple: head -n 10 "file anme"

>>tail

//Displays the ending of a file, by default 10 line.

>>less 

//Returns the content of a file one page at a time.

>>grep "phraseToSearch" "fileToSearch"

//Searches input phrases in input files

//If "phraseToSearch" contain spaces, use "", else without "" is fine.

>> |

//Piping "|" passes last command outputs as inputs for the next command

//Examples: ls /home/analyst/reports | grep OS

>>nano "fileName"

//Edits file content with tool nano

//Ctrl + O - Save; Ctrl + X - Exit

///////////////////////////
//PERMISSION DISTRIBUTION//
///////////////////////////
>>chmod "user/group/other""-/+""r/w/x" "file_name"

//"chmod" distributes permissions.
//"user/group/other" are simplified as "u/g/o"
//"r/w/x" written as "read/write/exexcute"
//"-/+" plus/adds permissons, minus/removes permissions.
//"," separate permission for different u/g/o
//Ex: chmod u-w,g-w "file_name" removes wrtie permission for both user and group.

>>chmod "###" "file_name"

//"###" 3 unique numbers can represent the permissions
//4 = read, 2 = write, and 1 = execute
//EX: chmod 440 "file_name" means permission to read for user and group only.

>>sudo useradd "user_name"

//"-g" sets user's default group;
//Adds new user to the system

>>sudo userdel "user_name"

//Deletes a existed user from the system
//"-r" deletes all files in user's home directory
//Ex: sudo userdel -r "user_name"

>>usermod

//Modifies existing users with options "-g" and "-G".
//Modifies the existing to existing group with "-a".
//"-d" changes the home directory of the user.
//Ex: sudo usermod -d "path"
//"-l" changes the user's login name.
//"-L" locks the account

>>chown

//Change the ownership of the files OR directory
//Ex: sudo chown "user_name" "file_name"
//Changes the ownership of the "file_name" to "user_name"
//Ex: sudo chown :"group_name" "file_name"
//Changes the ownership of the "file_name" to "group_name".
//Note!!! ":" must be added before "group_name" to indicates it's a group.
//"-G -a" adds the user to additional groups

>>cat /etc/passwd

//Outputs the existing users in the system
//"/etc/group" output the existing groups

>>id -nG "user_name"

//Shows supplementary group

>>groupdel "group_name"

//Deletes group that is named "group_name".
//Identical group was created as a new user was created.

//////////////////////
//SQL DATABASE QUERY//
//////////////////////
>>SELECT "column_name" FROM "table_name";

//Outputs "column_name" data from "table_name".
//Each sql command ends with ";".
//Use "," comma to separate tow or more column_name.

>>SELECT "column_name" FROM "table_name" ORDER BY "column_name";

//"ORDER BY" sets which column to references.
//Ex: SELECT "column_name" FROM "table_name" ORDER BY CustomerId;
//Outputs "column_name" data from the smallest to greatest id number.
//The default of "ORDER BY" is smallest to greatest for numbers,
//The first letter in alphabeta to the last letter.
//Add "DESC" to the end of "column_name" to specify the opposite/descending order.

>>sudo mysql "database_name"

//Conectes the database named "database_name".

>>SELECT "column_name" FROM "table_name" WHERE "column_name" = "search_phrase";

//Outputs "column_name" data from "table_name" that matches "search_phrase"
//Ex: >>SELECT job_position FROM "table_name" WHERE job_position = "IT_Staff";
//Outputs data about IT_Staff from "table_name".

>>SELECT "column_name" FROM "table_name" WHERE "column_name" LIKE "possible_phrase";

//Searches for "possible_phrase" at "column_name" from "table_name".
//"%" percentage sign substitutes for any number of other characters.
//Ex: ...LIKE "possible_phrase%" searches data that starts with "possible_phrase".
//Ex: ...LIKE "%possible_phrase" searches data that ends with "possible_phrase".
//"_" underscore symbol only substitutes for one other character.
//Ex: ...LIKE "possible_phrase_" searches data that starts with "possible_phrase" follow by ONLY one character.
//Ex: ...LIKE "_possible_phrase_" searches data that starts with ONLY one character, "possible_phrase" in the middle, follows by ONLY one character.

