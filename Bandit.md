# Bandit

## Bandit 0

Upon initially starting off with Bandit labs all you will need
to do is connect to bandit.labs.overthewire.org via SSH on port
2220 with the username and password Bandit0. Once you do this
there will be a single file at the ~ directory called 'readme'.
This file contains the "flag" for the level, which acts as the 
password for Bandit 1.

## Bandit 1

Once you complete Bandit 0 and get the password for Bandit1,
you can go ahead and connect to bandit.labs.overthewire.org with
the username Bandit1 and the password being the flag for Bandit0
(see the flags.txt file for all passwords). When you connect to
Bandit1 you will find a single file in the ~ directory with a 
filename of "-". If you try and open up the file however, it 
won't let you, as - is a convention that a lot of programs
use to refer to stdin. 

In order to get around this you will need to refer specifically 
to the - file. To view the contents of the file, we can type 
'cat ./-'. Doing this will print out the flag for Bandit1, 
and also the password for Bandit2.



