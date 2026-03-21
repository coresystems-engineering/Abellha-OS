# Abéllha OS Installation Guide
-------------------------------
*Please, download this file!
-------------------------------
*The cause is that it will be confuse if not downloaded!*

Firstly, install Debian or Ubuntu on your PC that will use Abéllha OS, recommended on **GNOME Session**. After the installation open the terminal and type or paste: sudo nano /etc/os-release type your password and when nano appears change everything from the original to this 

PRETTY_NAME="Abéllha OS"
NAME="Abéllha OS"
VERSION_ID="1"
VERSION="1 (Xenon)"
VERSION_CODENAME=xenon
DEBIAN_VERSION_FULL=1.0
ID=abéllha
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"

Press Control (CTRL) + O, Enter and Control + X.
Now run sudo apt update
sudo apt install gnome-shell-extension-manager dconf-editor git flatpak -y

And this sudo apt install gnome-shell-extensions gnome-shell-extension-dash-to-panel gnome-shell-extension-arc-menu -y
Now, you are changing the Debian logo on fastfetch to the Abéllha OS logo. So lets go!
First mkdir -p ~/.config/fastfetch and fastfetch --gen-config ~/.config/fastfetch/config.jsonc .
Add the file in Fastfetch folder (fastfetcher.txt) to your ~/ (user) folder; and do this command nano ~/.config/fastfetch/config.jsonc and in nano add this:

{
  "$schema": "https://github.com/fastfetch-cli/fastfetch/raw/dev/doc/json_schema.json",
  "logo": {
    "source": "/home/yourusername/fastfetcher.txt",
    "type": "auto",
    "padding": {
      "top": 1,
      "right": 2
    },
    "color": {
      "1": "red"
    }
  },
  "modules": [
    "title",
    "separator",
    "os",
    "host",
    "kernel",
    "uptime",
    "packages",
    "shell",
    "display",
    "de",
    "wm",
    "wmtheme",
    "theme",
    "icons",
    "font",
    "cursor",
    "terminal",
    "terminalfont",
    "cpu",
    "gpu",
    "memory",
    "swap",
    "disk",
    "localip",
    "battery",
    "poweradapter",
    "locale",
    "break",
    "colors"
  ]
}

Attention! in the line of source change "yourusername" to your user name!!!

After this, try fastfetch and see if takes a red X as logo, if yes, well, well done!
So next part, is customizing the terminal(Yeah its possible, but limitated). Do sudo nano ~/.bashrc and paste on the final of the block:

echo -e "\e[1;34mWelcome to the\e[0m \e[1;31mTerminal\e[0m"

export PS1="\[\e[1;93m\]\u@\h\[\e[0m\]:\[\e[1;34m\]\w\[\e[0m\]\$ "

***PLEASE DO NOT EDIT ANYTHING ELSE ON sudo nano ~/.bashrc***
Now grub, ahh grub. So download my grub custom image, on grub folder (note, if you think the images strange, that's because they were made on GIMP, and the cursor too). After downloaded, obviously, another nano **sudo nano /etc/default/grub**, and add *GRUB_BACKGROUND="/boot/grub/abellha_grub.png"*. If it has an GRUB_BACKGROUND="" replace to GRUB_BACKGROUND="/boot/grub/abellha_grub.png". Don't change nothing else on the file. And to finalize sudo update-grub. Now turn off your PC and restart again. It will appear Debian GNU/Linux Trixie, or anything else, click E key and it will appear in such text editor. and you try find of the Debian GNU/Linux Trixie or if it is Bookworm, or if is Ubuntu, look to Ubuntu, and change to Abéllha OS 1 Xenon GNU/Linux. (Xenon is the version codename, such version is 1). Do not remove any "" or anything else of the file. at the bottom, click the key that means to run with the changes or anything that is a synonymous of it.

Now the wallpaper. You will use the same wallpaper as grub, but to take it tidy, its to download on Wallpapers folder(it have an another blue version of it).
