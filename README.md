# wireguard-ui-setup

A wsimple script to install Wireguard and Wirguard-ui

## Features

- Automate minimal installation of Wirguard and Wireguard-ui
- Setup a strict firewall

## Usage

Download the script on your server:
```bash
wget https://gitlab.com/maelj/wireguard-ui-setup/-/raw/master/install.sh?inline=false -O /tmp/install.sh
```

_Personalise with your parameters:_

**wg_port="51820":**  
**wg_network="10.252.1.0/24":**
**wg_interface="wg0":**
**system_interface="ens18":**
**ssh_port="22":**
**admin_ip="client.domain.tld":**
**wgui_link="https://github.com/ngoduykhanh/wireguard-ui/releases/download/v0.2.7/wireguard-ui-v0.2.7-linux-amd64.tar.gz":**
**wgui_path="/opt/wgui":**
**wgui_bin_path="/usr/local/bin":**
**systemctl_path="/usr/bin/systemctl":**
**deb_backport="deb https://deb.debian.org/debian/ buster-backports main":**

Execute the script
```bash
bash /tmp/install.sh
```

At this point you should be able to acces wireguard-ui.  
Open a new ssh connection with port forwarding

```bash
ssh -L 5000:localhost:5000 user@vpn_server_ip
```

Access http://localhost:5000 from your favorite browser.
