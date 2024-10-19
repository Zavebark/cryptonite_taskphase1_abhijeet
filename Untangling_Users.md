# Untangling Users
This is the 10th module and contains 4 challenges.

## Becoming root with su
Requires the user to use `su` to become the root and find the flag consequently.

Use `su` and then enter the password to be `hack-the-planet`.

Then use `cat /flag`.

The flag is `pwn.college{MgZsI8jim9R5-Vie9f_nO5QUGp3.dVTN0UDLzkDN0czW}`.

## Other users with su
Requires the user to use `su` with an argument in order to change the user as well.

Use `su zardus` and then use the password to be `dont-hack-me`.

Then use `/challenge/run`.

The flag is `pwn.college{ckqQ0NfWoP-4WkssC_3qVl34cPg.dZTN0UDLzkDN0czW}`.

## Cracking Passwords
Requires the user to crack the password using a password leak by using `John The Ripper` and then shifting to the `zardus` shell and then using `/challenge/run`.

Use `cd /challenge` then use `john ./shadow-leak` which gives the password to be `aardvark`.

Now using the password `aardvark` with `sh zardus` and then using `/challenge/run` we get the flag.

The flag is `pwn.college{EjB-JD3_DHY4-XtcH6WWFWN5zt3.ddTN0UDLzkDN0czW}`.

## Using SUDO
Requires the user to use `SUDO` in order to get the final flag.

Use `sudo cat /flag` which gives us the flag.

The flag is `pwn.college{003wfyl70lbZTK_6rGJMhpfElii.dhTN0UDLzkDN0czW}`.
