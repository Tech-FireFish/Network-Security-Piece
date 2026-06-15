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

/////////////////////////
//FILTER OPERATOR USAGE//
/////////////////////////

>>SELECT "column_name" FROM "table_name" WHERE "column_name" "operator_sign" "compare_value";

//This searches for vaule of "column_name" that is "operator_sign" in comparsion to "compare_value"
//Notice: "<>" indicates not equal to sign.

>>SELECT "column_name" FROM "table_name" WHERE "column_name" BETWEEN "start_value" AND "end_value";

//Searches for range of values that are between the "start_value" and "end_value".

>>SELECT "column_name" FROM "table_name" WHERE "column_name" = "1specific_value" OR "2specific_value";

//Searches and returns column data where "column_name" has either "1specific_value" or "2specific_value";
//WHERE NOT "column_name" = "specific_value"; returns data column that are not "specific_value".
//Ex: >>SELECT "column_name" FROM "table_name" WHERE "job_position" NOT = 'finance'
//This searches and returns job_position columns that are not finance.

//////////////////
//SQL JOIN USAGE//
//////////////////

>>SELECT "column_name" 
>FROM "table1_name" INNER JOIN "table2_name" 
>ON 'table1_name'+".'column_name'" = 'table2_name'+."'column_name'";

//You MIGHT have all those lines in a single line when entering.
//You must specify the two tables to join by including the first or left table after FROM and the second or right table after INNER JOIN.

>>SELECT "column_name" 
>FROM "table1_name" LEFT JOIN "table2_name" 
>ON 'table1_name'+".'column_name'" = 'table2_name'+."'column_name'";

//LEFT JOIN returns all the records of the first table, but only returns rows of the second table that match on a specified column. 
//You MIGHT think "=" as "and".

>>SELECT "column_name" 
>FROM "table1_name" Right JOIN "table2_name" 
>ON 'table1_name'+".'column_name'" = 'table2_name'+."'column_name'";

//RIGHT JOIN returns all of the records of the second table, but only returns rows from the first table that match on a specified column. 
//if you're checking for is a column value is null, use where 'column_name' is null;

>>SELECT "column_name" 
>FROM "table1_name" Right JOIN "table2_name" 
>ON 'table1_name'+".'column_name'" = 'table2_name'+."'column_name'";

//FULL OUTER JOIN query include all records from both tables. Similar to INNER JOIN, the order of tables does not change the results of the query. 

////////
//MORE//
////////
>>SELECT AVG("numerical_data")

//Returns a single number that represents the average of the numerical data in a column;

>>SELECT COUNT("numerical_data")

//Returns a single number that represents the number of records returned from a query;

>>SELECT SUM("numerical_data")
Returns a single number that represents the sum of the numerical data in a column;

