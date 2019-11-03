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

## Bandit 5

Upon connecting to Bandit 5 you will find dozens of files in 
multiple subdirectories, and your task is to find the file that
is human-readable, 1033 bytes in size, and not exectuable.

This can be done with the following command:

find . -type f -size 1033c ! -executable -exec sh -c 'file -b $0 | grep -q text' {} \; -print

Doing this will return the file with the flag, which can of course
be read using the cat command.

## Bandit 6

Now that you've familiarized yourself with the "find" command you
should find this challenge to be even easier than the last. This
challenge requires you to find a file owned by the user bandit7
and the group bandit7. It also asks you to find the file that
is 33 bytes in size, but I found this didn't make the search any
easier.

My solution was to simply enter the following command:

find -group "bandit6" -user "bandit7"

This command returns a bunch of results, but all but one of them
are ended with "Permission Denied", which is the file that 
contains the flag. For users who are better with grep, I'm sure
you can also pipe these results into grep, to output the only 
line that didn't contain permission denied. 
