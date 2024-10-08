# Digesting Documentation
This the 4th module and contains 7 challenges as follows.

## Learning from documentation
Requires the user to understand the given documentaion and use it to get the flag.

Given that in order to get the flag we have to use `/challenge/challenge` with the `--giveflag` argument.

Following the given instructions we get the flag.

The flag is `pwn.college{8wUYyVwpPd2GcOc5TzbCSzwrr6T.dRjM5QDLzkDN0czW}`.

## Learning Complex Usage
Requires the user to understand the given documentaion and use it to get the flag.

Given that `/challenge/challenge` prints arbituary files to the terminal when `--printfile` argument is used, the argument of `--printfile` is the path to the path to be read.

Use `ls` command to list the existing files which contains `not-the-flag`.

On using `/challenge/challenge --printfile ~/not-the-flag` we get the flag.

The flag is `pwn.college{YiQMDA3P68ll3uHmMt7cvZwa79r.dVjM5QDLzkDN0czW}`.

## Reading Manuals
Requires the user to learn about `challenge` command using the `man` command and use it appropriately to find the flag.

Using `/challenge/challenge --yjbeop 696` as instructed by the manual we get the flag.

The flag is `pwn.college{MAMBAyJj69be6YIoV6pigyQTKd8.dRTM4QDLzkDN0czW}`.

## Searching Manuals
Requires the user to navigate through the manual and find the correct argument to print the flag.

As given `n` is used to go back, `q` is used to exit out of the page, arrow keys are used to navigate and `/` is used to search for certain keywords.

Using `man challenge` and then `/flag`, we find that the `--vaxhl` gives us the flag.

The flag is `pwn.college{McAH3nLLdMTy61nrTP_2uKw9lrE.dVTM4QDLzkDN0czW}`.

## Searching For Manuals
Requrires the user to use `man man` and read about it and then use the appropriate commands to find the flag.

On going through it we get `man -k printf` which gives short descriptions for whatever printf maybe.

On using `man -k flag`, we find that `bvgevnfdmb` gives the flag.

On using `man bvgevnfdmb` we get to know that using `--bvgevn 409` argument gives us the flag.

The flag is `pwn.college{AbJMUUvgB4evK0XnfdWmR9b4ZIJ.dZTM4QDLzkDN0czW}`.

## Helpful Programs
Requires the user to read a program's documentation by using the `--help` argument.

Using `/challenge/challenge --help` we discover that on using the `-p` argument we get the secret number, and on using the `-g GIVE_THE_FLAG` gives the flag for the correct value of `GIVE_THE_FLAG`.

Hence on using `/challenge/challenge -g 436` we get the flag.

The flag is `pwn.college{EJhy43_uP_l6B_T7A1C7JRhAZAz.ddjM4QDLzkDN0czW}`.

## Help For Builtins
Requires the user to use `help` to look up help for builtins.

Which tells us to use `--secret gfG3pM90` to get the flag.

The flag is `pwn.college{gfG3pM90nE6DSoGks-8LDc_MJxk.dRTM5QDLzkDN0czW}`.
