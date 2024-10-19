# Perceiving Permissions
This is the 9th module and contains 8 challenges.

## Changing File Ownership
Some files can only be accesed by the admin, to access such files you must change the owner of the files by using the `chown` which is used to change ownership.

The `ls -l` is used to display the permissions and ownership of files.

Use `chown hacker /flag` which gives us the flag.

The flag is `pwn.college{QpADfUwDMqAJXBHBagh_7FxpymX.dFTM2QDLzkDN0czW}`.

## Groups and Files
Requires the user to become a part of the root group in order to access the file by using `chgrp`, whearas `id` command is used to display what all groups the user is in.

Use `chgrp hacker /flag` which gives us the flag.

The flag is `pwn.college{4XukxgwNDXnIHob9GtCD3ubyWYN.dFzNyUDLzkDN0czW}`.

## Fun with Group Names
Requires the user to find the name of the group he is in by using `id` and then change the group name to `flag`.

Use `id` which gives us the name of the group to be `grp13214`.

After that use `chgrp grp13214 /flag` and then use `cat /flag` which gives us the flag.

The flag is `pwn.college{oYkti6cAOOuMeEdg-mwXVStpwQr.dJzNyUDLzkDN0czW}`.

## Changing Permuissions
```
r: the user that owns the file (user hacker) can read it
w: the user that owns the file (user hacker) can write to it
-: the user that owns the file (user hacker) cannot execute it
r: users in the group that owns the file (group hacker) can read it
-: users in the group that owns the file (group hacker) cannot write to it
-: users in the group that owns the file (group hacker) cannot execute it
r: all other users can read it
-: all other users cannot write to it
-: all other users cannot execute it
```
Requires the user to change the permission of the `/flag` file using `chmod` command in order to make it readable.
```
r - user/group/other can read the file (or list the directory)
w - user/group/other can modify the files (or create/delete files in the directory)
x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
- - nothing 
```

The general form of `chmod` is:
```
chmod [OPTIONS] MODE FILE
```
where
```
chmod allows you to tweak permissions with the mode format of WHO+/-WHAT, where WHO is user/group/other and WHAT is read/write/execute.
u+r, as above, adds read access to the user's permissions
g+wx adds write and execute access to the group's permissions
o-w removes write access for other users
a-rwx removes all permissions for the user, group, and world
```
To solve the given problem use `chmod o+r /flag` which gives us the flag.

The flag is `pwn.college{sqUGZViSggkH3I_NnaPlEr2RDP_.dNzNyUDLzkDN0czW}`.

## Executable Files
Requires the user to use the `chmod` command in order to make the command executable.

Use `chmod u+x /challenge/run` and then use `/challenge/run` which gives us the flag.

The flag is `pwn.college{EaznZ8DqT7PC2ASHzplsXTXhrMA.dJTM2QDLzkDN0czW}`.

## Permission Tweaking Practice
Requires the user to use the `chmod` command in order multiple times in a row to find the flag.

On using `ls` we find a `instructions` file which we can read by using the `cat` command.

```
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
```
Then shift to the `/challenge` directory and use `ls -l` and then follow the instructions to change the permissions as asked for.

The first challenge is:
```
NEEDED, BUT UNMET permissions of "/challenge/pwn": rw----r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

CURRENT, INCORRECT permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
```
To solve this use `chmod g-r,o+r pwn` which gives us the next challenge.
```
Current permissions of "/challenge/pwn": rw----r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-------
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
```
To solve this use `chmod o-r pwn` which gives us the next challenge which is
```
Current permissions of "/challenge/pwn": rw-------
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw----r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
```
To solve this use `chmod o+r pwn` which gives us the next challenge which is
```
Current permissions of "/challenge/pwn": rw----r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rwx---r-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
```
To solve this use `chmod u+x,o+x pwn` which gives us the next challenge which is
```
Current permissions of "/challenge/pwn": rwx---r-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrwxr-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
```
To solve this use `chmod g+rwx pwn` which gives us the next challenge which is
```
Current permissions of "/challenge/pwn": rwxrwxr-x
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
```
To solve this use `chmod a+rwx pwn` which gives us the next challenge which is
```
Current permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": r--rwxrwx
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
```
To solve this use `chmod u-wx pwn` which gives us the next challenge which is
```
Current permissions of "/challenge/pwn": r--rwxrwx
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": r--rwxr--
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
```
To solve this use `chmod o-wx pwn` which gives us a final challenge which is to set the permissions for the `/flag` file and then using `cat` which gives us the flag.

The flag is `pwn.college{AgxgrHv1i_Ku6UPPlD8wa2ocuN_.dBTM2QDLzkDN0czW}`.

## Permission Setting Practice
Similar to the previous question but requires the user to use `=` which sets the value and overwrites the previous permissions.

1st- Use `chmod g+x,o+wx pwn` which gives us the next challenge.

2nd- Use `chmod u=rx,g=rw,o=x pwn` which gives us the next challenge.

3rd- Use `chmod g=w,o=rx pwn` which gives us the next challenge.

4th- Use `chmod u=r,g=r,o=wx pwn` which gives us the next challenge.

5th- Use `chmod u=rx,g=x,o=r pwn` which gives us the next challenge.

6th- Use `chmod u=rwx,g=rwx,o=- pwn` which gives us the next challenge.

7th- Use `chmod u=-,g=rwx,o=x pwn` which gives us the next challenge.

8th- Use `chmod u=r,g=-,o=w pwn` which gives us the next challenge.

This gives us the flag after changing the permissions for the `/flag` file.

The flag is `pwn.college{Q0Nn1hjX0WBaI3fQEO6IkJyidKU.dNTM5QDLzkDN0czW}`.

## The SUID Bit
Requires the user to set the SUID Bit to a certain configuration in order to get the flag.

Given that `/challenge/getroot` opens a root terminal but to run it the SUID Bit must be set as `chmod u+s /challenge/getroot`.

Which sets the root
```
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~#
```
Then using `cat /flag` gives us the flag.

The flag is `pwn.college{8PcD7faYxwCQTFUcOoi0AhPHnCV.dNTM2QDLzkDN0czW}`.
