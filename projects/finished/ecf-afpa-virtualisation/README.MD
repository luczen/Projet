# Projet d'Administration Systèmes et Réseaux

## Présentation
Ce projet est divisé en trois parties, chacune abordant un aspect essentiel de la gestion d’infrastructure informatique :

1. **Virtualisation et sauvegarde d’infrastructure**
2. **Administration et sécurisation d’un domaine Active Directory**
3. **Administration de serveurs Linux sécurisés**

L’objectif global est de concevoir, déployer et sécuriser une infrastructure complète pour une entreprise fictive, en appliquant les bonnes pratiques d’administration et de sécurité.

---

## Partie 1 : Virtualisation et Sauvegarde d’Infrastructure
**Objectifs :**
- Installer et configurer un hyperviseur (Proxmox VE).
- Créer et configurer des machines virtuelles (Windows Server et Debian).
- Mettre en place un réseau virtuel avec OPNsense pour le routage et la sécurité.
- Déployer une stratégie de sauvegarde (snapshots automatisés et PBS).
- Sécuriser l’accès à l’hyperviseur (MFA, gestion des droits).

**Points clés :**
- Hyperviseur : Proxmox VE.
- Routage/Pare-feu : OPNsense.
- VM : Windows Server (AD DS), Debian (Apache2).
- Sauvegarde : snapshots quotidiens + PBS sur NAS.
- Sécurité : désactivation du compte root, MFA, droits administrateurs.

---

## Partie 2 : Administration et Sécurisation d’un Domaine Active Directory
**Objectifs :**
- Structurer l’Active Directory (OU, comptes utilisateurs, groupes).
- Mettre en place des stratégies de sécurité (GPO).
- Déploiement automatisé d’applications (LibreOffice, Firefox).
- Configuration avancée (ADMX Firefox, page d’accueil Ecosia).
- Activer l’audit des connexions et exporter les journaux.

**Points clés :**
- Domaine : TechnoPlus.lan.
- GPO : sécurité, déploiement logiciel, configuration navigateur.
- Supervision : audit des connexions, suivi des processus, export des logs.

---

## Partie 3 : Administration de Serveurs Linux Sécurisés
**Objectifs :**
- Installer et configurer un serveur Linux (Debian).
- Sécuriser SSH (désactivation root, authentification par clé publique).
- Gestion des utilisateurs et groupes.
- Mise en place d’un serveur web (Apache2).
- Configuration du pare-feu (UFW).
- Gestion et analyse des journaux.
- Déploiement de GestSup avec intégration LDAP.

**Points clés :**
- SSH durci (clé publique, pas de mot de passe).
- Pare-feu actif (ports SSH, HTTP/HTTPS).
- Journaux activés pour supervision.
- GestSup installé et synchronisé avec Active Directory.

---

## Prérequis Techniques
- Hyperviseur : Proxmox VE.
- OS : Windows Server, Debian.
- Pare-feu : OPNsense.
- Services : Active Directory, Apache2, GestSup.
- Sauvegarde : PBS + NAS.

---

## Structure des Dossiers
```
/Projet-Infra
│
├── Partie1_Virtualisation_Sauvegarde/
│   ├── Installation_Proxmox.md
│   ├── Configuration_VM.md
│   ├── Sauvegarde_Restauration.md
│
├── Partie2_AD_Securisation/
│   ├── Arborescence_OU.md
│   ├── GPO_Securite.md
│   ├── Audit_Logs.md
│
├── Partie3_Linux_Securise/
│   ├── SSH_Securisation.md
│   ├── PareFeu_Journaux.md
│   ├── GestSup_LDAP.md
│
└── README.md
```

---

## Comment utiliser ce projet ?
1. Suivre les étapes de la Partie 1 pour mettre en place l’infrastructure virtualisée.
2. Configurer le domaine Active Directory selon la Partie 2.
3. Déployer et sécuriser le serveur Linux comme décrit dans la Partie 3.
4. Vérifier la cohérence et la sécurité via les audits et journaux.
