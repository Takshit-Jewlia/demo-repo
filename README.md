# Demo

1) .md stands for markdown, allows for convinient text editing
2) "#" is used for headings
3) Same as in google collab

## Subheader
 Testing

## Commands
### ls -la
:list everything in the directory including hidden files and folders
### git status
shows which files are modified (need to be saved) 
and which files are untracked i.e. that are new/not recognized by git repo
### git add
creating new file in the repo locally isnt tracked my git by default. git add is used to make it track
git add . 
using period implies to track every file in the current folder
### git commit -m "<message>"
or git commit -m "<message>" -m "Some description"
-m stands for message, we need to have a message for every commit. Message can be meaningless if needed.
generally it's the what or why you are making the particular change
### git push
even after git commit, the changes are not live. To make them live to sync with the repo on github, git push is used.
### SSH keys
to push the commits, ownership needs to be proven. Which is done via SSH keys
in git-bash
$ ssh-keygen -t rsa -b 4096 -C "takshitjewlia49@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/dell/.ssh/id_rsa): testkey
Enter passphrase for "testkey" (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in testkey
Your public key has been saved in testkey.pub
The key fingerprint is:
SHA256:tI7as541QVjmwiJ/pYnAQoo00ztA0Cyj6jCGwQAPErY takshitjewlia49@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
|X@.     o        |
|@=*. . =         |
|BE* o + =        |
|oo * o B .       |
|o.  + + S        |
|=.   . o .       |
|+.    . +        |
| .   o.o .       |
|    ..=o         |
+----[SHA256]-----+

then to see the key
ls -la | grep testkey(name of the key)
testkey                 (private key)
testkey.pub             (public key)

cat testkey.pub

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQDN6KuoSD7bN6jPqe5FRKzyObspFqIlelegGDvPrsMM052L1Dt48rgUHDu1ILc8Djdg1e5Wnj7XYL2fLehZgSIRpGEgGQjzsUsQ0qNPnyU1AhpCVcD5/LMSOk79r8qTt9ZR1khWFHJod4pXTVnl1u4bdtxCkWT17S9iwyI/MHThI9JKfrHNFWzSYU4hkEdv7qWwQuPjQAA0HHnPYGlf+GuSBRQaOPFgOwM77N8LnstQ01PtfabTzuEbwHghc7lcEuWgfrJP9TReOv2tJrcJxE00U77zKqHq+i2EsApNupXNgtmUX/rIR5QExZ6RaVs8e7ajxXJbYjVWwNWtvjlD1qyChkKgQu53b+J7OVuMS9tzfHBXs63SLGRw+Dr8Q+xCEX1+Cg82JMOcZKM6cKZqQnzc7JVEF0+meRgKQ5vO5s/10BNKOSliDJTebK0QM4RJziMCLQzDTOg3FM8OqR1woTjm+4ed0RwANBJPGtZn9SE4SV23KIwBUE2p7XnU0/NP66MJayAriyZUkDUnCkkubOYe7NTKBhwmZb25c0yqXTbgYMZERcSt4XL7KboRMCvW/o3OLRP/BcY1fVzyTSKX5DH+2iwr3pWZ/KqyXcXeLT3sLs7zXnkeaP0Vi9j7qeJjSmFtprHyhO1zdUPztjD1j9O0w8Wtw6rlsDfXh/LBm4htfw== takshitjewlia49@gmail.com

then we copt the whole thing
