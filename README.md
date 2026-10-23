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

Voici la suite de ton README GitHub pour Borealis Linux Lab, en reprenant à partir de la section 4.7.

Je garde un style naturel, à la première personne, comme si tu expliquais toi-même les manipulations réalisées et leur intérêt. Les commandes sont accompagnées d'explications courtes, sans captures d'écran obligatoires.

Les étapes 4.7 et 4.8 correspondent aux tests que tu m'as confirmés. Pour les étapes suivantes, conserve uniquement les résultats que tu as réellement vérifiés.

## 4.7 — Autorisation de la clé SSH sur le serveur

Après avoir généré ma paire de clés SSH, j'ai configuré mon serveur Debian pour qu'il accepte ma clé publique.

L'objectif est de pouvoir me connecter à distance de manière plus sécurisée, sans utiliser systématiquement le mot de passe de mon compte Linux.

J'ai commencé par créer le répertoire `.ssh` dans le dossier personnel de mon utilisateur :

```
mkdir -p ~/.ssh
chmod 700 ~/.ssh
```

J'ai ensuite ouvert le fichier `authorized_keys` pour y ajouter ma clé publique :

```
nano ~/.ssh/authorized_keys
```

Ce fichier permet au serveur de connaître les clés publiques autorisées à se connecter au compte.

Une fois ma clé ajoutée, j'ai appliqué les permissions nécessaires :

```
chmod 600 ~/.ssh/authorized_keys
```

Ces permissions sont importantes : elles empêchent les autres utilisateurs du système de modifier les clés autorisées.

## 4.8 — Test de connexion SSH par clé

Une fois la clé publique enregistrée sur le serveur, j'ai effectué un test depuis mon poste client.

```
ssh -i ~/.ssh/id_ed25519 utilisateur@IP_DU_SERVEUR
```

J'ai réussi à établir une connexion SSH en utilisant ma clé privée, sans saisir le mot de passe de mon compte Debian.

Ce test m'a permis de confirmer que l'authentification par clé fonctionnait correctement.

## 4.9 — Renforcement de la configuration SSH

Après avoir validé l'authentification par clé, l'étape suivante consiste à désactiver les connexions SSH par mot de passe.

J'ai choisi cette approche pour réduire les risques liés aux tentatives de connexion par force brute et empêcher les connexions SSH directes au compte root.

J'ai ouvert le fichier de configuration :

```
sudo nano /etc/ssh/sshd_config
```

Les paramètres à appliquer sont les suivants :

```
PubkeyAuthentication yes
PasswordAuthentication no
KbdInteractiveAuthentication no
PermitRootLogin no
```

J'ai également prévu de vérifier les éventuels fichiers de configuration supplémentaires :

```
sudo grep -RniE 'PasswordAuthentication|KbdInteractiveAuthentication|PermitRootLogin|PubkeyAuthentication' /etc/ssh/sshd_config.d/
```

Avant de recharger le service, je vérifie la syntaxe et les paramètres réellement appliqués :

```
sudo sshd -t
sudo sshd -T | grep -E 'pubkeyauthentication|passwordauthentication|kbdinteractiveauthentication|permitrootlogin'
```

Si la configuration est correcte, je peux recharger SSH :

```
sudo systemctl reload ssh
```

Je conserve ma session actuelle ouverte pendant les tests, afin de ne pas perdre l'accès au serveur en cas d'erreur.

## 4.10 — Installation et configuration du pare-feu UFW

Pour compléter la sécurisation de mon serveur, j'ai choisi d'utiliser UFW, un outil qui simplifie la gestion des règles de pare-feu sous Linux.

Mon objectif est de bloquer les connexions entrantes qui ne sont pas nécessaires, tout en conservant l'accès SSH depuis mon poste d'administration.

J'ai commencé par installer UFW :

```
sudo apt update
sudo apt install ufw -y
```

Avant d'activer le pare-feu, je vérifie le port utilisé par SSH :

```
sudo sshd -T | grep '^port '
```

Si SSH utilise le port 22, je l'autorise avec la commande suivante :

```
sudo ufw allow 22/tcp
```

J'applique ensuite les règles par défaut :

