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
