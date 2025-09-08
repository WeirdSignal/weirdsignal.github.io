---
title: Gaulix : Un Réseau Meshtastic Français
date: 2025-09-09
layout: default
tags: [meshtastic, radio, projets]
---

# Gaulix : Un Réseau Meshtastic Français

## Introduction

Gaulix est une communauté française dédiée au développement et à l'utilisation du réseau Meshtastic, un système de communication maillé open-source basé sur la technologie LoRa. Meshtastic permet de créer des réseaux décentralisés et hors grille pour l'échange de messages texte, de positions GPS et d'autres données, sans dépendre d'infrastructures traditionnelles comme Internet ou les réseaux cellulaires. En France, Gaulix vise à unifier les utilisateurs autour d'un réseau national, favorisant l'interconnexion à l'échelle du pays et même avec d'autres pays européens. Ce réseau est particulièrement utile pour les communications en cas de crise, les activités de plein air ou les projets communautaires. Gaulix encourage une approche collaborative, avec des règles définies collectivement pour optimiser le fonctionnement du maillage.

Le réseau Gaulix repose sur une structure de 8 canaux standardisés, dont les cinq premiers sont essentiels au niveau national :
- Canal 1 (Fr_Balise) : Réservé aux données GPS, informations de nœuds et discussions directes.
- Canal 2 (Fr_EMCOM) : Dédié aux communications d'urgence.
- Canal 3 (Fr_BlaBla) : Pour les discussions informelles.
- Canal 4 (Fr_DIY) : Pour les makers et la télémétrie.
- Canal 5 (admin) : Pour l'administration des nœuds.

Les canaux 6 à 8 sont libres pour des usages locaux ou régionaux. Les nœuds sont nommés selon des conventions précises, comme l'utilisation des derniers caractères de l'adresse MAC pour les noms courts, et des formats incluant le département, la commune et le rôle pour les noms longs.

## Les Réglages "Long Moderate"

Dans le cadre du réseau Gaulix, les réglages recommandés pour les modems LoRa sont configurés en mode "Long Moderate". Ce préréglage est choisi pour équilibrer portée, vitesse et fiabilité des communications, adapté à un réseau national couvrant l'ensemble du territoire français. Spécifiquement, il opère à une fréquence de 869,4625 MHz, qui est conforme aux bandes autorisées en Europe pour les transmissions LoRa.

Pourquoi "Long Moderate" ? Ce mode offre une portée étendue (jusqu'à plusieurs kilomètres en conditions optimales) tout en maintenant une vitesse de transmission modérée (environ 0,34 kbps), ce qui réduit la consommation d'énergie et minimise les interférences dans un maillage dense. Contrairement à des préréglages comme "Long Fast" (plus rapide mais moins fiable sur de longues distances), "Long Moderate" priorise la robustesse pour interconnecter des nœuds distants, facilitant ainsi l'expansion du réseau vers d'autres pays européens. Ce choix est motivé par l'objectif de Gaulix de créer un maillage unifié et résilient, évitant les fragmentations régionales. Les utilisateurs peuvent appliquer ces réglages via des codes QR ou des URL fournis par la communauté, assurant une compatibilité homogène.

## Le Pixel Server

Le "Pixel Server" fait référence au serveur hébergeant l'outil Meshtastic MQTT Explorer, une plateforme dédiée à la surveillance et à l'exploration des trames transmises sur le réseau Meshtastic. Ce serveur, accessible via des domaines comme pixel-server.ovh, permet de collecter les données MQTT (un protocole léger pour l'échange de messages) envoyées par les nœuds du réseau. Dans le contexte de Gaulix, il sert de backend pour aggregator les informations en temps réel, telles que les positions des nœuds, les messages et les métriques du maillage.

Développé comme un projet open-source (disponible sur GitHub), le Pixel Server facilite l'intégration avec des applications clientes et assure une visualisation centralisée. Il n'est pas limité à la France mais est particulièrement utilisé par la communauté Gaulix pour monitorer le réseau national, aidant à identifier les zones de couverture et à optimiser les déploiements.

## L'Affichage sur la Carte

L'une des fonctionnalités phares de Gaulix est l'affichage des nœuds sur une carte interactive, accessible via des sites comme map.gaulix.fr ou meshtastic-mqtt-explorer.pixel-server.ovh. Cette carte utilise les données collectées par le Pixel Server pour représenter en temps réel les emplacements des nœuds, les connexions maillées et les messages transmis.

Pour apparaître sur la carte, un nœud doit activer le partage de position (via GPS intégré ou connecté) et se connecter au broker MQTT du réseau. Les données sont ensuite traitées et affichées sur une interface web avec des marqueurs pour chaque nœud, indiquant leur statut, leur rôle (comme CLIENT ou ROUTER) et leurs liens avec d'autres nœuds. Cela permet aux utilisateurs de visualiser la couverture du maillage, de détecter les zones faibles et de planifier des extensions. La carte est interactive, offrant des filtres pour les paquets, les nœuds connectés et les historiques de messages, rendant le réseau plus transparent et accessible à tous.

En résumé, Gaulix transforme Meshtastic en un outil puissant et communautaire pour la France, avec des réglages optimisés, un serveur dédié et une visualisation cartographique qui renforcent sa résilience et son utilité quotidienne. Pour rejoindre le réseau, consultez les ressources communautaires et configurez votre appareil en suivant les guidelines officielles.
