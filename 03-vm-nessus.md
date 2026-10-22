# Nessus

Nous allons maintenant installer Nessus sur une machine virtuel (2vCpu/8Go de Ram/64 Go de stockage).

## Prérequis & Installation

Vous pouvez récupéré votre version d'essaie [ici](https://www.tenable.com/tenable-nessus-for-education), Aprés avoir remplis le questionnaire pour la demande d'essaie, vous allez tomber sur cette page.

![](img/Capture%20d'écran_20261022_114335.png)

Vous pouvez maintenant récupéré le paquet et l'installer 
```
curl --request GET \
  --url 'https://www.tenable.com/downloads/api/v2/pages/nessus/files/Nessus-10.12.5-debian10_amd64.deb' \
  --output 'Nessus-10.12.5-debian10_amd64.deb'
dpkg -i Nessus-10.12.5-debian10_amd64.deb
systemctl start nessusd.service
```
Vous avez maintenant accées via l'interface web via `https://<ip-machine>:8834/`
Vous devez patienter quelque instant le temps de l'initialisation

![](img/Capture%20d'écran_20261022_114816.png)

Nous allons maintenant le configurer via l'interface web

![](img/Capture%20d'écran_20261022_115218.png)

Vous devez choisir la version que vous souhaité utilisé (Personnellement, étant étudiant je suis éligible a la version éducation) et renseignez votre clé de licence

![](img/Capture%20d'écran_20261022_115738.png)
![](img/Capture%20d'écran_20261022_115630.png)

Choisissez un nom d'utilisateur et un mot de passe

![](img/Capture%20d'écran_20261022_133157.png)

Repatienter un petit peu

![](img/Capture%20d'écran_20261022_133352.png)

Et voila c'est installer !

## Scan de notre premiére victimes

Nous allons faire un scan sur notre machine vulnérable (ici 10.10.10.103)

![](img/Capture%20d'écran_20261022_140623.png)

![](img/Capture%20d'écran_20261022_140738.png)

Patientez un peu

![](img/Capture%20d'écran_20261022_140846.png)

Et voila ! Comme on peut le voir notre machine est un gruyére

![](img/Capture%20d'écran_20261022_142726.png)

![](img/Capture%20d'écran_20261022_142935.png)