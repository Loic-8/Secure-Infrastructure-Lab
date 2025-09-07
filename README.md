# Laboratoire d'Infrastructure Sécurisée

Ce projet documente la mise en place d'un environnement de serveurs virtualisés et isolés, simulant un réseau d'entreprise de base.

## 🗺️ Schéma du Réseau

-   **Type de réseau :** VMware Host-only (`VMnet2`)
-   **Sous-réseau :** `192.168.100.0/24`
-   **Objectif :** Créer un environnement isolé pour la configuration et les tests de sécurité, sans accès direct à Internet.

---

## 🖥️ Serveurs du Laboratoire

### 1. Serveur Linux (`Linux-SRV-01`)
...
-   **Mesures de durcissement appliquées :**
    -   Service SSH sécurisé, configuration de SELinux et `firewalld`.
    -   *Pour plus de détails, voir le [rapport complet dans le dépôt Linux-Hardening](lien-vers-votre-dépôt-linux-hardening).*

### 2. Contrôleur de Domaine (`Win-DC-01`)

-   **Système d'exploitation :** Windows Server 2022 (Expérience de bureau)
-   **Adresse IP Statique :** `192.168.100.20` *(Note : nous allons configurer cette IP dans le prochain module)*
-   **Rôle :** Contrôleur de Domaine Active Directory.
-   **Configuration :**
    -   Promotion en Contrôleur de Domaine.
    -   Création d'une nouvelle forêt et d'un nouveau domaine : **`mondomaine.local`**.

---

## 🧠 Compétences Démontrées

-   Mise en place d'un réseau virtuel isolé.
-   Installation et configuration de serveurs **Linux (type RHEL)** et **Windows Server**.
-   Mise en œuvre de **bonnes pratiques de sécurité** (hardening, partitionnement).
-   Déploiement d'un service d'annuaire **Active Directory**.
