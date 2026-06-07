Cubic2‑ARM64 — Projet TN365

Cubic2‑ARM64 est un fork du projet Cubic, entièrement repensé pour ARM64.
Il permet de générer des images .img UEFI ARM64 personnalisées via ubuntu‑image, avec support des desktops, IA, outils admin, thèmes TN365, et configurations avancées.

Ce projet a été créé pour fournir un outil graphique moderne permettant de construire facilement des images ARM64 complètes et professionnelles.
✨ Fonctionnalités principales

    Génération d’images ARM64  
    Crée des images .img UEFI ARM64 modernes, compatibles Raspberry Pi, SBC ARM64, serveurs ARM, VM UEFI, etc.

    Backend ubuntu‑image intégré  
    Remplace totalement la génération ISO x86_64 par un système basé sur ubuntu-image et un manifest YAML.

    Assistant graphique complet  
    Interface simple et intuitive (GTK) pour configurer rootfs, kernel, paquets, services, thèmes et partitions.

    Support UEFI ARM64 natif  
    Génération automatique des partitions EFI, bootloader ARM64, shim, grub-efi-arm64.

    Personnalisation avancée du rootfs  
    Ajout, suppression ou modification de paquets, services, thèmes, IA, outils admin, environnements de bureau.

    Gestion automatique du manifest YAML  
    Génération dynamique du fichier manifest.yaml selon les choix de l’utilisateur.

    Logs en temps réel  
    Affichage des logs ubuntu-image directement dans l’interface.

🖥️ Fonctionnalités TN365 intégrées

    Profils préconfigurés TN365

        KDE Maia ARM64

        XFCE ARM64

        AI Edition ARM64

        Gaming ARM64

    Branding TN365  
    Thèmes, KSplash, icônes, fonds d’écran, sons de démarrage/extinction.

    Support IA local  
    Intégration possible de modèles IA (Ollama, GPT4All, LM Studio).

    Outils Admin Pro  
    Sélection d’outils système, réseau, sécurité et maintenance.

🧩 Fonctionnalités techniques

    Chroot ARM64 complet  
    Gestion du rootfs ARM64 via QEMU + binfmt.

    Support multi‑desktops  
    KDE, XFCE, GNOME, MATE, LXQt, Budgie, Cinnamon.

    Gestion des services systemd  
    Activation/désactivation automatique selon le profil.

    Configuration automatique du clavier FR  
    Pack FR intégré pour Live + TTY + X11 + Calamares.

    Optimisation SquashFS ARM64  
    Compression xz/BCJ, exclusion de fichiers inutiles.

🔧 Fonctionnalités à venir (Roadmap)

    Mode “ISO x86_64 + IMG ARM64” hybride

    Éditeur graphique de manifest YAML

    Support des images multi‑boot ARM64

    Génération d’images cloud ARM64

    Support Docker ARM64 préinstallé
🛠️ Installation de Cubic2‑ARM64

Cubic2‑ARM64 est un fork de Cubic conçu pour générer des images ARM64 UEFI via ubuntu-image.
Le projet fonctionne sur Ubuntu 22.04 / 24.04 (x86_64 ou ARM64).


📦 1. Installer les dépendances nécessaires

bash
sudo apt update
sudo apt install python3 python3-gi python3-gi-cairo \
                 gir1.2-gtk-3.0 gir1.2-vte-2.91 \
                 qemu-user-static binfmt-support \
                 ubuntu-image git

Ces paquets fournissent :

    GTK3 → interface graphique

    VTE → terminal intégré

    QEMU + binfmt → chroot ARM64

    ubuntu-image → génération .img ARM64

📥 2. Cloner le dépôt Cubic2‑ARM64
bash

git clone https://github.com/webmasterdu63-creator/Cubic2-ARM64.git
cd Cubic2-ARM64

▶️ 3. Lancer Cubic2‑ARM64
bash

python3 cubic2-arm64.py

    Le nom du fichier principal changera selon ton organisation interne.
    Tu pourras mettre : main.py, cubic2.py, ou tnbuilder.py.

🧪 4. Tester le mode ARM64

Une fois l’interface ouverte :

    Choisir Mode ARM64 (ubuntu-image)

    Sélectionner un rootfs ARM64

    Ajouter les paquets / thèmes / services

    Générer l’image .img ARM64

📁 5. Structure recommandée du projet
Code

Cubic2-ARM64/
 ├── src/
 │    ├── gui/           # Interface GTK
 │    ├── arm64/         # Backend ubuntu-image
 │    ├── chroot/        # Gestion rootfs ARM64
 │    └── utils/
 ├── presets/            # Profils TN365 (KDE, XFCE, AI…)
 ├── examples/           # Manifests YAML exemples
 ├── README.md
 └── LICENSE

🧩 6. Dépendances optionnelles (recommandées)

Pour les fonctionnalités avancées TN365 :
bash

sudo apt install squashfs-tools xz-utils \
                 grub-efi-arm64 shim-signed \
                 debootstrap

🎯 7. Désinstallation
bash

rm -rf Cubic2-ARM64

