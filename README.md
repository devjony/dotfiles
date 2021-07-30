# dotfiles
This repository contains the ansible playbook files to setup a shield's team workstation 

## Requirements
```bash
sudo apt update && \
  sudo apt install curl git python3-apt ansible -y
```

## Run Locally
```bash
git clone https://github.com/devjony/dotfiles.git && \
  cd dotfiles && \
  git checkout pags
```

## Edit the variables accordingly
```bash
$EDITOR vars/user.yml
```

## Test the playbook
```bash
ansible-playbook \
-i inventory \ 
playbooks/shield.yml --check
```

## Run the playbook
```bash
ansible-playbook \
-i inventory \ 
playbooks/shield.yml
```

## License
[MIT](https://choosealicense.com/licenses/mit/)