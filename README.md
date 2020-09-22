## My devbox setup
### Automated via Ansible

A playbook that automate the steps I take
after the installation of my box.

This is all very opinionated and changing with my mood :-)
Infact - for the whole package I suppose I'm the only user, 
but you can be interested on best-practices for installing some 
of the sofware here.

This will be a playground and a perennial
work in progress, but feedback is appreciated.

### Installed packages

* various Linux system tools
* various development libraries and tools
* Google Chrome beta
* Setup no-sudo password for current user
* Design tools: Gimp, Inkscape, Gravit-designer
* DB: MongoDB, postgresql, Redis
* Social: Slack, Skype
* Network: OpenSSH server
* Docker
* Audio: Spotify desktop app
* Sublime Text 3

### Usage

On recent Ubuntu versions - the fastest way to get started
is installing Ansible with APT:

    sudo apt install ansible

* And then run the script:

		./run.sh
		
At the beginning, you probably aren't in the password-less, in that case
if you get a `sudo: a password is required` you can type your user password
here running `./run.sh -K`
		
### Notes
You can eventually run a subset of tasks passing 
tags option to run.sh, for example:
  
  	/run.sh --tags social
  
  Available tags:
  
  _social, multimedia, design, audio, db, docker, development,
  python, ruby_

Ansible will take care of changes, so it is safe to run the script
as many time as you like.


### References:

*	http://docs.ansible.com/ansible/latest/index.html
*	https://blog.josephkahn.io/articles/ansible/
*	https://michaelheap.com/ansible-installing-google-chrome/
