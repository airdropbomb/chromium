# Using Chromium in Vps
Cromium Setup & Removal Instructions
To Install Chromium:

If you want to install Chromium, you can run the following script. This will download and install it for you automatically:

```
source <(wget -O - https://raw.githubusercontent.com/airdropbomb/chromium/refs/heads/main/Chromium.sh)
```

To Remove Chromium:

If you need to remove Chromium from your system, use this set of commands. These will stop the Chromium container, remove it, and clean up the related files:

```
docker-compose -f $HOME/chromium/docker-compose.yaml down && docker rmi lscr.io/linuxserver/chromium:latest && docker volume prune -f && rm -rf $HOME/chromium
```
