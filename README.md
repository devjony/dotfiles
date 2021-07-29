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
$EDITOR vars/$TEAM_NAME.yml
```

## Test the playbook
```bash
ansible-playbook -i inventory playbooks/$TEAM_NAME.yml --check
```

## Run the playbook
```bash
ansible-playbook \
-i inventory \ 
playbooks/$TEAM_NAME.yml
```

## License
[MIT](https://choosealicense.com/licenses/mit/)