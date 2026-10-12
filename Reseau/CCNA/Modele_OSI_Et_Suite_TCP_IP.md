---
title: Modele OSI Et Suite TCP/IP
author: KAZMIERCZAK, Cyril
---

## Qu'est-ce qu'un modele reseau?
Un *modele reseau* est une structure theorique sous forme de couches supersposees qui definit les regles, les etapes et les protocoles necessaires pour que des equipements informatiques puissent communiquer entre eux.
Sans ces modeles, un ordinateur Apple, un smartphone Android et un serveur Linux ne pourraient pas s'echanger d'infomations car ils ne parleraient pas la meme langue.
Le modele OSI et la suite TCP/IP sont les deux architectures de reference utilisees pour comprendre et normaliser les communications reseau.

## Le modele OSI
*OSI* signifie _Open Systems Interconnection Model_. Il s'agit d'un modele conceptuel qui categorise et standardise les differentes fonctions dans un reseau. Le modele OSI a ete cree par l'_International Organization for Standardization_ (*ISO*).
Les differentes fonctions d'un reseau sont reparties en sept couches. Ces couches travaillent ensemble pour faire fonctionner le reseau.

### Les sept couches du modele OSI
La communication passe de la couche 7 a la couche 1. Chaque couche effectue une tache specifique avant d'envoyer les donnees a la couche suivante.

#### Couche 7 - Couche applicative
Couche la plus proche de l'utilisateur final. Initie la communication entre l'utilisateur et les applications avec lesquelles il interagit. Sur cette couche, les donnees sont traduites de la syntaxe vers laquelle elles ont ete converties en quelque chose que l'utilisateur peut lire.
Exemples d'applications de couche 7: navigateur Web (Chrome, Safari ou Firefox) ou application de messagerie.
La couche 7 peut egalement identifier les partenaires de communication, verifier les ressources disponibles et s'assurer que la communication est correctement synchronisee.

#### Couche 6 - Couche de presentation
La couche de presentation s'occupe de preparer les donnees a la couche applicative. Les deux dispositifs qui communiquent peuvent utiliser differentes methodes d'encodage de leurs donnees. La couche 6 transforme donc les donnees entrantes en quelque chose qui peut etre lu au niveau de la couche application. Cela inclut le chiffrement et le dechiffrement des donnees.
La couche de presentation compresse egalement les donnees qui proviennent de la couche application avant de les envoyer a la couche 5, la couche session.

#### Couche 5 - Couche session
Gere l'ouverture et la fermeture des communications reseau entre deux appareils en interaction. La session fait reference au delai entre l'ouverture et la cloture de l'interaction. La couche de session s'assure que la session est ouverte pendant une periode suffisamment longue pour que toutes les donnees necessaires soient envoyees. La couche de session ferme ensuite pour eviter d'investir des ressources inutiles.
Synchronise le transfert des donnnees. Si une grande quantite de donnees est envoyee, la couche de session peut configurer des points de controle. Si la transmission est interrompue avant que toutes les donnees ne soient telechargees, les points de controle permettent de reprendre la transmission sans qu'elle ne recommence.

#### Couche 4 - Couche transport
Gere la communication de bout en bout entre les appareils qui interagissent les uns avec les autres. La gestion de la communication implique de prendre les donnees dans la couche session et de les diviser en elements appeles segments. La couche de transport sur le dispositif recevant la communication gere le reassemblage des segments en donnees qui sont consommables par la couche de session.
La couche transport s'occupe de la gestion du flux et de tous les messages d'erreur necessaires qui doivent etre envoyes en cas de probleme. Pour gerer le flux de donnees, la couche transport s'assure qu'elle n'est pas envoyee si rapidement que l'appareil du destinataire ne peut pas la gerer. Pour controler les erreurs, la couche de transport verifie si les donnees transmises ont ete entierement effectuees. Si ce n'est pas le cas, cette couche demandera une retransmission.
La couche 4 est l'endroit ou fonctionnent les numeros de port TCP (Transmission Control Protocol) et UDP (User Datagram Protocol). Les adresses IP (Internet Protocol) fonctionnent a la couche 3, la couche reseau. TCP, UDP et IP sont des protocoles qui facilitent la facon dont les donnees sont envoyees et recues.

#### Couche 3 - Couche reseau
Facilite le transfert de donnees lorsque deux reseaux communiquent entre eux. Si deux dispositifs de communication utilisent le meme reseau, la couche reseau n'est pas necessaire. La couche reseau divise les segments qui proviennent de la couche de transport. Celles-ci sont appelees paquets. La division des segments en paquets se produit sur le dispositif de l'expediteur et ils sont reassembles sur le dispositif de reception.
La couche reseau fonctionne egalement comme un outil d'efficacite. Il determine le chemin physique optimal necessaire pour acheminer les donnees vers leur destination. Cette fonction est appelee routage.

#### Couche 2 - Couche liaison de donnees
Similaire a la couche reseau sauf que la couche liaison de donnees facilite le transfert de donnees entre deux appareils utilisant le meme reseau. Dans la couche de liaison de donnees, les paquets sont divises en morceaux appeles trames. Similaire a la couche reseau, la couche de liaison de donnees gere le controle des flux et des erreurs. La couche de transport est differente dans la mesure ou elle ne gere le flux de donnees et les erreurs que lorsque deux reseaux communiquent entre eux.
Dans la couche de liaison de donnees, il y a deux sous-couches, les couches de controle d'acces aux medias (MAC) et de controle de liaison logique (LLC). La majorite des commutateurs executent leurs taches a la couche 2. Dans certains cas, les commutateurs fonctionnent a la couche 3 parce qu'ils facilitent la communication entre deux reseaux ou les reseaux locaux virtuels (VLAN). Cela doit se produire au niveau de la couche 3, car dans ces situations, les donnees doivent etre acheminees, qui est une tache de couche 3.

#### Couche 1 - Couche physique
Implique l'equipement physique qui transfere des donnees, comme les commutateurs et les cables. Dans cette couche, les donnees sont converties en chaines de 0 et de 1. Dans la couche physique, les dispositifs doivent convenir d'une methode pour distinguer les 0 et les 1, ce qui permet aux donnees numeriques d'etre correctement interpretees par chaque dispositif.
La couche physique comprend une variete de composants, tels que les cables, la radiofrequence utilisee pour transmettre les donnees, le Wi-Fi et les autres structures physiques pour transmettre les donnees, telles que les broches, les tensions necessaires et les types de ports. 
 
