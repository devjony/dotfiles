# dotfiles
This repository contains the ansible playbook files to setup a shield's team workstation 

## Requirements
```bash
sudo apt update && \
  sudo apt install openssh-server sshpass ansible && \
  eval $(ssh-agent)

sudo ufw allow ssh && \
  sudo ufw enable
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
ansible-playbook -i inventory $TEAM_NAME.yml --check
```

## Run the playbook
```bash
ansible-playbook \
-u $(whoami) \
-i inventory $TEAM_NAME.yml
```

## License
[MIT](https://choosealicense.com/licenses/mit/)