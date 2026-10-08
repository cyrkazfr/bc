---
title: Interfaces Et Cables
author: KAZMIERCZAK, Cyril
---

## Presentation
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

## Ethernet
L'Ethernet est la technologie standard mondiale utilisee pour connecter des appareils entre eux au sein d'un reseau local filaire (LAN) ou pour les relier a Internet. Creee dans les annees 1970 et encadree par la norme internationale IEEE 802.3, elle utilise des cables physiques (generalement equipes de connecteurs RJ45) pour transferer des donnees de maniere ultra-rapide, stable et securisee.
Contrairement au Wi-Fi, l'Ethernet n'est pas soumis aux fluctuations de signal ou aux obstacles physiques (murs, micro-ondes), ce qui garantit un debit maximal constant.

### Standards Ethernet
Les standards Ethernet sont encadres par le groupe de travail IEEE 802.3 de l'Institute of Electrical and Electronics Engineers. Ils definissent precisement la couche physique (cables, connecteurs) et la couche liaison de donnees (format des trames) pour garantir l'interoperabilite des equipements reseau a travers le monde.

#### Nomenclature officielle
Chaque standard suit une logique d'appelation stricte divisee en trois parties:
- **Le nombre (Debit)**: `10` pour 10 Mb/s, `100` pour 100 Mb/s, `1000` pour 1 Gb/s, `10G` pour 10 Gb/s.
- **BASE**: signifie "bande de base" (_baseband_), indiquant que le signal numerique est transmis directement sans modulation de frequence.
- **Le suffixe (Media/Distance)**: `-T` pour les paires torsadees en cuivre (_Twisted pair_), `-SR/-LR` pour la fibre optique a courte ou longue distance.

#### Principaux standards Ethernet (Cuivre & Fibre)
| **Norme IEEE** | **Nom Standard** | **Debit Maximal** | **Type de support (Media)** | **Portee Max** |
| :--- | :--- | :--- | :--- | :--- |
| **802.3i** | **Ethernet (10BASE-T)** | 10 Mb/s | Cuivre (Paires torsadees Cat 3) | 100m |
| **802.3u** | **Fast Ethernet (100BASE-TX)** | 100 Mb/s | Cuivre (Cat 5 ou superieur) | 100m |
| **802.3ab** | **Gigabit Ethernet (1000BASE-T)** | 1 Gb/s | Cuivre (Cat 5e,6) | 100m |
| **802.3an** | **10 Gigabit Ethernet (1GBASE-T)** | 10 Gb/s | Cuivre (Cat 6a ou superieur) | 100m |

### Categories de cables Ethernet (RJ45)
Les performances d'un reseau filaire dependent directement de la categorie (**Cat**) imprimee sur la gaine du cable:

| **Categorie** | **Debit Maximal** | **Bande passante** | **Usage recommande** |
| :--- | :--- | :--- | :--- |
| **Cat 5** | **1 Gb/s** | 100 MHz | Connexions Internet basiques a la maison |
| **Cat 6** | **10 Gb/s** (sur max 55m) | 250 MHz | Le **standard actuel** ideal pour le streaming 4K et le gaming |
| **Cat 6a** | **10 Gb/s** (sur 100m) | 500MHz | Le meilleur choix pour le futur (compatibilite Box fibre de 2 a 8 Gb/s) |
| **Cat 8** | **40 Gb/s** (sur max 30m) | 2000 MHz | Reserve aux serveurs et centres de donnees |

### Types de blindage
Pour eviter les parasites electriques causes par les autres cables ou appareils menagers, l'Ethernet utilise differents types de protection:
- **U/UTP**: cable non blinde, tres flexible mais sensible aux interferences.
- **F/UTP**: blindage global par une feuille d'aluminium autour des fils.
- **S/FTP**: blindage maximal (chaque paire de fils est entouree d'aluminium, et le cable entier possede une tresse en cuivre).
