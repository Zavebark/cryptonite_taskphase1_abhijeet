# Pondering PATH
This is the last module and contains 4 challenges

## The PATH variable
Requires the user to use `PATH` command and delete the path for `rm` in order to use `/challange/run` which gives us the flag.

Use `PATH=" "` which clears the path for `rm` and now we can use `/challenge/run` which gives us the flag.

The flag is `pwn.college{w1dBCyE1Cv5rfIxYX8-OX_7inC5.dZzNwUDLzkDN0czW}`.

## Setting PATH
Requires the user to overwrite the path to `/challenge/more_commands/` and then we can use `/challenge/run` since now it can access the `win` command.

Use `PATH="/challenge/more_commands/"` after that use `/challenge/run` which gives us the flag.

The flag is `pwn.college{AsxM90LJGlcIl1ZmzfUCKS83eAR.dVzNyUDLzkDN0czW}`.

## Adding Commands
Requires the user to; 
  1. Create a shell script called `win`.
                      
  2. Requires the user to set the `PATH` variable properly.
                      
  3.Then finally run `/challenge/run`.

Use `mkdir setting` and then use `cd` to shift to the `setting` directory and then use `touch win`.

Edit `win` by using `nano` as `nano win` and then add `cat /flag` to `win`.

Now to find the location of `cat` use `echo $PATH` which gives us 
```
cat: '/nix/store/3v4hdb2gmpj7jv2z848ikakhzl9rjgwh-code-server/libexec/code-server/lib/vscode/bin/remote-cli:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin'
```
Analysing this we find that `cat` is in the `/usr/bin` directory.

Now use `chmod a+x win` and then use `PATH="/usr/bin:~/setting"` which gives us the flag.

The flag is `pwn.college{o9G11MAtgr7RiEyuhKyyQEwU-qS.dZzNyUDLzkDN0czW}`.

## Hijacking Commands 
Requires the user to use `/challenge/run` but prevent it from using `rm` and print the flag out.

Create a directory `mkdir final` and move to it using `cd`. Now since the absolute path of `cat` is `/usr/bin/cat` you can override `rm` with it to get the flag.
```
echo "/usr/bin/cat /flag" > rm
```
Also use `chmod a+rwx rm` to make it executable.

Then set `PATH="~/final"` and then use `/challenge/run` which gives us the flag.

The flag is `pwn.college{0APx6CF_zMfKQymv_bI31v3yYLe.ddzNyUDLzkDN0czW}`.
