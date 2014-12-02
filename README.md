custom_commands
===============

Contains custom commands to be run from the terminal. Have only been tested in the mac os x terminal

These files should be moved to: `/usr/local/bin/` and must be set as executable: `chmod +x <file_name>`

##gcheckout
This command I made because I'm lazy and was tired of writing out entire branch names when switching branches.
This command will output all branch names for the current repository then you just need to enter the number
corresponding to the branch name and it will switch to that branch.

Example:

```
$ gcheckout
 => 1. master
 => 2. develop
Enter the number of the branch you want to checkout to:
2
 => Switched to branch 'develop'
 => Your branch is up-to-date with 'origin/develop'.
````

##search
This command is used to `grep` recursively for a pattern that is passed in as an argument.
By default it runs from the current directory, will search nested directories, and is case
insensitive. Without passing any flags it will list the file name, line number, and content
that matches in the file. By passing the `-f` flag as the first argument it will just list the file names
that match the pattern.

I have to credit `granolocks` who introduced my and taught me about the commands used in the script.

Example:

```
# Without -f flag:
$ search greg
 => ./file1.txt:2:Hello my name is Greg.
 => ./file1.txt:5:LALALALALAL Gregorious.
 => ./some_rby.rb:1:class Greg
 => ./some_rby.rb:3:    puts 'Greg'


# With -f flag:
$ search -f greg
 => ./file1.txt
 => ./some_rby.rb
````
