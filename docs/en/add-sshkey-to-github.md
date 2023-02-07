# Add SSH key to Github

Basic example:

- Create a new key

```bash
ssh-keygen -t ed25519 -C your@mail.com
```
It will ask for optional alt' name or passphrase creation. Can ignore them and just press Enter.

- Start the SSH agent

```bash
eval "$(ssh-agent -s)"
```
- Add the key to the agent

Edit, or create'n'edit ~/.ssh/config  

```bash
vim ~/.ssh/config 
```
add thhis to the file:

```bash
Host *
	AddKeysToAgent yes
	IdentityFile ~/.ssh/id_ed25519 
```
Run it to add the identity 

```bash
ssh-add ~/.ssh/id_ed25519 
```
Copy the key content

```bash
cat ~/.ssh/id_ed25519.pub
```
- Head to https://github.com 

In Setting > SSH &GPG keys click on the [New SSH key] button

Paste the copied key into the textarea, give it a title. Done!

## RTFM

Inside the terminal, `man ssh`

## YouTube

https://www.youtube.com/watch?v=8X4u9sca3Io


