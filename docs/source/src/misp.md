# ![](img/misp.png) Misp Description
## Misp Vagrant
### 1 - Création d'un user _misp_

```misp$ sudo adduser misp```  

Suivre les instructions de création d'un nouveau user.  
Sur sa machine, se connecter au user _misp_ :   
```misp$ su - misp```  
```misp$ mot de passe : "votre mot de passe"```  

### 2 - Cloner et installer MISP

Aller sur [MISP](https://github.com/MISP/MISP) :  
```misp$ git clone https://github.com/MISP/MISP.git```  
```misp$ cd MISP/```  
Installation des submodules :  
```misp$ git submodule init```  
```misp$ git submodule update```  

### 3 - Installer MISP Vagrant

Installation de VirtualBow et vagrant :  
```misp$ sudo apt-get install virtualbox vagrant```  
    Si l'installation de VirtualBox est en échec, redirigez-vous vers [VirtualBox](https://www.virtualbox.org/wiki/Downloads).  

* Déploiement de MISP Vagrant  
    

* Installation de MISP Vagrant sans l'environement de développement  

Aller sur [MISP Vagrant](https://github.com/MISP/misp-vagrant) :  
```misp$ git clone https://github.com/MISP/misp-vagrant.git```  
```misp$cd misp-vagrant/```  
```misp$ export MISP_ENV='demo'```  
```misp$ vagrant up```  

## Sources

- [MISP](https://www.misp-project.org/features.html)  
- [MISP Vagrant](https://github.com/MISP/misp-vagrant)  


