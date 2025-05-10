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
Reference:
1. https://github.com/jamsnxs/hyprpuccin @ https://www.reddit.com/r/unixporn/comments/1k9yc22/hyprland_some_improvements_to_the_latest_rice_im/

Step 1 - Update package manager
sudo pacman -Syu

Step 2 - Install hyprland
sudo pacman -S hyprland

Step 3 - NVidia setup - NVIDIA GeForce RTX 2070 Max-Q
sudo pacman -S linux-header
sudo pacman -S nvidia-open-dkms

Extras for gaming
sudo pacman -S nvidia-utils
sudo pacman -S lib32-nvidia-utils




```
#   ███╗  ███╗████████╗███╗   ██╗████████╗
#    ╚██╗██╔╝    ══╣██║████╗  ██║    ╔██╔╝
#     ╚███╔╝    ██████║██╔██╗ ██║  ╔██╔╝
#     ██╔██╗     ══╣██║██║╚██╗██║╔██╔╝
#   ███╔╝ ███╗████████║██║ ╚████║████████╗
#   ╚══╝  ╚══╝╚═══════╝╚═╝  ╚═══╝╚═══════╝
```
