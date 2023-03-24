# windows 11 - wsl2 setup
## installing linux
- open powershell
- wsl --install -d Debian
- it would take sometime time install
- enter username and password when prompted

Note: WSL was hanging due to the recent window update. Based on the suggestion in one of blog post, I have uninstalled a recent windows update.
I hope there won't further problem with my WSL setup.

## Linux env setup
- update and upgrade linux - sudo apt-get update; sudo apt-get upgrade
- install zsh - sudo apt-get install zsh
- install curl - sudo apt-get install curl
- install git - sudo apt-get install git
- install ohmyzsh 'sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"'
- add 'jump' plugin in .zshrc
### git setup
- git config --global user.name "Aadini Tech"
- git config --global user.email techaadini@gmail.com
#### github ssh setup - new key
- ssh-keygen -t ed25519 -C "xxxx1234@gmail.com"
- eval "$(ssh-agent -s)"
- ssh-add ~/.ssh/id_ed25519
- cat ~/.ssh/id_ed25519.pub
- copy the string printed in paste in github->settings->ssh and gpg keys-> click button 'New SSH key' -> pass the copied key ->  click "Add SSH key" button
- verify ssh -T git@github.com
