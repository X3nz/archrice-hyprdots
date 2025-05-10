# archrice-hyprdots
my Arch + Hyprland Dot Adventure

Arch Installation
Laptop Spec:
Intel Core i7-9750H processor, 16GB of DDR4 RAM
Reference: 
1. https://wiki.archlinux.org/title/Installation_guide
2. https://www.arcolinuxd.com/5-the-actual-installation-of-arch-linux-phase-1-uefi/
3. https://www.arcolinuxd.com/6-the-actual-installation-of-arch-linux-phase-2/
4. https://www.arcolinuxd.com/7-the-actual-installation-of-arch-linux-phase-3/
5. https://www.arcolinuxd.com/choose-a-desktop/

Desktop Manager - Hyprland
Step 1 - Update package manager
sudo pacman -Syu

Step 2 - Install hyprland
sudo pacman -S hyprland

Step 3 - NVidia setup - NVIDIA GeForce RTX 2070 Max-Q
Reference: https://wiki.hyprland.org/Nvidia/
sudo pacman -S linux-header
sudo pacman -S nvidia-open-dkms

Extras for gaming
sudo pacman -S nvidia-utils
sudo pacman -S lib32-nvidia-utils

Rice Template - hyprpuccin
Reference: https://github.com/jamsnxs/hyprpuccin @ https://www.reddit.com/r/unixporn/comments/1k9yc22/hyprland_some_improvements_to_the_latest_rice_im/

Pre Setup
sudo pacman -S git

Step 1 - Shell (zsh + OhMyZsh) 
Reference: https://ohmyz.sh/
sudo pacman -S zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Step 2 - Enhance Shell
Theme
Reference: https://github.com/romkatv/powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"

sudo nano ~/.zshrc
Locate "ZSH_THEME"
Change value to "powerlevel10k/powerlevel10k"

Terminal Emulator
Reference: https://github.com/alacritty/alacritty

git clone https://github.com/alacritty/alacritty.git
cd alacritty

Pre Setup:
Install rustup.rs
Reference: https://rustup.rs/

rustup override set stable
rustup update stable

pacman -S cmake freetype2 fontconfig pkg-config make libxcb libxkbcommon python

Build:
cargo build --release --no-default-features --features=wayland

Configuration
sudo cp target/release/alacritty /usr/local/bin # or anywhere else in $PATH
sudo cp extra/logo/alacritty-term.svg /usr/share/pixmaps/Alacritty.svg
sudo desktop-file-install extra/linux/Alacritty.desktop
sudo update-desktop-database

mkdir -p ${ZDOTDIR:-~}/.zsh_functions
echo 'fpath+=${ZDOTDIR:-~}/.zsh_functions' >> ${ZDOTDIR:-~}/.zshrc

cp extra/completions/_alacritty ${ZDOTDIR:-~}/.zsh_functions/_alacritty

```
#   ███╗  ███╗████████╗███╗   ██╗████████╗
#    ╚██╗██╔╝    ══╣██║████╗  ██║    ╔██╔╝
#     ╚███╔╝    ██████║██╔██╗ ██║  ╔██╔╝
#     ██╔██╗     ══╣██║██║╚██╗██║╔██╔╝
#   ███╔╝ ███╗████████║██║ ╚████║████████╗
#   ╚══╝  ╚══╝╚═══════╝╚═╝  ╚═══╝╚═══════╝
```
