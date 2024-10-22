### Post-Installation Configuration

#### System Update
To ensure your system is up-to-date, run:
```bash
sudo dnf upgrade
```

#### DNF Configuration
Open the DNF configuration file:
```bash
sudo nano /etc/dnf/dnf.conf
```
Add the following lines:
```
fastestmirror=True
max_parallel_downloads=10
defaultyes=True
keepcache=True
```

#### Clear Cache
To clear the DNF cache, use:
```bash
sudo dnf clean dbcache
```
or
```bash
sudo dnf clean all
```

#### RPM Fusion Repositories
For media codecs and additional software, enable RPM Fusion:
[Configuration Guide](https://rpmfusion.org/Configuration)
Then, update core packages:
```bash
sudo dnf groupupdate core
```

#### Add Flatpak
For Flatpak support, follow the setup instructions here:
[Flatpak Setup for Fedora](https://flatpak.org/setup/Fedora)

#### Change Hostname
To set your desired hostname, run:
```bash
sudo hostnamectl set-hostname "New_Custom_Name"
```

#### Install NVIDIA Drivers and Codecs
For instructions on installing NVIDIA drivers, visit:
[NVIDIA Howto](https://rpmfusion.org/Howto/NVIDIA)

To install media codecs, use:
```bash
sudo dnf groupupdate multimedia --setop="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin
```
Then, update sound and video packages:
```bash
sudo dnf groupupdate sound-and-video
```

#### Install Apps
Consider installing the following apps and gnome extensions:
- **Extensions**:
  - User Themes
  - Clipboard Manager
  - Accent Themes
  - Asusctl


- **Apps**:
  - Firefox
  - KeePassXC
  - Roggui
  - Spotify 

#### Restart
Finally, restart your system.

#### Install Asusctl
For Asus ROG hardware support, follow the guide here:
[Asusctl Installation Guide](https://asus-linux.org/guides/fedora-guide/)

--- 