```
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

Cela signifie que les nouvelles connexions entrantes sont refusées par défaut, sauf lorsqu'une règle les autorise explicitement.

Après avoir vérifié la présence de ma règle SSH :

```
sudo ufw show added
```

Je peux activer le pare-feu :

```
sudo ufw enable
```

Enfin, je contrôle son état :

```
sudo ufw status verbose
```

Cette configuration permet de limiter l'exposition réseau du serveur et de mieux maîtriser les services accessibles.

## 4.11 — Restriction de l'accès SSH au réseau d'administration

Après avoir mis en place UFW, je souhaite limiter l'accès SSH aux machines de mon réseau d'administration.

Même avec une authentification par clé, il est préférable de ne pas exposer inutilement le service SSH à toutes les machines du réseau.

Pour commencer, j'identifie les interfaces et les adresses IPv4 de mon serveur :

```
ip -4 addr
```

Je dois ensuite identifier le sous-réseau depuis lequel mon poste client se connecte.

Par exemple, si mon réseau d'administration est `192.168.1.0/24`, je peux ajouter la règle suivante :

```
sudo ufw allow from 192.168.1.0/24 to any port 22 proto tcp
```

Cette adresse est uniquement un exemple : je dois utiliser le véritable sous-réseau de mon laboratoire.

Avant de supprimer la règle SSH qui autorise toutes les adresses, je teste une nouvelle connexion depuis mon poste client.

Je peux ensuite afficher les règles existantes :

```
sudo ufw status numbered
```

Puis supprimer la règle générale devenue inutile, en utilisant son numéro réel :

```
sudo ufw delete NUMERO_DE_LA_REGLE
```

L'intérêt de cette configuration est d'appliquer le principe du moindre privilège au niveau réseau : seules les machines ayant réellement besoin d'administrer le serveur doivent pouvoir accéder au service SSH.

## 4.12 — Vérification des ports et services actifs

Pour terminer cette partie consacrée à la sécurisation du serveur, je vérifie les services réseau qui sont actuellement à l'écoute.

J'utilise la commande :

```
sudo ss -tulpen
```

Elle me permet d'identifier les ports TCP et UDP ouverts en écoute ainsi que les processus associés.

Je compare ensuite ces informations aux règles configurées dans UFW :

```
sudo ufw status numbered
```

Cette vérification est utile pour repérer les services qui ne devraient pas être exposés sur le réseau.

Un port en écoute n'est pas forcément accessible depuis l'extérieur : cela dépend notamment de l'interface sur laquelle le service écoute et des règles du pare-feu.

L'objectif est donc de conserver uniquement les services nécessaires au fonctionnement du laboratoire et de limiter autant que possible la surface d'attaque du serveur.

### Bilan de cette partie

Cette phase de Borealis Linux Lab est consacrée à la sécurisation des accès à mon serveur Debian.

Elle m'a permis de travailler sur plusieurs notions importantes en administration Linux : l'authentification SSH par clé, la gestion des permissions, le durcissement du service SSH et le filtrage des connexions réseau.

Au-delà de l'exécution des commandes, l'objectif est de comprendre pourquoi chaque configuration est nécessaire et comment vérifier qu'elle fonctionne correctement.

Pour la suite du projet, je te propose de passer à la section 5 — Supervision et surveillance du serveur Linux, avec notamment l'analyse des journaux système, le suivi des connexions SSH et la mise en place d'outils de surveillance. Cela permettra de compléter la partie sécurisation par une approche de détection et de diagnostic.
Parfait ! On reprend Borealis Linux Lab à l'étape 5, puisque tu as terminé toute la partie 4 consacrée à la sécurisation SSH et au pare-feu UFW.

On va maintenant travailler sur la surveillance et l'analyse des journaux Linux. C'est une bonne suite pour ton portfolio, car elle montre que tu ne te limites pas à installer et sécuriser un serveur : tu sais aussi surveiller son fonctionnement et rechercher des incidents.

Je conserve ton format : des commandes Debian à exécuter, puis des explications naturelles à la première personne, directement utilisables dans ton README GitHub.

# 5. Supervision et analyse des journaux système

## 5.1 — Vérification du service de journalisation

Avant de commencer l'analyse des événements, j'ai voulu comprendre comment Debian enregistre les activités du système.

Linux utilise notamment `systemd-journald`, un service qui centralise les journaux des services et du système. Ces informations sont utiles pour diagnostiquer des erreurs, surveiller les connexions et comprendre ce qui se passe sur le serveur.

J'ai commencé par vérifier l'état du service :

```
sudo systemctl status systemd-journald
```

Le service doit être actif, avec un état similaire à :

```
Active: active (running)
```

J'ai ensuite utilisé `journalctl` pour consulter les événements enregistrés :

```
sudo journalctl -n 30 --no-pager
```

Cette commande affiche les 30 dernières entrées du journal système, sans ouvrir d'interface de pagination.

## 5.2 — Consultation des journaux SSH

Après avoir vérifié la journalisation, je me suis intéressé aux événements liés à SSH.

Comme j'ai précédemment configuré l'authentification par clé et désactivé les connexions par mot de passe, je souhaite maintenant pouvoir identifier les connexions réussies et les éventuelles tentatives refusées.

Pour consulter les événements du service SSH :

```
sudo journalctl -u ssh --since "today" --no-pager
```

Pour rechercher les authentifications réussies :

```
sudo journalctl -u ssh --no-pager | grep "Accepted"
```

Une connexion réussie par clé peut apparaître sous cette forme :

```
Accepted publickey for utilisateur from 192.168.1.10 port 54321 ssh2
```

Ce message permet notamment d'identifier l'utilisateur concerné, l'adresse IP du client et la méthode d'authentification utilisée.

J'ai également prévu de rechercher les événements de refus :

```
sudo journalctl -u ssh --no-pager | grep -Ei "Failed|Invalid|refused|Disconnected"
```

L'absence de résultat ne signifie pas forcément qu'aucune tentative n'a eu lieu : les messages disponibles dépendent de la configuration et de la période de conservation des journaux.

## 5.3 — Surveillance des événements en temps réel

Après avoir consulté les journaux existants, j'ai voulu pouvoir observer les nouveaux événements au moment où ils apparaissent.

Pour cela, j'utilise :

```
sudo journalctl -u ssh -f
```

L'option `-f` permet de suivre les nouveaux événements en temps réel.

Depuis mon poste client, je peux ouvrir une seconde connexion SSH afin d'observer les événements correspondants dans le terminal du serveur.

Cette méthode est particulièrement utile pour vérifier le fonctionnement de l'authentification et faciliter le diagnostic d'un problème de connexion.

Pour arrêter le suivi des journaux, il suffit d'utiliser `Ctrl + C`.

## 5.4 — Vérification de la conservation des journaux

Pour aller un peu plus loin, j'ai souhaité vérifier comment les journaux étaient conservés sur mon serveur Debian.

La conservation des événements est importante : si les journaux disparaissent après un redémarrage, il devient plus difficile d'analyser un incident survenu précédemment.

J'ai commencé par vérifier l'espace utilisé :

```
sudo journalctl --disk-usage
```

Puis j'ai consulté le paramètre de stockage effectif :

```
systemd-analyze cat-config systemd/journald.conf
```

Sur Debian, `journald` peut utiliser un stockage persistant ou volatile selon sa configuration.

Si le stockage persistant n'est pas déjà activé, je peux créer une configuration dédiée :

```
sudo mkdir -p /etc/systemd/journald.conf.d
sudo nano /etc/systemd/journald.conf.d/10-persistent.conf
```

Et y ajouter :

```
[Journal]
Storage=persistent
SystemMaxUse=200M
```

Cette configuration demande à `journald` de conserver les journaux sur disque, avec une limite d'utilisation de 200 Mo pour les journaux persistants.

Pour appliquer la modification :

```
sudo systemctl restart systemd-journald
sudo journalctl --flush
```

Je peux ensuite vérifier la présence du répertoire de stockage :

```
sudo ls -ld /var/log/journal
```

Cette étape permet de conserver un historique des événements, ce qui facilite les recherches en cas d'incident ou de dysfonctionnement.

## 5.5 — Contrôle de l'état du serveur

En complément des journaux, je souhaite disposer de quelques commandes simples pour surveiller l'état général de Debian.

Pour vérifier la durée de fonctionnement et la charge du serveur :

```
uptime
```

Pour consulter l'utilisation de la mémoire :

```
free -h
```

Pour vérifier l'espace disque :

```
df -h
```

Et pour afficher les processus et leur consommation de ressources :

```
top
```

Ces commandes constituent une première base de diagnostic. Elles permettent notamment d'identifier une consommation excessive de mémoire, un disque presque plein ou une charge système inhabituelle.


Oui, on peut continuer avec la partie 6 de Borealis Linux Lab : automatisation de l'administration Linux avec Bash.

Pas besoin de captures d'écran pour toutes les étapes. Pour ton GitHub, je te conseille simplement une capture du résultat final du script. Ce sera une preuve concrète de son fonctionnement auprès des recruteurs.

## 6. Automatisation de l'administration Linux avec Bash

### 6.1 — Création d'un script de supervision

Après avoir travaillé sur la sécurisation et la surveillance de mon serveur Debian, j'ai souhaité automatiser certaines vérifications.

L'objectif est de créer un script Bash capable de récupérer rapidement des informations sur l'état du serveur : utilisation du processeur, mémoire disponible, espace disque et fonctionnement du service SSH.

J'ai commencé par créer un répertoire pour regrouper mes scripts :

```
mkdir -p ~/scripts
cd ~/scripts
```

J'ai ensuite créé mon premier script :

```
nano monitoring.sh
```

### 6.2 — Développement du script Bash

J'ai utilisé plusieurs commandes Linux pour récupérer les informations essentielles sur le serveur et les afficher dans un rapport lisible.

Voici le contenu du script :

```
#!/bin/bash

