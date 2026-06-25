## Intro

**This note contains things to know when solving the OverTheWire Bandit series of challenges.**


_OverTheWire Link: [Bandit-Challenges](https://overthewire.org/wargames/bandit/)_

**Topics covered**
- Linux Commands (Mostly)
- Bash Script Writings
- Git Commands

## GET START
- Windows -> Powershell
- Linux -> Terminal 
- Mac -> Terminal


## References

- [bandit0](#bandit0)
- [bandit1](#bandit1)
- [bandit2](#bandit2)
- [bandit3](#bandit3)

### Bandit0
- [Go Back to Reference](#references)
```
ssh user_name@server_IP -p 2220
```
- `ssh` starts a secure remote shell connection.
- `-p` specifies the port number.
- `user_name@server_IP` specifies username and remote server. 
#### Examples: `ssh bandit0@bandit.labs.overthewire.org -p 2220`.


```
ls 
```
- `ls` list the files and folders in the current directory.
#### Examples: `ls`.


```
cat 'file_name'
```
- `cat` displays the content of the specified 'file_name'.
#### Examples: `cat readme`.


##
<!-- 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR -->


### Bandit1
- [Go Back to Reference](#references)

```
ssh user_name@server_IP -p 2220
```
- `ssh` starts a secure remote shell connection.
- `-p` specifies the port number.
- `user_name@server_IP` specifies username and remote server. 
#### Examples: `ssh bandit1@bandit.labs.overthewire.org -p 2220`.


```
ls 
```
- `ls` list the files and folders in the current directory.
#### Examples: `ls`.


```
cat ./'file_name'
```
- `./` option tells the `cat` command to open file included `-` in its name instead of interpreting `-` as a standard input.
#### Examples: `cat ./-`.


##
<!-- PK8fYLZg2hnHSz83plBL1iEPKdD3QToB -->


### Bandit2
- [Go Back to Reference](#references)

```
ssh user_name@server_IP -p 2220
```
- `ssh` starts a secure remote shell connection.
- `-p` specifies the port number.
- `user_name@server_IP` specifies username and remote server. 
#### Examples: `ssh bandit2@bandit.labs.overthewire.org -p 2220`.


```
ls 
```
- `ls` list the files and folders in the current directory.
#### Examples: `ls`.


```
cat ./'file\ name\ with\ spaces'
```
- `./` display files with dashes in their names.
- `\` specifies spaces in the file_name.
#### Examples `cat ./--spaces\ in\ this\ filename--`.


##
<!-- 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME -->


### Bandit3
- [Go Back to Reference](#references)

```
ssh user_name@server_IP -p 2220
```
- `ssh` starts a secure remote shell connection.
- `-p` specifies the port number.
- `user_name@server_IP` specifies username and remote server. 
#### Examples: `ssh bandit3@bandit.labs.overthewire.org -p 2220`.


```
ls 
```
- `ls` list the files and folders in the current directory.
#### Examples: `ls`.


```
cd 'directory_name'
```
- `cd` changes the current working directory to the specified directory. 
#### Examples `cd inhere`.


```
cat .`file_name`
```
- `.` is actually a part of the filename and filename with a dot in the front is hidden from the bash.
#### Examples: `cat ...Hiding-From-You`.


##
<!-- xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq -->


### Bandit4
- [Go Back to Reference](#references)
