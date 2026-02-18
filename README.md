## install node.js using nvm
```
-- sudo apt update
   sudo apt upgrade -y

-- sudo apt install curl build-essential libssl-dev -y

-- curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash

-- source ~/.bashrc

-- nvm install --lts or nvm install 24

-- node -v
   npm -v
   nvm alias default <version_number> # e.g., nvm alias default 24 to set default version
   
   install pnpm
-- curl -fsSL https://get.pnpm.io/install.sh | sh -
   
   optional
-- sudo apt remove curl -y
   sudo apt remove build-essential libssl-dev -y
   sudo apt autoremove -y
```   
## antigravity

link - https://antigravity.google/download/linux

## git

install
-- sudo apt update
   sudo apt install git -y
   
global user
-- git config --global user.name "Your Name"
   git config --global user.email "your@email.com"
   
SSH key
-- link: https://claude.ai/share/a5f90056-3382-4641-8bc0-4ddfb4fea389

## ngrok

-- sudo snap install ngrok
   authenticate using token

## FileZilla

-- sudo apt update
   sudo apt install filezilla -y
