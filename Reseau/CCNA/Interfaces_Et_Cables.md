---
title: Interfaces Et Cables
author: KAZMIERCZAK, Cyril
---

### Presentation
Les interfaces et les cables constituent la couche physique d'un reseau informatique.
Ils assurent le transport des signaux (electriques, lumineux ou radio) et definissent la connectique permettant de relier physiquement les equipements (routeurs ou commutateurs) aux postes clients et aux serveurs.

## Interfaces Reseaux
L'interface est le point de contact materiel entre l'equipement et le media de transmission.

- **Le connecteur RJ45 (Registered Jack 45)**: prise en plastique standard situee au bout des cables a paire torsadee, dote de 8 broches metalliques.

- **Le port et le module SFP/SFP+/QSFP**: emplacements modulaires presents sur les equipements professionnels (commutateurs, routeurs). Permettent d'inserer un petit emetteur-recepteur (transceiver) adapte au type de media choisi (module SFP pour fibre optique).

- **Les connecteurs de fibre optique**: contrairement au RJ45, il existe plusieurs formats de prises pour la fibre:
	- **LC (Lucent Connector)**: petit format, tres populaire dans les commutateurs et les modules SFP.
	- **SC (Subscriber Connector)**: format carre "pousser-tirer", souvent utilise sur les boitiers muraux ou les installations grand public (FTTH).
	- **ST (Straight Tip)**: format rond a baionnette (plus ancien).

- **La carte reseau (NIC - Network Interface Card)**: composant materiel (integre a la carte mere ou sous forme de carte d'extension PCIe) qui prepare, envoie et recoit les donnees sur le reseau. Chaque carte possede une adresse physique unique au monde appelee adresse MAC.

## Cables Reseaux
Le choix du cablage depend de la distance a couvrir, du debit souhaite et de l'environnement (sensibilite aux perturbations electromagnetiques).

- **Le cable a paire torsadee (Cable Ethernet RJ45)**: c'est le plus repandu dans les reseaux locaux (LAN). Il est compose de 4 paires de fils de cuivre entrelaces pour limiter les inteferences. Il se decline en plusieurs categories:
	- **Categorie 5e (Cat 5e)**: debit jusqu'a 1 Gbit/s sur 100 metres.
	- **Categorie 6 (Cat 6)**: debit jusqu'a 10 Gbit/s sur de courtes distances (environ 37 a 55m).
	- **Categorie 6a (Cat 6a)**: debit jusqu'a 10 Gbit/s garanti sur 100 metres, mieux blinde.
	- **Blindages courants**: **UTP** (non blinde), **FTP** (blindage global par feuille d'aluminium), ou **SFTP** (blindage maximal, tresse + paires blindees individuellement).

- **La fibre optique**: utilise des impulsions lumineuses pour transporter les donnees a tres haute vitesse sur de longues distances, sans aucune sensibilite aux interferences electromagnetiques.
	- **Fibre Monomode (SMF)**: coeur tres fin, utilise un laser. Ideale pour les tres longues distances (plusieurs kilometres, reseaux operateurs ou liaisons inter-batiments).
	- **Fibre Multimode (MMF)**: coeur plus large, utilise des LED ou VCSEL. Adaptee aux distances courtes (Data Centers, raccordement de serveurs ou de commutateurs dans un meme batiment).

- **Le cable coaxial**: historiquement utilise dans les premiers reseaux (Ethernet fin/gros), il est aujourd'hui principalement reserve a la distribution de la television ou aux connexions Internet par le cable (technologie de modem cable). 
