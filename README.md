# APT repository for public telekom-mms packages
To use repo in your environment use following commands to setup source list with related key:
```
wget -O- https://telekom-mms.github.io/linux-apt/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/github-telekom-mms.gpg > /dev/null
echo 'deb [arch=amd64 signed-by=/usr/share/keyrings/github-telekom-mms.gpg] https://telekom-mms.github.io/linux-apt/repo jammy main' | sudo tee /etc/apt/sources.list.d/github-telekom-mms.list

sudo apt update
sudo apt install fw-id-agent oc-daemon corp-net-indicator
```