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

## 3. Validation du contrôle d'accès

Après avoir structuré les comptes, groupes et espaces de travail de BOREALIS-SRV01, j'ai réalisé une série de tests afin de vérifier que les permissions mises en place correspondent réellement aux rôles définis.

L'objectif n'est pas uniquement de configurer des droits Linux, mais de vérifier qu'un utilisateur ne peut pas accéder ou modifier une ressource qui ne lui est pas destinée.
Cette approche s'inscrit dans le principe du moindre privilège : chaque utilisateur dispose uniquement des autorisations nécessaires à son activité.

## 3.1 Stratégie de validation

Deux profils représentatifs ont été utilisés pour les tests :

| Compte | Groupe | Ressource autorisée |
|---|---|---|
| `dev01` | `borealis-dev` | `/srv/borealis/dev` |
| `web01` | `borealis-web` | `/srv/borealis/web` |

Le répertoire :
/srv/borealis/backup

est quant à lui réservé au groupe d'administration.
Pour valider le cloisonnement, les tests sont réalisés dans deux situations :
Accès légitime : l'utilisateur tente d'écrire dans son propre espace.
Accès non autorisé : le même utilisateur tente d'écrire dans un espace appartenant à un autre groupe.
Un contrôle d'accès n'est considéré comme fonctionnel que si ces deux comportements sont correctement appliqués.

## 3.2 Validation des droits du profil développement

Je commence par ouvrir une session avec le compte dev01 :
su - dev01

Ce compte appartient au groupe :
borealis-dev

Il doit donc être capable de travailler dans :
/srv/borealis/dev

Un fichier de test est créé :
touch /srv/borealis/dev/test-dev.txt

Puis les propriétés du fichier sont contrôlées :
ls -l /srv/borealis/dev/

Le résultat obtenu est :
-rw-rw-r-- 1 dev01 borealis-dev ... test-dev.txt

Deux éléments sont ainsi validés.

Premièrement, dev01 possède bien les droits d'écriture nécessaires dans l'espace réservé au développement.
Deuxièmement, le fichier créé appartient automatiquement au groupe borealis-dev.

Ce comportement provient du bit SetGID configuré précédemment sur le répertoire. Il permet de conserver automatiquement le groupe du répertoire parent pour les nouveaux fichiers, ce qui facilite la gestion d'espaces de travail collaboratifs.

Test d'isolation
Je tente ensuite volontairement de créer un fichier dans l'espace réservé au profil Web :
touch /srv/borealis/web/interdit.txt

<img width="590" height="106" alt="Capture d&#39;écran 2026-10-05 235432" src="https://github.com/user-attachments/assets/6e3b6136-6dfa-465c-a6b5-bda764f6c815" />

Le système retourne :

Permission non accordée

Le contrôle d'accès fonctionne donc dans les deux sens : dev01 peut travailler dans son espace, mais ne peut pas modifier celui d'une autre équipe.
Preuve de validation

## 3.3 Protection des sauvegardes

Les sauvegardes constituent une ressource plus sensible que les espaces de travail standards.
Le répertoire :
/srv/borealis/backup

a donc été réservé au groupe d'administration borealis-admin.
Pour vérifier cette restriction, une tentative d'écriture est effectuée depuis le compte dev01 :
touch /srv/borealis/backup/interdit.txt

Le système bloque l'opération :
Permission non accordée

Cette vérification confirme qu'un compte disposant d'un accès au serveur ne bénéficie pas automatiquement d'un accès aux sauvegardes.
Cela limite notamment le risque de modification ou de suppression accidentelle de données par un utilisateur ne disposant pas du rôle approprié.
Preuve de validation

<img width="608" height="29" alt="Capture d&#39;écran 2026-10-05 235510" src="https://github.com/user-attachments/assets/e32b8217-f023-45cd-acce-35e2d5fa10cc" />


## 3.4 Validation des droits du profil Web
Le même principe est appliqué au compte web01.
Une session est ouverte :
su - web01

Ce compte appartient au groupe :
borealis-web

Il doit pouvoir travailler dans :
/srv/borealis/web

Je vérifie son droit d'écriture en créant un fichier :
touch /srv/borealis/web/test-web.txt

