# Shell Variables
Is the 7th module and has 8 problems to solve.

## Printing Variables
Requires the user to read a variable which gives the flag.

The flag is given by `echo $FLAG`.

Where `$` specifies that it is a variable.
 
The flag is `pwn.college{cM06CFMyMWf2_dMED2p_P3Zs0xp.ddTN1QDLzkDN0czW}`.

## Setting Variables
Requires the user to use `=` and assign a value to a variable.

To get the flag use `PWN=COLLEGE` which in turn gives the flag.

The flag is `pwn.college{8Dm1xityn3Oie1RRw37jJroco4y.dlTN1QDLzkDN0czW}`.

## Multi-word Variables
Requires the user to understand the use of `""` in assigning multi word values to a variable.

To get the flag use `PWN="COLLEGE YEAH"`.

The flag is `pwn.college{ck2Re03QfaG1PzkUD10WOkPmRK-.dBjN1QDLzkDN0czW}`.

## Exporting Variables
Requires the user to make a variable available to a child shell by using the `export` command.

Use `COLLEGE=PWN` and then use `export PWN=COLLEGE` which exports `PWN` but not `COLLEGE` as required.

Then use `/challenge/run` which gives us the flag.

The flag is `pwn.college{k4sJjM0Tm5QqEnuDdVy4fFZY5es.dJjN1QDLzkDN0czW}`.

## Printing Exported Variables
Requires the user to use `env` command to read all the variables in the shell and search through them to find the flag variable.

Use `env` and then on going through the results we find the flag.

The flag is `pwn.college{YLE5B-0pRjgDNUAPzuRrQGoT4RD.dhTN1QDLzkDN0czW}`.

## Storing Command Output
Requires the user to store the output of a function in another variable and then read it to get the key.

Use `PWN=$(/challenge/run)` and then read the variable using `echo`.

Use `echo $PWN` which gives us the flag.

The flag is `pwn.college{g6EId5lKsDpzTFA0RYFEWpaOLkj.dVzN0UDLzkDN0czW}`.

## Reading Input
Requires the user to use `read` command which is used to take the input from the user, the `-p` argument is used along with it.

Use `read -p "Input:" PWN` which gives the output as `Input=` to which enter `COLLEGE` which gives us the flag.

The flag is `pwn.college{Ar1y7qr2PBxs6vntUwuO7Khf56_.dhzN1QDLzkDN0czW}`.

## Reading Files
Requires the user to redirect a file to the `read` command and then read it which gives us the flag.

Use `read PWN</challenge/read_me` which gives us the flag.

The flag is `pwn.college{ky0XrYuTqU5AFHeF4wGXQp8n8la.dBjM4QDLzkDN0czW}`.
