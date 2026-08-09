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
```
install
-- sudo apt update
   sudo apt install git -y
   
global user
-- git config --global user.name "Your Name"
   git config --global user.email "your@email.com"
   
SSH key
-- link: https://claude.ai/share/a5f90056-3382-4641-8bc0-4ddfb4fea389
```

## ngrok
```
-- sudo snap install ngrok
   authenticate using token
```

## FileZilla
```
-- sudo apt update
   sudo apt install filezilla -y
```

## Claude Desktop
***Download***
```
curl -fsSL https://aaddrick.github.io/claude-desktop-debian/KEY.gpg | sudo gpg --dearmor -o /usr/share/keyrings/claude-desktop.gpg

echo "deb [signed-by=/usr/share/keyrings/claude-desktop.gpg arch=amd64,arm64] https://aaddrick.github.io/claude-desktop-debian stable main" | sudo tee /etc/apt/sources.list.d/claude-desktop.list

sudo apt update
sudo apt install claude-desktop
```

***MCP Server config for filesystem***
```
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/home/<name>/Desktop",
        "/home/<name>/Downloads"
      ]
    }
  }
}
```
* link: [git](https://github.com/aaddrick/claude-desktop-debian)
* link: [reddit](https://www.reddit.com/r/ClaudeAI/comments/1hmrtlz/claude_desktop_for_debianbased_linux/)

## Kazam screen recorder
***Install***
```
sudo apt update
sudo apt install kazam -y
```
***Fix black screen***
```
sudo nano /etc/gdm3/custom.conf
```
uncomment waylandenable=false


## OBS

```
sudo apt update
sudo apt install ffmpeg

sudo add-apt-repository ppa:obsproject/obs-studio

sudo apt update
sudo apt install obs-studio
```

## Update localwp by Flywheel
* Download latest version
* Close local
* Install & Fix Dependency Issues via terminal
*local-x.x.x-linux.deb - downloaded file name
```
cd ~/Downloads && sudo dpkg -i local-x.x.x-linux.deb
sudo apt install -f
```
mysql error missing library fix: [link](https://claude.ai/chat/49e0320b-77b4-45f1-bf9e-63bf9e27406f)
```
sudo apt install libaio1t64
sudo ln -s /usr/lib/x86_64-linux-gnu/libaio.so.1t64 /usr/lib/x86_64-linux-gnu/libaio.so.1
sudo ldconfig
```
```
sudo apt install libncurses-dev
sudo ln -s /usr/lib/x86_64-linux-gnu/libncurses.so.6 /usr/lib/x86_64-linux-gnu/libncurses.so.5
sudo ldconfig
```
```
sudo apt install libtinfo5
# or symlink if not found:
sudo ln -s /usr/lib/x86_64-linux-gnu/libtinfo.so.6 /usr/lib/x86_64-linux-gnu/libtinfo.so.5
sudo ldconfig
```
**Fix LocalWP launching issues:**
***try to open using terminal:***
```
 /opt/Local/local
```
***Fix (SUID sandbox permission issue):***
```
sudo chown root:root /opt/Local/chrome-sandbox
sudo chmod 4755 /opt/Local/chrome-sandbox
```


## Bluetooth Headphone sound interruption
```
sudo apt update && sudo apt install blueman

open bluetooth manager app
select device and right click
Audio Profile থ-> High Fidelity Playback (A2DP Sink) 
```

## Stickynotes
```
https://github.com/pavel-glukhov/linsticky?tab=readme-ov-file#snap-store-recommended
```