echo "=================================="
echo "     BOREALIS LINUX LAB"
echo "     Rapport de supervision"
echo "=================================="

echo ""
echo "Date : $(date)"
echo "Serveur : $(hostname)"

echo ""
echo "=== CHARGE SYSTEME ==="
uptime

echo ""
echo "=== MEMOIRE RAM ==="
free -h

echo ""
echo "=== ESPACE DISQUE ==="
df -h /

echo ""
echo "=== SERVICE SSH ==="

if systemctl is-active --quiet ssh; then
    echo "SSH : ACTIF"
else
    echo "SSH : INACTIF"
fi

echo ""
echo "=== FIN DU RAPPORT ==="
```

Ce script rassemble plusieurs contrôles dans une seule commande, ce qui évite de devoir les exécuter manuellement les uns après les autres.

La commande `uptime` indique la charge moyenne du système, mais ne mesure pas directement le pourcentage d'utilisation du processeur.

### 6.3 — Attribution des permissions

Une fois le script enregistré, je lui ai donné les droits d'exécution :

```
chmod +x monitoring.sh
```

J'ai ensuite lancé le script :

```
./monitoring.sh
```

Le terminal doit afficher un rapport contenant les informations système et l'état du service SSH.

Exemple de résultat attendu

Illustration

```
==================================
     BOREALIS LINUX LAB
     Rapport de supervision
