# Practicing Piping
This is the sixth module and contains 11 challenges as follows.

## Redirecting output
Requires the user to use `>` to redirect the output to some other file.

Use `echo PWN > COLLEGE` which gives us the flag.

The flag is `pwn.college{kBdhcoqrFarYuwFEsO7Ek85SGg_.dRjN1QDLzkDN0czW}`.

## Redirecting  more output
Requires the user to redirect the output of `/challenge/run` to the file `myflag`.

Use `/challenge/run > myflag` and then use `cat myflag` which gives us the flag.

The flag is `pwn.college{M5luiWBQvMOCwoiRg-od4vuYT7H.dVjN1QDLzkDN0czW}`.

## Appending output
Requires the user to use `>` in append mode ie `>>` to add instead of overwritting the existing data.

Use `/challenge/run >> ~/the-flag` and then using `cat ~/the-flag` which gives us the flag.

The flag is `pwn.college{wuQeVGxM_hNTet6AGAbkOaE_COb.ddDM5QDLzkDN0czW}`.

## Redirecting Errors
Requires the user to use FD number which describes a communication channel in linux. 

We have been using FD's in the background due to implicit transformation.

`0-Standard Input` 

`1-Standard Output`

`2-Standard Error`

Requires the user to use `/challenge/run 1> myflag 2> instructions` .

And then using `cat myflag` gives us the flag.

The flag is `pwn.college{MlgDbDELRZlTmwhKSF5ZF2UZZF7.ddjN1QDLzkDN0czW}`.

## Redirecting Inputs
Requires the user to redirect the input to a program using the `<` command.

Using `echo COLLEGE > PWN` and then using `/challenge/run < PWN` gives us the flag.

The flag is `pwn.college{cLO3pIAcKMQtD7Td94p0Hm2cJ1u.dBzN1QDLzkDN0czW}`.

## Grepping Stored Results
Requires the user to redirect the output of a command to another file and then `grep` it to find the flag.

Use `/challenge/run > /tmp/data.txt`.

Then use `grep pwn.college /tmp/data.txt` whioh gives us the flag.

The flag is `pwn.college{cU3q8LUqPpMqIV--2usUHrwqsBC.dhTM4QDLzkDN0czW}`.

## Grepping Live Output
Requires the user to `grep` for the file using piping command `|`.

Using `|` we can eliminate the need to store valure of a command in a file and then grep that file, now we can directly grep without the need for an extra file.

Use `/challenge/run | grep pwn.college` which gives us the flag.

The flag is `pwn.college{oSZuTPbSrnLwpvC_fpS8oUB5oUB.dlTM4QDLzkDN0czW}`.

## Grepping errors
Requires the user to pipe through the errors file to find the flag.

Use `/challenge/run 2>&1 | grep pwn.college` which gives us the flag.

The flag is `pwn.college{kpfAy-4ORSuTVi6cvjeYWDbfe-B.dVDM5QDLzkDN0czW}`.

## Duplicating piped data with tee
Requires the user to pipe the output of `/challenge/pwn` and then duplicate it using `tee` command as follows.

Use `/challenge/pwn | tee random | /challenge/college` and then use `cat random`.

It gives us
```
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "c5sZNMMf"
```
Hence using `/challenge/pwn --secret c5sZNMMf | /challenge/college` we get the flag.

The flag is `pwn.college{c5sZNMMfGVVOHGH7D6L8GpThTkc.dFjM5QDLzkDN0czW}`.

## Writing to multiple programs
Requires the  user to redirect the input to multiple programs to get the flag.

Using `()` we can use the same input for multiple programs as follows.

Use `/challenge/hack | tee >(/challenge/the) | /challenge/planet` which gives us the flag.

The flag is `pwn.college{sbctQoHGJdBANnD7dcC8VFvtbT9.dBDO0UDLzkDN0czW}`.

## Split-piping stderr stdout
Requires the user to use all the knowledge acquired to redirect error and output to two different files which gives us the flag.

Use `2>` and `>(/challenge/the)` which gives us the flag.

Then use `/challenge/hack 2> >(/challenge/the) | /challenge/planet` which gives us the flag.

The flag is `pwn.college{AlvAt_rz-xz-l_LhIzpYmpXag5y.dFDNwYDLzkDN0czW}`.
The flag is ``.
