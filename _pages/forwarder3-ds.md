---
title: "Forwarder3-DS"
---

[Post Originel](https://gbatemp.net/threads/nds-forwarder-cias-for-your-home-menu.426174/)

Ceci est une traduction d’un post en anglais. Vous pouvez me contacter sur @hrshl-is-crap-at-games (Tumblr) s' il y a un problème de traduction.
Info intéressante : appuyer sur select pendant le chargement du jeu permet d’activer l’affichage “natif”.


# Guide

Notes :
+ Pour faire des raccourcis pour des roms SD sur votre 3DS, suivez ce [guide](https://wiki.ds-homebrew.com/ds-index/forwarders)
+ Pour installer plus de 40 raccourcis et/ou si vous voulez une bannière différente de l’icône du jeux, alors utilisez [YANBF](https://gbatemp.net/threads/nds-yet-another-nds-bootstrap-forwarder-more-than-40-forwarders-are-now-possible.606138/)

Vous vous rappelez des vieux jours avec les raccourcis de chaîne sur votre wii qui démarre les jeux depuis votre disque dur ou carte SD?
Vous avez déjà voulu une façon de démarrer les jeux DS comme des titres originaux depuis le menu d’accueil de votre 3DS ou DSi? Maintenant vous pouvez!
Dans ce tutoriel, vous pouvez faire des raccourcis qui démarrent les ROMs NDS depuis une carte SD (ou si vous voulez, une flashcard en mode DS (R4))

## Pré-requis
### DSi :
+ [GodMode9i](https://github.com/DS-Homebrew/GodMode9i/releases)
+ Unlaunch
+ hiyaCFW
+ TMFH (Manager de Titre pour Hiya)
+ Une Carte SD
+ (Optionnel) flashcard en mode DS (aka, adaptateur Slot-1 vers carte microSD)

### 3DS :
+ [GodMode9](https://github.com/d0k3/GodMode9/releases)
+ Un CFW qui patch TWL_FIRM ([Luma3DS](https://github.com/d0k3/Decrypt9WIP/releases))
+ Un installeur CIA (FBI, DevMenu, etc)
+ Une carte SD (ou carte microSD pour N3DS)
+ (Optionnel) flashcard en mode DS (aka, adaptateur Slot-1 vers carte microSD)

### PC :
+ Version x64 de votre OS (peut être nécessaire pour Windows)
+ Forwarder3-DS. ([Téléchargement](https://www.dropbox.com/s/b9de5ii6vm3dxfn/Forwarder3DS-v2.9.6.zip?dl=0), vérifiez le post originel pour les dernières versions du programme)

### Windows seulement :
+ Microsoft Visual C++ 2010 SP1 Redistributable

### Windows/Linux/Mac :
+ Java 8 Update 251 (Merci à [@djwyman](https://gbatemp.net/members/435779/) pour avoir remarqué ça)
+ Java SE Development Kit 8u281 (Merci à [@RoyalTea](https://gbatemp.net/members/549344/) pour avoir remarqué ça)
+ Langue locale mise en Anglais
+ Linux: JavaFX

Utilisateurs de Carte SD : regardez quels jeux fonctionnent ou pas :
[nds-bootstrap compatibility list](https://docs.google.com/spreadsheets/d/1LRTkXOUXraTMjg1eedz_f7b5jiuyMv2x6e_jY_nyHSc/edit#gid=0)

## Instructions
### Partie 1.1 (Carte SD)
Faites ces étapes. Les raccourcis ne marcheront pas si vous ne les faites pas.
1. Téléchargez les fichiers requis [ici](https://github.com/RocketRobz/NTR_Forwarder/releases) (regardez pour les tags commençant par “SD”)
1. Dans le fichier 7z, extrayez ce qui est dans "for SD card root” vers la racine de la carte SD

Après que vous ayez extrait le pack pour votre carte sd, vous pouvez éditer “ds:/_nds/nds-bootstrap.ini” et changer un des paramètres.
+ BOOST_CPU :  Si mis sur 1, la fréquence d’horloge de TWL est utilisée, donc plus de lag.
+ SOUND_FREQ : Si mis sur 1, le son sortira en 48kHz, au lieu de 32kHz.
+ LANGUAGE : Si mis sur -1, la langue du système sera utilisée.
+ REGION : Si mis sur -2, la région du jeu DSiWare sera utilisé au lieu de celle du système.

### Partie 1.2 (Flashcard)
Faites ces étapes. Les raccourcis ne marcheront pas si vous ne les faites pas.
Si vous n’avez pas de flashcard, vous pouvez passer cette partie.
*Note : Les flashcards/r4 ne sont plus produites depuis un moment.*

1. Téléchargez un de ces packs

[Original R4/M3 Simply](https://www.dropbox.com/s/juxzri7h8bttunh/DS%20Game%20Forwarder%20pack%20%28Original%20R4%2C%20M3%20Simply%29.7z?dl=0)  
[Acekard 2(i)/M3DS Real](https://www.dropbox.com/s/5elogf885sd62hu/DS%20Game%20Forwarder%20pack%20%28M3DS%20Real%29.7z?dl=0)  
[DSTT/R4i Gold/R4i-SDHC/R4 SDHC Upgrade/SC DSONE](https://www.dropbox.com/s/xxfmvikwmnvsu63/DS%20Game%20Forwarder%20pack%20%28DSTT%2C%20R4i%20Gold%2C%20R4i-SDHC%2C%20SC%20DSONE%29.7z?dl=0)  
[Acekard RPG](https://drive.google.com/file/d/0B2_1xHkEp2_6OHVuZEJwU1BKbEU/view?usp=sharing)  
[R4iDSN/R4i Gold RTS/R4i Gold 3DS Plus](https://www.dropbox.com/s/j8nquh073k9y0h7/DS%20Game%20Forwarder%20pack%20%28R4iDSN%2C%20R4i%20Gold%20RTS%29.7z?dl=0)  
[Ace 3DS+/Gateway Blue Card/R4iLS/R4iTT](https://www.dropbox.com/s/fd7dzhn8burcq02/DS%20Game%20Forwarder%20pack%20%28Ace3DS%2C%20GW%20Blue%20Card%2C%20R4iTT%29.7z?dl=0)  
[SC DSTWO](https://www.dropbox.com/s/pyyg0vq8b0nmhqd/DS%20Game%20Forwarder%20pack%20%28SC%20DSTWO%29.7z?dl=0)  

2. Dans le fichier 7z, extrayez ce qui est dans "for Slot-1 microSD" vers la racine de la carte SD de la flashcard, et (si le dossier existe) "for 3DS SD card” vers la racine de la carte SD de la 3DS.

Ce qui sera dans chaque paquets pour charger les ROMs :  
Original R4/M3 Simply - WoodR4 & YSMenu  
DSTT/R4i Gold/R4i-SDHC/R4 SDHC Dual-Core/R4 SDHC Upgrade/SC DSONE, Acekard 2(i)/M3DS Real/R4i-SDHC 1.4.x - YSMenu  
Acekard RPG, Ace 3DS+/Gateway Blue Card/R4iLS/R4iTT, R4iDSN/R4i Gold RTS - WoodR4  

Après que vous avez extrait le paquet pour votre carte, vous pouvez éditer `sd:/nds/ntr_forwarder.ini` et changer un des paramètres. Ce n’est pas possible pour les Acekard RPG, R4 DS, et R4i Gold RTS.
+ NTRCLOCK : Si mis sur 0 ou si A est tenu, l’écran de chargement de la DSi apparaîtra au lieu du menu DS normal, et la fréquence d’horloge de TWL est utilisée, donc plus de lag.
+ DISABLEANIMATION : Si mis sur 1 ou si B est tenu, le menu de chargement de la DS/DSi est sauté.
+ HEALTHSAFETYMSG : Si mis sur 1, le message de santé de l’écran de chargement apparaîtra sur l’écran du bas. Si mis sur 0, l’écran du bas restera blanc sans message de sécurité.

### Partie 2: Récupérez le paquet AP-fix pack de TWiLight Menu++ (Sautez si l’application est déjà installée)
1. Téléchargez la dernière version de TWiLight Menu++ [ici](https://github.com/DS-Homebrew/TWiLightMenu/releases). Récupérez seulement le fichier `3DS.7z`.
1. Dans le fichier 7z, allez dans `_nds`, `TWilightMenu` et `extras`.
1. Glissez le fichier `apfix.pck` dans `sd:/_nds/ntr-forwarder/`.

### Partie 3.1: GodMode9 (3DS)
(Sautez si vous avez déjà les ROMs qu’il vous faut)
1. Vérifiez que vous avez votre carte de jeux DS insérée
1. Tenez START lors de l’allumage pour afficher le menu de sélection.
1. Sélectionnez GodMode9.
1. Dans [root], sélectionnez GAMECART.
1. Copiez le fichier `.nds` ou `_trim.nds` n’importe où sur votre carte SD.
1. Quand vous avez fini de décharger vos ROMs, éteignez le système.  

### Partie 3.2: GodMode9i (DSi)
(Sautez si vous avez déjà les ROMs qu’il vous faut)
1. Vérifiez que vous avez votre carte de jeux DS insérée
1. Sélectionnez GAMECART
1. Appuyez sur A pour décharger la ROM complète, ou appuyez sur Y pour décharger la ROM élaguée.
1. Quand vous avez fini de décharger vos ROMs, éteignez le système.  

### Partie 4: Forwarder3-DS
![]({{ "assets/images/Forwarder3-DS.png" | absolute_url }})  
![]({{ "assets/images/Forwarder3-dsComment.png" | absolute_url }})  
Si quelqu’un se demande comment faire tourner `Forwarder3DS.jar`, je l’ai fait en créant un fichier bat. Donc… j’ai créé le fichier `run.bat` (faites juste un fichier txt où `Forwarder3DS.jar` est et renommez-le en `run.bat` au lieu de `Nouveau Document Texte.txt`) et j’ai fait clic droit dessus, puis “Modifier” et une fois ouvert, j’ai écrit `java -jar Forwarder3DS.jar`.  
Ensuite j’ai sauvegardé, sorti, et double cliqué et fait tourner le forwarder (Forwarder3DS.jar).  

1. A gauche, sélectionnez la carte SD cible que vous utilisez.
**Note :** Si vous n’avez pas de liste de cartes, téléchargez un fichier zip ici, et mettez “forwarders” dans le même dossier que le fichier .jar, et renommer “forwarders” en “.forwarders”.
1. Activez "Automatically set ROM path" pour mettre le chemin où votre ROM est directement dans la carte SD ou la flashcard.
**Utilisateur Linux :** Le chemin automatique est incorrect car il inclut le chemin entier (e.g. /media/$USER/something/). Enlevez cette partie.
**Utilisateur MacOS :** Le chemin automatique est incorrect car il inclut "/Volumes/(cardname)/" au début. Enlevez cette partie.
1. Utilisateur DSi : Activez "Keep .NDS files".
1. Cliquez sur le dossier en haut à droite et trouvez les ROMs sur la carte SD (ou flashcard) que vous utilisez, ou glissez/déposez les (depuis la carte SD ou flashcard, pas le PC) dans la fenêtre.
1. Utilisateur de carte SD : Si vos sauvegardes de jeux DS sont dans le même dossier que la ROM, déplacez-les dans un dossier nommé “saves”, qui devrait être au même endroit que la ROM.
1. Si vous jouez une version hack/traduite d’un jeux DSi-Enhanced qui a eu sa bannière/title édité, trouvez la bannière pour le jeux, faites un clic-droit dans Forwarder3-DS, cliquez “Import banner”, et cliquez sur la bannière à utiliser.
1. Si vous utilisez une ROM homebrew, cliquez dessus, puis effacez et tapez le titre du jeu.
1. Cliquez sur le bouton disquette pour générer les raccourcis.  

Finalisation (DSi) :
1. Copiez le fichier NDS fait par l’application vers la carte SD de votre DSi.
1. Installez le raccourci NDS en utilisant TMFH.  

Finalisation (3DS) :
1. Copiez le CIA vers la carte SD de votre 3DS, ou mettez le dans Boop pour une installation via réseau.
1. Installez le CIA. Si vous utilisez EmuNAND, installez-le dans Sys et Emu NANDs.  

Vous avez maintenant fini ! Amusez-vous à jouer via les raccourcis !

## Remerciements
[@Olmectron](https://gbatemp.net/members/320499/), pour avoir créé Forwarder3-DS.  
Moi ([@RocketRobz](https://gbatemp.net/members/rocketrobz.263852/)), pour avoir créé le Auto-Boot ROM Path setter pour DSTT/R4i Gold/R4i-SDHC/R4 SDHC Dual-Core/R4 SDHC Upgrade/SC DSONE, Acekard 2(i)/R4iTT, et DSTWO.  
[@ahezard](https://gbatemp.net/members/383573/), pour avoir fait les modèles de raccourcis pour la R4/M3, Acekard RPG, R4iDSN/R4i Gold RTS, et nds-bootstrap.  
[@Apache Thunder](https://gbatemp.net/members/105648/), pour avoir recréé le menu de chargement de la DS/DSi.  
[@MasterCheese](https://gbatemp.net/members/391610/), pour m’avoir ([@RocketRobz](https://gbatemp.net/members/rocketrobz.263852/)) aidé à faire fonctionner les cartes Ace3DS Plus, Gateway Blue Card, et les cartes de [www.r4isdhc.com.cn](http://www.r4isdhc.com.cn).  

## FAQ
### 3DS/DSi
**Q (Utilisateur Linux) :** Pourquoi Forwarder3-DS ne démarre pas ?  
**A :** JavaFX n’est pas installé. Installez JavaFX.  

**Q :** Comment fixer l’erreur "could not find or load main class com.olmectron.forwarder.Forwarder3DS"  
**A :** Vous avez besoin d’installer JavaFX version 8. (merci [@Cosmopool](https://gbatemp.net/members/530923/))  

**Q (Utilisateur 3DS) :** Je ne reçois pas de `CIA`, juste un fichier `.nds`. Pourquoi ?  
**A1 :** Parce que vous utilisez un PC x86. La build make_cia inclus ne fonctionne pas sur les PC x86, il ne marche que sur les PC x64.  
Si vous voulez toujours faire tourner des jeux DS, suivez [ce guide](https://wiki.ds-homebrew.com/ds-index/3ds-forwarders) (pour 3DS), ou utilisez [TWiLight Menu++](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/) à la place.   
**A2 :** Le nom de la ROM est peut-être trop long. Essayez de le raccourcir.  
**A3 (Utilisateur Linux et MacOS) :** `make_cia` n’a pas les droits nécessaires. Exécutez `chmod +x make_cia` dans le terminal sur le répertoire `.jar` pour que `make_cia` ai les droits nécessaires pour être exécuté.  

**Q :** En cliquant sur le bouton pour générer un raccourci, aucune fenêtre ne s’affiche. Comment fixer ça ?  
**A :** Malheureusement, je ne sais pas comment fixer ça.  
De nouveau, si vous voulez tout de même jouer à des jeux DS, suivez [ce guide](https://wiki.ds-homebrew.com/ds-index/3ds-forwarders) (pour 3DS), ou utilisez [TWiLight Menu++](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/) à la place.   

**Q :** L’icône pour le raccourci DSiWare ne s’anime pas. Comment fixer ça ?  
**A :** Utilisez NDSForwarder sur votre 3DS au lieu de Forwarder3-DS pour créer les raccourcis.  

**Q :** Pourquoi la bannière/titre est vide ?  
**A :** Vérifiez que le nom des `.nds` de vos ROM sont courts et/ou créez un dossier Forwarder3-DS dans la racine de votre disque dur (ou clef usb) et exécutez le fichier `.jar` dedans.  

**Q :** Comment je supprime les raccourcis blancs ?  
**A (DSi) :** Utilisez TMFH pour supprimer les raccourcis.  
**A (3DS) :** Dans FBI, supprimez les titres commençant par "00048004".  

**Q :** Comment mettre à jour les modèles de raccourcis ?  
**A :** L’application met à jour automatiquement les modèles si ils sont mis, ou vous pouvez cliquer sur le bouton à côté du titre Forwarder3-DS et cliquer sur “Update templates”.  

**Q :** Comment se débarrasser des lag dans les jeux ?  
**A :** Tenez A avant que l’écran de chargement de la DS apparaisse, ou ouvrez `sd:/nds/ntr_forwarder.ini` (`sd:/_nds/nds-bootstrap.ini` pour utilisateur de carte SD) et mettez NTRCLOCK (BOOST_CPU pour `nds-bootstrap.ini`) sur 0 (1 pour `nds-bootstrap.ini`) afin d’utiliser la fréquence d’horloge de TWL.  

**Q :** Pourquoi certains de mes raccourcis n’apparaissent pas ?  
**A :** Vous êtes passé au-dessus de la limite de 40 jeux pour DSiWare. Copiez les DSiWare/raccourcis que vous n’utilisez pas vers votre carte SD et supprimez-les de la mémoire système.  
Alternativement, utilisez YANBF pour créer des raccourcis.  

**Q (Utilisateur 3Ds) :** Est-ce que le jeu auquel je joue va s’afficher dans le Journal d’Activité ?  
**A :** Oui !  

**Q :** Pourquoi est-ce que j’arrive sur un menu de sélection de ROM ?  
**A :** Vérifiez que "Games are on SD card" était coché et que vous avez glissé/déposé les ROMs de la carte SD de la flashcard dans la fenêtre de Forwarder3-DS.  

**Q :** Est-ce que je peux faire tourner des jeux DSi-Enhanced dans la DSi en mode flashcard ?  
**A :** Na, ce n’est pas possible, compte tenu que les flashcards ne tournent qu’en mode DS.  

**Q :** Comment utiliser des codes de triche ?  
**A :** Utilisez un programme appelé [DSATM](https://drive.google.com/file/d/1w_W2TXUVYGb1-4OnxzOV8DKyh9Ecsh7W/view), ou utilisez [TWiLight Menu++](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/) au lieu des raccourcis.  

**Q :** J’ai un écran du haut noir et un écran du bas blanc, ou un écran noir avec un message d’erreur “Start failed”. Comment je fixe ça ?    
**A :** Vérifiez que “Automatically set ROM path” est activé, et que la ROM a été glissée depuis la carte SD (et pas le PC) dans Forwarder3-DS en faisant vos raccourcis.   
Si vous avez déjà fait ça, alors re-téléchargez le paquet de raccourci SD.  
Si vous avez déjà fait ça, alors vérifiez qu’il a un dossier `saves` dans la location de la ROM ayant le raccourci.  
Si rien ne marche, alors utilisez [TWiLight Menu++](https://gbatemp.net/threads/ds-i-3ds-twilight-menu-gui-for-ds-i-games-and-ds-i-menu-replacement.472200/) à la place.  

### Flashcards
#### R4 DS/M3 DS Simply, R4iDSN/Acekard RPG/R4i Gold RTS:
**Q :** Pourquoi certains jeux ont des écrans blancs ?  
**A :** Les raccourcis sont basés sur une ancienne version de Wood, qui a eu son code source trouvé. La version utilisée a une mauvaise compatibilité avec certains jeux. Ouvrez `_wfwd/wfwd.ini`, et mettez `useLatestWood` en 1.  

#### DSTT/R4i Gold/R4i-SDHC/R4 SDHC Dual-Core/R4 SDHC Upgrade/SC DSONE, M3DS Real:
**Q :** Pourquoi mon jeu freeze des fois ?  
**A :** Le jeu a un système d’Anti-Piratage. YSMenu est censé fixer ça, mais ne le fait pas pour une raison inconnue.  

**Q :** Lancer le CIA m’amène juste au menu de sélection de ROM. Comment je fixe ça   
**A :** Supprimez ou renommer les fichiers YSMenu.ini existants dans les dossiers/répertoires de YSMenu et de la racine.  

**Q :** Comment je saute au menu de sélection de ROM ?  
**A :** Quand vous lancez YSMenu, tenez B pour aller au menu de sélection de ROM.  

**Q :** Pourquoi j’ai :  
`[Rom Loading failed]  
load rom errcode=-  
Please reset system.`  
**A :** Regardez le [guide de codes d’erreur de YSMenu](https://gbatemp.net/threads/ysmenu-error-code-guide.179377/).
