# Borealis-Linux-Lab - Administration & Sécurisation Linux

### Alexandre KIEFER

**Administrateur Systèmes, Réseaux & Cybersécurité**  
📍 Savigny-sur-Orge, Île-de-France  
🔗 [LinkedIn](https://www.linkedin.com/in/alexandre-kiefer-847334282/) | 🐙 [GitHub](https://github.com/kieferalexandre1-creator) | ✉️ kiefer.alexandre1@gmail.com

[![Statut](https://img.shields.io/badge/Statut-En%20préparation-orange)](#)
[![Environnement](https://img.shields.io/badge/Environnement-Debian%2012-blue)](#)




> [!NOTE]
> ### 🌌 BOREALIS · LINUX LAB
>
> Projet personnel consacré à l'administration, la sécurisation et
> l'automatisation d'un environnement Linux.
>
> **Administration Linux · Hardening · Bash · Docker · Ansible**

---

## 🧭 Navigation

[🎯 Objectifs](#-objectifs) •
[🏗️ Architecture](#️-architecture) •
[🐧 Administration Linux](#-administration-linux) •
[🛡️ Hardening](#️-hardening) •
[⚙️ Automatisation](#️-automatisation) •
[🐳 Conteneurisation](#-conteneurisation) •
[🧪 Tests](#-tests) •
[📚 Documentation](#-documentation)


## Objectifs

Après Aegis Infra Lab, consacré à la mise en place d'une infrastructure d'entreprise virtualisée, Borealis Linux Lab se concentre sur l'administration et la sécurisation des systèmes Linux.
L'objectif de ce laboratoire est de construire progressivement un environnement Linux permettant de développer et de mettre en pratique mes compétences autour de plusieurs axes :

- 🐧 Administration Linux — gestion des utilisateurs, permissions, services, processus et stockage
- 🌐 Administration réseau — configuration réseau, services et accès distants
- 🛡️ Hardening — sécurisation du système et réduction de la surface d'attaque
- 💻 Bash — scripting et automatisation de tâches d'administration
- ⚙️ Ansible — automatisation et standardisation des configurations
- 🐳 Docker — déploiement et administration de services conteneurisés
- 🧪 Tests & validation — contrôle du fonctionnement et de la sécurité des configurations mises en place
  
Borealis est construit comme un laboratoire d'apprentissage pratique : chaque étape sera documentée avec les configurations réalisées, les commandes utilisées, les problèmes rencontrés et les solutions mises en œuvre.


## Architecture du laboratoire

Borealis est conçu comme un laboratoire Linux composé de plusieurs machines Debian ayant chacune un rôle précis.

Contrairement à **Aegis Infra Lab**, qui reproduisait l'infrastructure globale d'une petite entreprise, Borealis se concentre sur l'administration Linux. L'environnement est volontairement séparé en plusieurs serveurs afin de travailler les communications entre machines, l'administration distante, la sécurisation et l'automatisation.

### 🖥️ Infrastructure cible

| Machine | Système | Rôle principal | Statut |
|---|---|---|---|
| `SRV-BOREALIS-01` | Debian 12 | Serveur Linux principal | 🔜 Prévu |
| `SRV-BOREALIS-02` | Debian 12 | Services & conteneurs | 🔜 Prévu |
| `SRV-BOREALIS-CTL` | Debian 12 | Administration & automatisation | 🔜 Prévu |

> Les rôles et ressources pourront évoluer au cours du projet en fonction des besoins rencontrés pendant la construction du laboratoire.

---

### 🔹 SRV-BOREALIS-01

**Serveur Linux principal**

Cette machine servira de base pour travailler l'administration quotidienne d'un serveur Debian.

Objectifs prévus :

- gestion des utilisateurs et groupes
- permissions et propriété des fichiers
- administration des services avec `systemd`
- gestion des paquets
- stockage et système de fichiers
- configuration réseau
- administration distante avec SSH
- analyse des journaux système
- sécurisation progressive du serveur

---

### 🔹 SRV-BOREALIS-02

**Serveur de services & conteneurisation**

Cette machine sera utilisée pour déployer et administrer différents services Linux.

Objectifs prévus :

- installation et configuration de services
- déploiement de Docker
- création et gestion de conteneurs
- gestion des volumes
- configuration des réseaux Docker
- exposition et sécurisation des services
- tests de communication entre les différents serveurs

---

### 🔹 SRV-BOREALIS-CTL

**Serveur d'administration & automatisation**

Cette machine aura pour objectif de centraliser l'administration des autres serveurs du laboratoire.

Objectifs prévus :

- administration distante via SSH
- authentification par clés SSH
- scripts Bash d'administration
- installation d'Ansible
- inventaire des machines
- création de playbooks
- automatisation des configurations
- déploiement de configurations reproductibles

---

### 🌐 Réseau

Les différentes machines seront connectées à un réseau virtuel dédié au laboratoire.

<img width="1672" height="941" alt="image" src="https://github.com/user-attachments/assets/6e91e552-ddd4-44a0-8e07-b15eaa77f5e7" />

## 📋 03 — Planification du projet

Avant le déploiement des machines virtuelles, le laboratoire Borealis est organisé
en plusieurs phases afin de construire progressivement l'environnement et de
documenter chaque étape.

### 🗺️ Feuille de route

| Phase | Objectif | État |
|---|---|---|
| **01 — Conception** | Définition des objectifs et de l'architecture | ✅ Terminé |
| **02 — Déploiement** | Création et configuration initiale des VM Debian | ⏳ À venir |
| **03 — Administration** | Utilisateurs, permissions, services, stockage et réseau | ⏳ À venir |
| **04 — Accès distant** | Configuration et sécurisation de SSH | ⏳ À venir |
| **05 — Hardening** | Durcissement et réduction de la surface d'attaque | ⏳ À venir |
| **06 — Scripting** | Automatisation de tâches avec Bash | ⏳ À venir |
| **07 — Ansible** | Administration et configuration automatisées | ⏳ À venir |
| **08 — Docker** | Déploiement et sécurisation de services conteneurisés | ⏳ À venir |
| **09 — Validation** | Tests fonctionnels et contrôles de sécurité | ⏳ À venir |
| **10 — Documentation** | Finalisation des procédures et bilan du laboratoire | ⏳ À venir |

---

### 🖥️ Machines prévues

| Hôte | Fonction | Système |
|---|---|---|
| `SRV-BOREALIS-CTL` | Administration & automatisation | Debian 12 |
| `SRV-BOREALIS-01` | Administration & hardening | Debian 12 |
| `SRV-BOREALIS-02` | Services & conteneurisation | Debian 12 |

Les ressources matérielles et l'adressage IP seront définis lors du déploiement
des machines virtuelles.

---

### 🧰 Technologies envisagées

![Debian](https://img.shields.io/badge/Debian%2012-A81D33?logo=debian&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-121011?logo=gnubash&logoColor=white)
![SSH](https://img.shields.io/badge/SSH-Administration%20distante-2496ED)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?logo=virtualbox&logoColor=white)

> [!IMPORTANT]
> Les technologies présentées dans cette section correspondent aux outils
> envisagés pour le laboratoire. Le README sera mis à jour progressivement
> afin de refléter uniquement les éléments réellement déployés et testés.


## Chapitre 1 — Déploiement de BOREALIS-SRV01

## 1.1 Mise en place de la machine virtuelle

La première étape du projet Borealis Linux Lab consiste à mettre en place le serveur Linux principal de l'infrastructure.

Une machine virtuelle sous Debian GNU/Linux 13 (Trixie) est utilisée comme base du serveur. Elle est renommée afin de respecter une convention de nommage claire et de pouvoir facilement identifier son rôle au sein du laboratoire.

Configuration de la VM

| Paramètre | Configuration |
|---|---|
| Nom de la VM | `BOREALIS-SRV01` |
| Hostname | `borealis-srv01` |
| Système d'exploitation | Debian GNU/Linux 13 (Trixie) |
| Architecture | x86_64 |
| Réseau | `192.168.56.0/24` |
| Adresse IPv4 | `192.168.56.30` |
| Rôle | Serveur Linux principal |

La machine existait déjà dans l'environnement de virtualisation, mais elle ne contenait que la configuration de base de Debian. Elle a donc été réutilisée et reconfigurée pour le projet Borealis, plutôt que de procéder à une nouvelle installation complète.

## 1.2 Configuration du nom du serveur
*borealis-srv01*

Le hostname est configuré avec :
*hostnamectl set-hostname borealis-srv01*

La modification est ensuite vérifiée :
*hostnamectl*

L'utilisation de la convention borealis-srvXX permet de conserver une organisation cohérente lorsque plusieurs serveurs seront intégrés à l'infrastructure.
Le second serveur pourra ainsi être identifié comme :
*borealis-srv02*

## 1.3 Configuration de l'adressage réseau
Le laboratoire Borealis utilise le réseau privé :
*192.168.56.0/24*

Une adresse IP dédiée est attribuée au premier serveur :
*192.168.56.30*

Cette adresse permet d'identifier de manière stable BOREALIS-SRV01 sur le réseau du laboratoire.
L'adressage du projet est organisé de manière à pouvoir intégrer progressivement d'autres machines :

| Machine | Adresse IP |
|---|---|
| `BOREALIS-SRV01` | `192.168.56.30` |
| `BOREALIS-SRV02` | `192.168.56.31` |

La configuration peut être contrôlée avec :
*ip addr*

ou :
*hostname -I*

## 1.4 Mise à jour du système

Avant le déploiement des différents services, les dépôts et les paquets du serveur sont mis à jour :
*apt update*
*apt upgrade -y*

Cette étape permet de partir sur un système à jour avant de commencer les opérations d'administration et de sécurisation.

## 1.5 Vérification de l'environnement

La version du système peut être contrôlée avec :
*cat /etc/os-release*

Le serveur utilisé pour le projet fonctionne sous :
Debian GNU/Linux 13 (Trixie)

Le nom de la machine est vérifié avec :
*hostname*

Résultat attendu :
*borealis-srv01*

La configuration réseau est ensuite vérifiée :
*hostname -I*

Résultat attendu :
*192.168.56.30*

À l'issue de cette première étape, BOREALIS-SRV01 est opérationnel et intégré au réseau du laboratoire. Il constitue désormais le serveur Linux principal sur lequel seront progressivement déployées les différentes fonctions d'administration et de sécurisation.

## Chapitre 2 — Gestion des utilisateurs, groupes et permissions

## 2.1 Objectif

Afin de reproduire le fonctionnement d'une infrastructure professionnelle, les accès aux ressources du serveur sont séparés selon les rôles des utilisateurs.
Trois groupes sont mis en place :

| Groupe | Fonction |
|---|---|
| `borealis-admin` | Administration du serveur |
| `borealis-dev` | Ressources de développement |
| `borealis-web` | Ressources Web |

Ils sont créés avec :

*groupadd borealis-admin*
*groupadd borealis-dev*
*groupadd borealis-web*

Leur présence est vérifiée avec :

*getent group borealis-admin borealis-dev borealis-web*

## 2.2 Création des utilisateurs

Le compte alex est utilisé comme compte d'administration et rejoint le groupe :

*usermod -aG borealis-admin alex*

Deux utilisateurs sont également créés afin de représenter différents profils au sein de l'entreprise :

*useradd -m -s /bin/bash dev01*
*useradd -m -s /bin/bash web01*

Ils sont ensuite associés à leurs groupes respectifs :

*usermod -aG borealis-dev dev01*
*usermod -aG borealis-web web01*

Cette séparation permettra de tester par la suite que chaque utilisateur dispose uniquement des ressources nécessaires à son rôle.

## 2.3 Organisation des données

Une arborescence dédiée est créée dans /srv :

/srv/borealis/
├── backup/
├── dev/
├── shared/
└── web/

Les répertoires sont créés avec :
*mkdir -p /srv/borealis/{shared,dev,web,backup}*

Chaque espace possède une fonction distincte :

| Répertoire | Fonction |
|---|---|
| `dev/` | Données accessibles à l'équipe de développement |
| `web/` | Ressources liées aux services Web |
| `backup/` | Sauvegardes réservées à l'administration |
| `shared/` | Espace destiné aux ressources communes |

## 2.4 Attribution des droits

Les différents répertoires sont associés aux groupes appropriés :

**chown root:borealis-dev /srv/borealis/dev
chown root:borealis-web /srv/borealis/web
chown root:borealis-admin /srv/borealis/backup**

Les permissions sont ensuite appliquées :
**chmod 2770 /srv/borealis/dev
chmod 2770 /srv/borealis/web
chmod 2770 /srv/borealis/backup
chmod 2775 /srv/borealis/shared**

Le bit SetGID est utilisé sur ces répertoires. Il permet aux nouveaux fichiers et sous-répertoires de conserver automatiquement le groupe associé au répertoire parent.
La configuration est contrôlée avec :

ls -ld /srv/borealis/*



