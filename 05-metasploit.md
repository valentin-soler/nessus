# Metasploit

## Installation Metasploit
```
sudo apt update
sudo apt install -y curl

curl -fsSL https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb -o msfinstall
chmod 755 msfinstall
sudo ./msfinstall
```
Et voila c'est installé

![](img/Capture%20d'écran_20261026_132612.png)