# creating_multiple_ssh_keys
#### guide on how to generate multiple ssh keys and adding to github

 ### Generate the ssh key-pairs and add in `-f` to state the name and location of the file
 ssh-keygen -t rsa -b 4096 -C "jennxf.ng@gmail.com" -f ~/.ssh/id_rsa_name

### start the ssh-agent in the background if it's not already running
eval "$(ssh-agent -s)"

### start the new ssh agent (very important)
ssh-add ~/.ssh/id_rsa_name

### next copy the new id_rsa_name.pub into Github
pbcopy < ~/.ssh/id_rsa_name.pub 

### paste in Github
https://github.com/settings/keys

### Done