L'opération est réalisée avec succès.
Je tente ensuite volontairement d'écrire dans l'espace réservé au développement :
touch /srv/borealis/dev/interdit.txt

Le serveur refuse l'opération :
Permission non accordée

<img width="578" height="75" alt="Capture d&#39;écran 2026-10-05 235612" src="https://github.com/user-attachments/assets/9aef415f-a030-40c2-a6d8-bc5ef021f17a" />

Cette seconde vérification confirme que le cloisonnement n'est pas spécifique à dev01 : les restrictions définies au niveau des groupes sont correctement appliquées aux différents profils.
Preuve de validation

## 3.5 Résultat du contrôle d'accès

Les tests permettent de synthétiser les droits de la manière suivante :

| Profil | Développement | Web | Sauvegardes |
|---|:---:|:---:|:---:|
| `dev01` | ✅ Lecture/écriture | ❌ Refusé | ❌ Refusé |
| `web01` | ❌ Refusé | ✅ Lecture/écriture | ❌ Refusé |
| Administration | Selon privilèges | Selon privilèges | ✅ Autorisé |

## 3.6 Bilan

Cette phase m'a permis de mettre en pratique et surtout de valider concrètement un modèle de contrôle d'accès Linux.
La configuration repose sur plusieurs mécanismes complémentaires :
- comptes utilisateurs distincts ;
- groupes associés aux fonctions ;
- propriétaires et groupes des fichiers ;
- permissions Unix ;
- héritage de groupe avec SetGID ;
- séparation des ressources ;
- principe du moindre privilège.
Les tests positifs et négatifs montrent que les restrictions ne sont pas uniquement définies dans la configuration : elles sont effectivement appliquées par le système.
Compétences mises en pratique : administration des utilisateurs et groupes Linux, gestion des permissions, chmod, chown, SetGID, contrôle d'accès, cloisonnement des ressources et validation du principe du moindre privilège.

## 4. Sécurisation de l'administration SSH

Une fois les permissions locales validées, je me suis concentré sur un autre point sensible de l'infrastructure : l'administration distante du serveur.
BOREALIS-SRV01 est administré depuis un poste Windows à l'aide du protocole SSH.
SSH chiffre les communications, mais son simple déploiement ne suffit pas à sécuriser correctement un serveur. Une configuration trop permissive peut notamment autoriser l'utilisation directe de comptes privilégiés ou dépendre uniquement de mots de passe.
J'ai donc choisi de durcir progressivement la configuration OpenSSH sans interrompre l'accès d'administration au serveur.

## 4.1 Situation initiale

Le service OpenSSH était déjà installé et opérationnel sur la machine.
L'administration s'effectuait initialement depuis le poste Windows avec le compte Linux alex :
ssh alex@192.168.56.22

L'utilisateur saisissait ensuite son mot de passe Linux pour ouvrir la session.
Cette méthode fonctionne, mais elle repose sur un secret que l'utilisateur doit connaître et transmettre au serveur lors de l'authentification.
L'objectif est donc de faire évoluer cette architecture vers :
Poste administrateur Windows
          │
          │ SSH
          │ authentification ED25519
          ▼
    BOREALIS-SRV01
          │
          └── compte alex

La clé privée restera exclusivement sur le poste administrateur tandis que le serveur conservera uniquement la clé publique autorisée.

## 4.2 Mesures de durcissement retenues

Plusieurs mesures sont appliquées progressivement

| Mesure | Objectif |
|---|---|
| Interdiction du login SSH `root` | Éviter l'utilisation distante directe du compte le plus privilégié |
| `MaxAuthTries 3` | Réduire le nombre de tentatives d'authentification par connexion |
| Authentification par clé publique | Remplacer progressivement l'utilisation du mot de passe |
| Clé ED25519 | Utiliser un algorithme moderne adapté à l'authentification SSH |
| Compte nominatif `alex` | Conserver un compte identifiable pour l'administration |
| Désactivation future du mot de passe SSH | Imposer l'authentification par clé une fois celle-ci validée |

## 4.3 Sauvegarde de la configuration OpenSSH
Avant toute modification, je sauvegarde la configuration existante :
cp /etc/ssh/sshd_config /etc/ssh/sshd_config.bak

La présence de la sauvegarde est vérifiée :
ls -l /etc/ssh/sshd_config*

