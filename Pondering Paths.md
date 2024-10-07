# Pondering Paths
Second module to attempted and it contains 9 challenges.

## The Root
Requires the user to invoke the `pwn` program using its absolute path.

On typing `/pwn` and clicking the `enterkey` we get the flag.

The flag is `pwn.college{kGMvUhE6xeINpbXmjilNVw3XuWg.dhzN5QDLzkDN0czW}`.

## Program and absolute paths
Requires the user to use absolute paths to find the flag.

On typing `/program/run` as instructed we get the flag.

The flag is `pwn.college{8gICTf-LKPSwNdC4V8rI-yTfaHI.dVDN1QDLzkDN0czW}`.

## Position Thy Self
Requires the user to change directory using the `cd` command to change the current directory to a specified directory.

The directory to change to is `/var`.

Using `cd` to change directory to `/var` as `cd /var`.

And then typing `/program/run` as instructed to find the flag.

The flag is `pwn.college{sRk2SNbXu7XCMWkRC-p6Bk69HKe.dZDN1QDLzkDN0czW}`.

## Position elsewhere
Requires the user to change directory using the `cd` command to change the current directory to a specified directory.

The directory to change to is `/usr/aarch64-linux-gnu/include/gnu`.

Using `cd` to change directory to `/usr/aarch64-linux-gnu/include/gnu` as `cd /usr/aarch64-linux-gnu/include/gnu`.

And then typing `/program/run` as instructed to find the flag.

The flag is `pwn.college{kLUZUyeAHYjkVi3nqotv0W_ReVB.ddDN1QDLzkDN0czW}`.

## Position yet elsewhere
Requires the user to change directory using the `cd` command to change the current directory to a specified directory.

The directory to change to is `/usr/aarch64-linux-gnu/include/gnu`.

Using `cd` to change directory to `/usr/aarch64-linux-gnu/include/gnu` as `cd /usr/aarch64-linux-gnu/include/gnu`.

And then typing `/program/run` as instructed to find the flag.

The flag is `pwn.college{wRjbtovuhmvY39fDc_r-EPPguTI.dhDN1QDLzkDN0czW}`.

## Implicit relative paths, from /
Requires the user to run `/challenge/run` from the `/` directory.

First change the `cwd` to '/' by using the `cd` command.

Then type `challenge/run` to get the flag.

The flag is `pwn.college{MtJsvFRt8_fAg9c0rG1P5CRlU4q.dlDN1QDLzkDN0czW}`.

## Explicit relative paths, from /
Requires the user to use `.` in the relative paths.

`./` specifies a relative path and is used as `./challenge`.

First change the `cwd` to `/` by using the `cd` command.

Then type `./challenge/run` to get the flag.

The flag is `pwn.college{chZ5Wfk6jWMJrZEJfwrNPSNZjrT.dBTN1QDLzkDN0czW}`.

## Implicit relative path
Requires the user to use `.` in the relative paths.

`./` specifies a relative path and is used as `./run`.

First change the `cwd` to `/challenge` by using the `cd` command.

Then type `./run` to get the flag.

The flag is `pwn.college{4djdHSjL2RIbyDlBfERDCtyi3b-.dFTN1QDLzkDN0czW}`.

## home sweet home
Requires the user to copy the flag to any file using `/challenge/run`.

The constraints are;

1.Argument must be an absolute path

2.Path must be within the home directory(ie must include `/home/hacker`)

3.BEFORE expansion the argument must be 3 characters long(ie they are asking us to use `~` instead of `/home/hacker`)

Therefore let the argument for the file to which the flag must be copied be `~/K`.

Now type `/challenge/run ~/K` and press `enterkey`, this gives us the key.

The key is `pwn.college{0OBtG8UBTasPQtIa5_aqeo09azG.dNzM4QDLzkDN0czW}`.