==================================

Date : Fri Oct 23 19:30:00 CEST 2026
Serveur : borealis-debian

=== CHARGE SYSTEME ===
up 2 days, load average: 0.02, 0.04, 0.01

=== MEMOIRE RAM ===
total   used   free   available
3.8Gi   1.1Gi  2.1Gi  2.5Gi

=== ESPACE DISQUE ===
Filesystem   Size  Used  Avail  Use%
/dev/sda1     30G  8.0G    20G   29%

=== SERVICE SSH ===
SSH : ACTIF

=== FIN DU RAPPORT ===
```

Les valeurs ci-dessus sont fictives. Ton serveur affichera ses propres informations.

### 6.4 — Enregistrement automatique du rapport

Pour conserver une trace des contrôles, j'ai ensuite prévu d'enregistrer les résultats dans un fichier journal.

J'ai créé un répertoire dédié :

```
mkdir -p ~/scripts/logs
```

Puis j'ai testé l'enregistrement du rapport :

```
~/scripts/monitoring.sh >> ~/scripts/logs/monitoring.log 2>&1
```

Pour consulter les résultats enregistrés :

```
cat ~/scripts/logs/monitoring.log
```

L'utilisation de `>>` permet d'ajouter chaque nouveau rapport à la suite du fichier, sans écraser les précédents.

### 6.5 — Planification automatique avec cron

Pour éviter d'exécuter le script manuellement, j'ai prévu de programmer son lancement avec `cron`.

J'ouvre la configuration des tâches planifiées :

```
crontab -e
```

J'ajoute la ligne suivante :

```
0 */6 * * * /bin/bash /home/UTILISATEUR/scripts/monitoring.sh >> /home/UTILISATEUR/scripts/logs/monitoring.log 2>&1
```

Je remplace `UTILISATEUR` par le nom de mon compte Debian.

Cette configuration permet d'exécuter le script automatiquement toutes les six heures.
