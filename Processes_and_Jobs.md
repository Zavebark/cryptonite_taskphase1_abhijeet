# Processes and Jobs
The 8th module and contains 9 challenges as follows

## Listing Processes
Requires the user to use the `ps` command to list the list of processes running currently in the shell and stands for "process snapshot".

We need to use either `-ef` or `aux` arguments to make ps command usefull.

Use `ps -ef` which gives a list of processes running currently which gives us a list of programs currently running out of which when we execute `/challenge/642-run-25708` we get the flag.

The flag is `pwn.college{AXoVSWmGKPtC50oBk7rc83nM6Fg.dhzM4QDLzkDN0czW}`.

## Killing Processes
Requires the user to use the `kill` command to stop a program that is running and then execute another program to get the flag.

Use `ps aux` and then find the PID of `/challenge/dont_run` which happens to be `73`.

Use `kill 73` and then use `/challenge/run` which gives us the flag.

The flag is `pwn.college{ISl-BlfNNmljaWYCuciELmP3w1w.dJDN4QDLzkDN0czW}`.

## Interrupting Processes
Requires the user to interrupt the process of a program by using the hotkey `ctrl+c` which stops the process and gives us the flag.

Use `/challenge/run` which will refuse to give the flag until you interrupt is by using `ctrl+c` which gives us the flag.

The flag is `pwn.college{QM8DMtVzTdRyuFQ73nLSa977WPL.dNDN4QDLzkDN0czW}`.

## Suspending Processes
Requires the user to suspend a program to the background using the hotkey `ctrl+z`.

Use `/challenge/run` and then use `ctrl+z` which suspends it to the background and then again use `/challenge/run` which gives us the flag.

The flag is `pwn.college{8QJFNRlsthT6oBMrSx4bApQ6oW-.dVDN4QDLzkDN0czW}`.

## Resuming Processes
Requires the user to suspend a program and then resume by using `fg` command to resume it to get the flag.

Use `/challenge/run` and then use `ctrl+z` to suspend it, and now use `fg` to get the flag.

The flag is `pwn.college{ARouLX7pc5FyODxCmUM0g0He8_j.dZDN4QDLzkDN0czW}`.

## Background Processes
Requires the user to move a program to the background by using the `bg` command.

Use `/challenge/run` and then use `ctrl+z` after this use `bg` and then again relaunch the program as `/challenge/run` which gives us the key.

The key is `pwn.college{olEv2g-YdbFeKXbdlUy3qF5JJAv.ddDN4QDLzkDN0czW}`.

## Foregrounding Processes
Requires the user to bring a background program to the foreground to make changes to it by using the `fg` command which brings a background program to the foreground.

Use `/challenge/run` and then suspend it by using `ctrl+z` and then use `bg` which pushes it to the background and then use `fg` to bring to the foreground which gives us the flag.

The flag is `pwn.college{cVIEmnV6aJr9eJzuEXniAbwp-uu.dhDN4QDLzkDN0czW}`.

## Starting Background Processes
Requires the user to background a process without suspending it by adding `&` at the end of the command.

Use `/challenge/run &` which bacmgrounds the `/challenge/run` program which gives us the flag.

The flag is `pwn.college{4OOwUOhnIgHTkz3AyhpKlyMCbJg.dlDN4QDLzkDN0czW}`.

## Process Exit Codes
Requries the user to acess the exit code of the most recently terminated program by using the special variable `?` which must be perpended with `&` in order to read it.

Requires the user to retrieve the exit code returned by `/challenge/get-code` and then to run the command `/challenge/submit-code` with the error code as an argument.

Use `/challenge/get-code` and then use `echo $?` which gives the error code to be `65`.

Now use `/challenge/submit-code 65` which gives us the code.

The code is `pwn.college{EwwWquj4_JUAvtUsU3i-q2oL7FS.dljN4UDLzkDN0czW}`.
