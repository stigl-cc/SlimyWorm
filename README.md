# Slimy worm
  A malware proof of concept designed to exploit unsecured SSH keys in ~/.ssh/ directory, and uses .ssh/config and the shell history to attempt to spread to as many machines as possible.  
  Once it finds a valid host it can try to exploit, it can easilly copy itself to that machine (and since it uses SCP to copy itself, anti viruses have a hard time blocking it), along with a payload in form of any SSH command to be executed on that machine.  
  It can allow an attacker to easilly move across systems if SSH security is impropertly configured

## How to protect yourself?
  You can use passphrase-protected ssh keys, do not copy private SSH keys across machines, and do not rely on just 1 method of authentication, always use a combination (such as password + ssh key).
  Do not add more authorized ssh keys than you need.

