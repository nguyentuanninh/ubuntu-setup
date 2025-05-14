# Setup Ubuntu

# SYSTEM
## 1. ibus-unikey
```bash
sudo apt update
sudo apt install ibus-unikey
```

```bash
ibus restart
```

---


#  CUSTOME THEME
## 1. Install GNOME Tweaks and Extensions

GNOME Tweaks is a tool to customize the GNOME desktop environment.

```bash
sudo apt update
sudo apt install gnome-tweaks gnome-shell-extensions
```

---

## 2. Install WhiteSur GTK Theme

WhiteSur is a macOS-inspired GTK theme.

### Step 1: Install Git (if not already installed)

```bash
sudo apt install git
```

### Step 2: Clone and install the WhiteSur theme

```bash
git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git
cd WhiteSur-gtk-theme
./install.sh
```

---

## 3. Install WhiteSur Icon Pack

```bash
git clone https://github.com/vinceliuice/WhiteSur-icon-theme.git
cd WhiteSur-icon-theme
./install.sh
```

---

## 4. Install San Francisco Pro Fonts

San Francisco Pro is Apple's official font.

### Download the fonts

- GitHub Repo: [San Francisco Pro Fonts](https://github.com/sahibjotsaggu/San-Francisco-Pro-Fonts)

### Install fonts to system

```bash
# Create fonts directory if it doesn't exist
mkdir -p ~/.fonts

# Copy all .ttf font files to the directory
cp path/to/downloaded/fonts/*.ttf ~/.fonts/

# Update font cache
fc-cache -fv
```

---

## 5. Install CompizConfig Settings Manager (CCSM)

This tool allows you to enable visual effects like Wobbly Windows.

```bash
sudo apt install compiz compizconfig-settings-manager compiz-plugins
```

- Launch with: `ccsm`
- Enable effect: **Wobbly Windows**

---

## 6. Install GNOME Extension Manager

This allows you to manage GNOME Shell extensions more easily.

```bash
sudo apt install gnome-shell-extension-manager
```

---

✅ **After Installation:** Open GNOME Tweaks (`gnome-tweaks`) to select your theme, icons, and fonts.  
You may need to **logout/login** to apply changes.
