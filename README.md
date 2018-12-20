# vkl

Use your [github ssh keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) with ease!

## Installation
* Copy file into your path.
* Make the file executable. (chmod +x) 

## Dependencies
* [Lastpass-CLI](https://github.com/lastpass/lastpass-cli)
* Save your github ssh private key in a secure note in the Lastpass `Productivity Tools` folder.
* .git-authors file is present in home directory. File should be in [git-duet](https://github.com/git-duet/git-duet) format.
    
## Usage
Call vkl with the initials of the user and the number of hours the SSH keys should be added to the ssh-agent. If the user is not logged into lastpass on the command line, they will be prompted to login.

Example:
`vkl ww 3`

If it is before 6pm local time, omitting the number will autoset the key to expire at 6pm.

Example:
`vkl ww`