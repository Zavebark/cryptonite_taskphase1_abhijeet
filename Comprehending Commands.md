# Comprehending Commands
Third module to be attempted and contains 12 challenges

# cat: not the pet, but the command!
Requires the user to use the `cat` command to read a file.

It is given that the flag is copied to the `flag` file in the home directory.

Hence typing `cat flag` we get the key.

The key is `pwn.college{U8tYlRUcaJIQXHn3Y9mq6LesVqH.dFzN1QDLzkDN0czW}`.

# catting absolute paths
Requires the user to use the `cat` command to read a file.

It is given that the flag is stored in the `flag` file in the home directory.

Hence typing `cat /flag` we get the key.

The key is `pwn.college{0KOJrFtfD7aJEBXiZeomnigxBj7.dlTM5QDLzkDN0czW}`.

# more catting practice
Requires the user to use the `cat` command to read a file.

It is given that the flag is stored in the `flag` file in the some directory.

The directory in which it is stored is `/lib/gprolog/bin`.

Hence typing `cat /lib/gprolog/bin/flag` we get the key.

The key is `pwn.college{ch8P9j-JHC6Zn07l7SFtEGQc2xY.dBjM5QDLzkDN0czW}`.

# grepping for a needle in a haystack
Requires the user to use the `grep` command to find the flag in a very large text file.

It is given that the flag is stored in `/challenge/data.txt`.

Hence typing `grep pwn.college  /challenge/data.txt` gives us the key.

The key is `pwn.college{0kCFcuSvh4wfhtsbepvHz5cup3W.ddTM4QDLzkDN0czW}`.

# listing files
Requires the user to use the `ls` command to find the random name of `/challenge/run` which is stored in `/challenge`.

Use the `cd` command to change directory to change to `/challenge` and then use `ls` to list the files present.

We get the random name to be `13598-renamed-run-22379`.

Therefore using `/challenge/13598-renamed-run-22379` we find the flag.

The flag is `pwn.college{I9kLyKRD-CDukyasNLlTXJ3RjTz.dhjM4QDLzkDN0czW}`.

# touching files
Requires the user to create new files using the `touch` command.

Use `touch` to create `/tmp/pwn` & `/tmp/college` then use `/challenge/run` to get the flag.

The flag is given by `pwn.college{YZr216_lNtLSsxF4_Ylbjxx3Fwv.dBzM4QDLzkDN0czW}`.

 # removing files
 Requires the user to use the `rm` command to remove files.

 Remove `delete_me` using the `rm` command and the run `/challenge/check` which gives us the flag.

 The flag is given by `pwn.college{gj74i9mOvim2vMadPWxLYwfl92U.dZTOwUDLzkDN0czW}`.

 # hidden files
 By default linux does not display the files starting with `.` when `ls` is used, hence `ls -a` is used to display all such files.

 change directory using `cd` command to `/` directory to find the file which contains the flag.

 then use the `cat` command to read the file which gives us the flag.

 the flag is given by `pwn.college{450pzMl528uwYL9n-SS8xqBA207.dBTN4QDLzkDN0czW}`.

 # An Epic Filesystem Quest
 Requires the user to use `ls`,`cd`&`cat`commands to find the flag which is hidden somewhere in `/` directory.

 first use `cd` command to change to `/` directory and then use `ls` command to view the files present.

 
