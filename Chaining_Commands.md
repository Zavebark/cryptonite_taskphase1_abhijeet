# Chaining Commands
This is the 11th module and contains 4 challenges.

## Chaining With Semicolons
Requires the user to chain two commands using `;`.

Use `/challenge/pwn;/challenge/college` which gives us the flag.

The flag is `pwn.college{YMHNfDNfsArXtNOo74xyyUToFPI.dVTN4QDLzkDN0czW}`.

## Your First Shell Script
Requires the user to use a shell script.

Create a shell script by using `touch x.sh` now use `nano` to edit as `nano x.sh`.

Now use `bash x.sh` which gives us the flag.

The flag is `pwn.college{EM_uYQoBfmpSUnXkYyP67ORGQnz.dFzN4QDLzkDN0czW}`.

## Redirecting Script Output
Requires the user to make a shell script and then use piping to direct the output to another program which will give the flag.

Use `touch x.sh` and then use `nano x.sh`.

Now use `bash x.sh|/challenge/solve` which gives us the flag.

The flag is `pwn.college{8qNiWh8TjfY8gad6G1Mhn4FwBUr.dhTM5QDLzkDN0czW}`.

## Executable Shell Scripts
Requires us to invoke the shell script without using `bash` by changing the file permisions.

Use `touch x.sh` and then use `nano x.sh` and change the contents of `x.sh` to `/challenge/solve`.

Now use `chmod u+x x.sh` and then use `./x.sh` which executes without using the `bash` command and gives us the flag.

The flag is `pwn.college{g17Zdf2Gg8QE8n6ckWgzRWTzWFF.dRzNyUDLzkDN0czW}`.
