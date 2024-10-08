# File Globbing
The fifth module to be completed and contains 6 challenges.

## Matching with *
Requires the user to use `*` to change directory while keeping the argument less then or equal to 4 characters.

Using `cd /ch*` we succesfully change to challenge directory hence now use `/challenge/run` which gives us the flag.

The flag is `pwn.college{UNVtV_ZX7m8SfHzwcaO_7wsigWm.dFjM4QDLzkDN0czW}`.

## Matching with ?
Requires the user to use `?` to change directory to `challenge` while keeping c&l as `?`.

Using `cd /?ha??enge` and then using `/challenge/run` we get the flag.

The flag is `pwn.college{QmVI5d9H5IJxxLMeWHnKmiWyWCz.dJjM4QDLzkDN0czW}`.

## Matching with []
Requires the user to use `[]` to look for many files at the same time which will give us the flag.

Use `cd /challenge/files` and then use `/challenge/run file_[bash]` which gives us the flag.

The flag is `pwn.college{onPucbGe0Y06tNEHXnxar7153nc.dNjM4QDLzkDN0czW}`.

## Matching paths with []
Requires the user to use a single argument to find the flag using `[]`.

Use `/challenge/run /challenge/files/file_[bash]` which gives us the flag.

The flag is `pwn.college{kmxFYLKEGyTENoZtzpkQyhCDRvU.dRjM4QDLzkDN0czW}`.

## Mixing Globs
Requires the user to use `*`,`?`&`[]` to write a single glob less then or equal to 6 characters.

Use `cd /challege/files` and then use `/challenge/run [cep]*` which gives us the flag.

The flag is `pwn.college{woHDlR4rEulQSyOkb8hAhxn6z5p.dVjM4QDLzkDN0czW}`.

## Exclusionary globbing
Requires the user to use `!` which is used to indicate that except for it everything else should be shown.

Use `cd /challenge/files` and then use `/challenge/run ![pwn]*` which gives us the flag.

The flag is `pwn.college{QIU8S4jxPVOR36BMA4Yux1RMVYc.dZjM4QDLzkDN0czW}`

