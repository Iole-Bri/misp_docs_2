# ![](img/debian_25.png) Linux

## Connexion wifi - command line

[Source](https://linuxhint.com/3-ways-to-connect-to-wifi-from-the-command-line-on-debian/)

## Créer une image ISO 

Cette partie va me permettre de générer des images ISO à partir de fichiers et de dossiers.
Help : pour MISP

## Dockerfile

#### 1. Créer son Dockerfile

```vim Dockerfile```

<br/>FROM kalilinux/kali-rolling
<br/>RUN apt-get -y update && apt-get -y dist-upgrade && apt-get -y autoremove && apt-get clean
<br/>RUN apt-get -y install nmap
<br/>CMD ["/bin/bash"]

#### 2. Build Image

```sudo docker build -t nmap -f Dockerfile```

<br/>Vérification de la création de l'image :
<br/>```sudo docker image ls```
<br/> Mettre une image du résultat de la commande ci-dessus :

#### 3. Run Container

```sudo docker run --name nmap_cont --rm -i -t nmap bash```

<br/>Vérification de la création de l'image :
<br/>```sudo docker container ls```
<br/> Mettre une image du résultat de la commande ci-dessus :

La commande final "bash" permet d'ouvrir un shell root du container.


