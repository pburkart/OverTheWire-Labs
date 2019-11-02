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


## Bandit 2

Once you collect the flag from Bandit1 you will be able to 
move on to Bandit2 by connecting to bandit.labs.overthewire.org
on port 2220 via SSH with the Flag from the previous challenge.

Once logging into Bandit2 you will find a single file in the ~
directory called "spaces in this filename". In order to read 
this file, all you have to do is encapsulate the file in double
quotes when invoking the cat command. 

cat "spaces in this filename"

Doing the above command will present you with the flag for this
challenge, and the password for Bandit3. 

## Bandit 3 

Once you connect to bandit.labs.overthewire.org on port 2220
with the Bandit3 user account and the password being the flag
for the Bandit 2 challenge, you will find yourself with one
directory called 'inhere' in the ~ directory. 

Upon changing into this directory, you will initially not find 
any files. This is because they're hidden. In order to view all 
files, you can add the -a switch to the dir command. Doing this 
will present you with the .hidden file, which you can read 
normally with the cat command. Once you do this, you will be 
presented with the flag for the challenge and the password for 
Bandit 4.

## Bandit 4

Similar to the Bandit 3 challenge, when you login to the Bandit4
user account, you will be presented with an /inhere directory.
This time however it contains 10 dashed file names labeled
-file00 through -file09. The flag is contained in ./-flag07.
