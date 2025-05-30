[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## :one: Project presentation
Sur ce repo je vous partage la mise en place de mon nouveau serveur nas.  
Actuellement possesseur d'un Synology DS220+, je souhaite upgrade vers un nouveau système qui m'offre plus de possibilité.  
Il était prévu que je migre vers un Synology DS1621+, mais les récentes nouvelles concernant Synology m'ont confortées dans mon choix qu'il était temps de passer sur ma propre solution.  

Voici mes principaux objectifs à mettre en place :
- Un volume partagé sur le lan
- Un volume propre au vm/container
- Un volume pour les téléchargements
- Un volume dédié à la vidéo-surveillance
- ...


J'ai quelques contraintes à respecter, notamment qu'il faut un boitier rackable, une configuration plutôt économique en énergie mais qui puisse m'offrir suffisamment de performance pour héberger tout mes services en cours et à venir.  


## :two: Hardware
- Rackable case 4U
- Hotswap hdd rack
- Cpu 6c/12t
- Ram 32go minimum
- Motherboard ATX, besoin d'un slot 16x et un slot 4x
- Sata expansion card 10x sata
- Ethernet network card 2x10Gb SFP+
- Psu atx 700W Gold ou Platinum
- Storage os : 500go nvme
- Storage vm/container : 2x2to ssd 2.5" en raid 1
- Storage cache ssd : 2x1to nvme
- Storage data : 6x10to hdd en raid 6
- Storage cctv : 2x4to hdd en raid 1


## :three: Operating system
Contrairement à un autre de mes serveurs qui exploite OpenMediaVault en bare metal, je souhaite ici le virtualiser.  
J'ai donc choisi Proxmox VE 8.4 comme os.  
https://www.proxmox.com/en/


## :four: Virtual machine
- OpenMediaVault 7 (Pour mon os de nas)  
  https://www.openmediavault.org/
- Debian 12 xfce (Pour une vm de sécurité, accès ssh au différent serveurs, ..)  
  https://www.debian.org/index.fr.html


## :five: Container and services
Je liste ici sans explication particulière tout les outils à déployer.
- OpenVpn https://openvpn.net/
- ddclient https://github.com/ddclient/ddclient
- swag (include Certbot & fail2ban) https://github.com/linuxserver/docker-swag
- authelia https://github.com/authelia/authelia
- dashy https://github.com/Lissy93/dashy
- glance https://github.com/glanceapp/glance
- uptime-kuma https://github.com/louislam/uptime-kuma
- portainer https://github.com/portainer/portainer
- librespeed https://github.com/librespeed/speedtest
- nextcloud https://nextcloud.com/fr/
- file-browser https://github.com/filebrowser/filebrowser
- guacamole https://guacamole.apache.org/
- moodle https://moodle.org/
- crowdsec https://github.com/crowdsecurity/crowdsec
- ~gitlab https://about.gitlab.com/~
- forgejo https://forgejo.org/
- keepassXC https://keepassxc.org/
- home-assistant https://www.home-assistant.io/
- ~jdownloader https://github.com/jlesage/docker-jdownloader-2~
- ~deluge https://github.com/linuxserver/docker-deluge~
- pyload https://github.com/pyload/pyload
- frigate https://github.com/blakeblackshear/frigate
- headscale https://headscale.net/stable/
- joomla https://github.com/joomla/joomla-cms
- mastodon https://github.com/mastodon/mastodon
- nut https://github.com/networkupstools/nut
- grafana https://github.com/grafana/grafana
- telegraf https://github.com/influxdata/telegraf
- mealie https://github.com/mealie-recipes/mealie
- immich https://github.com/immich-app/immich?tab=readme-ov-file
- komga https://github.com/gotson/komga
- code-server https://github.com/coder/code-server
- WatchYourLan https://github.com/aceberg/WatchYourLAN
- ...


## :six: Features
- Partage réseau CIFS et NFS
  - Dépôt téléchargements
  - Répertoire de travail
  - Répertoire d'échanges avec les autres serveurs
  - Répertoire vidéo-surveillance
  - Archivage photo/vidéo (synchro smartphone)
- Carte sata en passthrough sur la vm OpenMediaVault
- Partition principal du raid 6 en XFS ou ZFS
- Cache ssd SLOG et L2ARC
- ...


## :seven: Progress
- [ ] Rassemblement des composants hardware
  - [x] case
  - [ ] hdd rack
  - [x] cpu
  - [ ] ram
  - [ ] motherboard
  - [x] sata expansion card
  - [x] ethernet network card
  - [ ] psu
  - [ ] storage
- [ ] Montage hardware du serveur
- [ ] Installation de Proxmox
- [ ] Déploiement de la vm OpenMediaVault



<sub><sup>
T3NlciBlbnRyZXByZW5kcmUgZXN0IGxlIGTDqWJ1dCBkJ3VuZSB2aWUgc3VyIG1lc3VyZS4KQW50b2luZSBDb3JiaW4=
</sup></sub>
