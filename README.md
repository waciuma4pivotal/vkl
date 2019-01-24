# vkl

Use your [github ssh keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) with ease!

## Installation
* Copy the script into your path.
* Make the script executable. (chmod +x) 

## Dependencies
* [Lastpass-CLI](https://github.com/lastpass/lastpass-cli)
* Github ssh private key saved in a secure note in Lastpass `Productivity Tools` folder.
* .git-authors file present in home directory. File should be in [git-duet](https://github.com/git-duet/git-duet) format.
    
## Usage
Call vkl with the initials of the user and the number of hours you intend to use your ssh keys. If the user is not logged into lastpass on the command line, they will be prompted to login.

Example:
`vkl ww 3`

If it is before 6pm local time, omitting the number will autoset the key to expire at 6pm.

Example:
`vkl ww`

## Acknowledgements
Hat tip to [Paul Nikonowicz](https://github.com/pnikonowicz) and Andreas Voellmer who passed along earlier versions of this script.

## FAQ

* ssh_askpass: exec(/usr/X11R6/bin/ssh-askpass): No such file or directory
```
brew install ssh-askpass
sudo brew services start theseal/ssh-askpass/ssh-askpass
pushd /usr/X11r6/bin
sudo ln -s /usr/local/bin/ssh-askpass ssh-askpass
popd
```
