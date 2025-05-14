# 🚀 Ubuntu Setup Guide

This guide provides step-by-step instructions to set up a productive and visually appealing Ubuntu development environment.

---

## ⚙️ SYSTEM

### 1. Install `libfuse2` (for AppImage support)

```bash
sudo apt update
sudo apt install libfuse2
```

### 2. Install `ibus-unikey` (Vietnamese input method)

```bash
sudo apt update
sudo apt install ibus-unikey
ibus restart
```

---

## 👨‍💻 DEVELOPER TOOLS

### 1. Git

```bash
sudo apt update
sudo apt install git
```

### 2. Visual Studio Code

```bash
sudo snap install code --classic
```

### 3. .NET SDK 8.0

```bash
sudo apt install -y wget
wget https://packages.microsoft.com/config/ubuntu/24.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb

sudo apt update
sudo apt install -y dotnet-sdk-8.0

# Check installation
dotnet --version
```

### 4. Node.js, npm, TypeScript, Yarn

```bash
sudo apt install curl
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs

# Global TypeScript
npm install -g typescript

# (Optional) Install Yarn
npm install -g yarn
```

### 5. Docker

```bash
sudo apt install docker.io
sudo systemctl enable --now docker
sudo usermod -aG docker $USER
```

### 6. Postman

```bash
sudo snap install postman
```

### 7. DBeaver (Database GUI Client)

```bash
sudo snap install dbeaver-ce
```

### 8. Install Meslo Nerd Fonts (for terminal themes)

```bash
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts

# Download fonts
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf

# Update font cache
fc-cache -fv
```

### 9. Install Zsh and Oh My Zsh

```bash
sudo apt update
sudo apt install zsh -y

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Change default shell
chsh -s $(which zsh)

# Add autosuggestions plugin
git clone https://github.com/zsh-users/zsh-autosuggestions \  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

---

## 🎨 CUSTOM THEME

### 1. Install GNOME Tweaks and Extensions

```bash
sudo apt update
sudo apt install gnome-tweaks gnome-shell-extensions
```

### 2. Install WhiteSur GTK Theme

```bash
sudo apt install git
git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git
cd WhiteSur-gtk-theme
./install.sh
```

### 3. Install WhiteSur Icon Pack

```bash
git clone https://github.com/vinceliuice/WhiteSur-icon-theme.git
cd WhiteSur-icon-theme
./install.sh
```

### 4. Install San Francisco Pro Fonts

- GitHub Repo: [San Francisco Pro Fonts](https://github.com/sahibjotsaggu/San-Francisco-Pro-Fonts)

```bash
mkdir -p ~/.fonts
cp path/to/downloaded/fonts/*.ttf ~/.fonts/
fc-cache -fv
```

### 5. Install CompizConfig Settings Manager (CCSM)

```bash
sudo apt install compiz compizconfig-settings-manager compiz-plugins
# Launch with: ccsm
# Enable effect: Wobbly Windows
```

### 6. Install GNOME Extension Manager

```bash
sudo apt install gnome-shell-extension-manager
```

---

✅ **After Installation:** Open GNOME Tweaks (`gnome-tweaks`) to select your theme, icons, and fonts.  
You may need to **logout/login** to apply changes.
