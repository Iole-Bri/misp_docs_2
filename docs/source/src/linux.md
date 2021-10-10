# ![](img/debian_25.png) Linux

## Connexion wifi - command line

[Source](https://linuxhint.com/3-ways-to-connect-to-wifi-from-the-command-line-on-debian/)

## Créer une image ISO 

Cette partie va me permettre de générer des images ISO à partir de fichiers et de dossiers.
Help : pour MISP

## Dockerfile

#### 1. Créer son Dockerfile

```vim Dockerfile```

    FROM kalilinux/kali-rolling
    RUN apt-get -y update && apt-get -y dist-upgrade && apt-get -y autoremove && apt-get clean
    RUN apt-get -y install nmap
    CMD ["/bin/bash"]

#### 2. Build Image

```sudo docker build -t nmap -f Dockerfile .```

Vérification de la création de l'image : ```sudo docker image ls```

    REPOSITORY               TAG       IMAGE ID       CREATED          SIZE
    <none>                   <none>    14f7a4289e50   4 minutes ago    114MB
    pentest_img              latest    e9c44ba94204   14 minutes ago   1.02GB
    <none>                   <none>    d6a75ea21da0   14 minutes ago   1.02GB
    <none>                   <none>    142d08b79bec   19 minutes ago   168MB
    kalilinux/kali-rolling   latest    d4bd98a89b78   5 days ago       126MB
    debian                   buster    9e1a64aca99c   11 days ago      114MB
#### 3. Run Container

```sudo docker run --name nmap_cont --rm -i -t nmap bash```

Vérification de la création de l'image : ```sudo docker container ls```

    CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS     NAMES
    a49cd245b80d   14f7a4289e50   "/bin/sh -c 'apt-get…"   5 minutes ago   Up 5 minutes             dreamy_mendeleev    

La commande final "bash" permet d'ouvrir un shell root du container.

#### 4. Save Container 

```sudo docker ps```
```sudo docker commit -p <id_container> <backup_name>```
```sudo docker save -o ~/<backup_name>.tar <backup_name>```

#### 5. Restore Container

```sudo docker load -i ~/<backup_name>.tar```
## Ports en écoute sur la machine

```sudo netstat -tulpn | grep LISTEN```