Cette étape permet de disposer d'un point de retour rapide en cas d'erreur lors du durcissement.

## 4.4 Durcissement de sshd
La configuration du serveur OpenSSH est modifiée dans :
nano /etc/ssh/sshd_config

Trois paramètres sont dans un premier temps explicitement définis :
PermitRootLogin no
MaxAuthTries 3
PubkeyAuthentication yes

PermitRootLogin no
Cette directive interdit l'ouverture directe d'une session SSH avec le compte root.
L'administration distante doit être effectuée avec un compte nominatif, ici alex, puis les privilèges nécessaires sont obtenus avec sudo.
Cette séparation permet notamment d'éviter d'utiliser systématiquement le compte disposant du niveau de privilège maximal.
MaxAuthTries 3
Le nombre maximal de tentatives d'authentification pour une connexion est réduit à trois :
MaxAuthTries 3

La valeur par défaut observée dans la configuration était de six.
Cette modification réduit la marge disponible pour multiplier les essais d'authentification au sein d'une même connexion.
Elle sera complétée plus tard dans le projet par une protection contre les tentatives répétées.
PubkeyAuthentication yes
L'authentification par clé publique est explicitement autorisée :
PubkeyAuthentication yes

Elle permettra au poste administrateur de prouver son identité à l'aide d'une clé privée sans avoir à utiliser le mot de passe Linux pour chaque connexion.
Preuve de configuration

<img width="198" height="113" alt="Capture d&#39;écran 2026-10-06 001137" src="https://github.com/user-attachments/assets/6fd875af-a8f7-4655-9038-ac54591068df" />


## 4.5 Validation avant application

Une erreur dans sshd_config peut empêcher le service SSH de fonctionner correctement.
Avant de recharger OpenSSH, je vérifie donc systématiquement la syntaxe :
sshd -t

Aucun message n'étant retourné, la configuration est considérée comme syntaxiquement valide.
Le service est ensuite rechargé :
systemctl reload ssh

J'utilise ensuite sshd -T afin de contrôler la configuration réellement interprétée par OpenSSH, plutôt que de me limiter au contenu du fichier :
sshd -T | grep -E 'permitrootlogin|pubkeyauthentication|maxauthtries'

Le résultat obtenu est :
maxauthtries 3
permitrootlogin no
pubkeyauthentication yes

Les trois mesures de durcissement sont donc effectivement prises en compte par le serveur.
Preuve de validation

<img width="198" height="113" alt="Capture d&#39;écran 2026-10-06 001137" src="https://github.com/user-attachments/assets/38d20726-f5a8-4722-9110-d97d9692e270" />

Cette capture est particulièrement utile dans le portfolio : elle montre à la fois la validation syntaxique, le rechargement du service et le contrôle de la configuration réellement appliquée.

## 4.6 Mise en place de l'authentification par clé

L'étape suivante consiste à remplacer progressivement l'authentification par mot de passe par une authentification cryptographique.
La paire de clés est générée sur le poste Windows administrateur, et non sur le serveur.
Depuis PowerShell :
ssh-keygen -t ed25519 -C "alex@borealis"

Deux fichiers sont générés :

| Élément | Rôle | Conservation |
|---|---|---|
| `id_ed25519` | Clé privée permettant de prouver l'identité du poste | Poste Windows uniquement |
| `id_ed25519.pub` | Clé publique permettant au serveur de reconnaître le poste | Serveur Debian |

La clé privée n'a pas vocation à être copiée sur BOREALIS-SRV01 ou publiée dans le dépôt GitHub.
Preuve de génération : 

## 4.7 Autorisation de la clé sur le serveur
La clé publique du poste administrateur est ajoutée au fichier :
/home/alex/.ssh/authorized_keys

OpenSSH impose des permissions suffisamment restrictives sur ces éléments.
Le répertoire .ssh est configuré en :
chmod 700 /home/alex/.ssh

et le fichier contenant les clés autorisées en :
chmod 600 /home/alex/.ssh/authorized_keys

La configuration est contrôlée avec :
ls -la /home/alex/.ssh

Le fichier authorized_keys appartient au compte alex et n'est modifiable que par son propriétaire.
Preuve de configuration 

