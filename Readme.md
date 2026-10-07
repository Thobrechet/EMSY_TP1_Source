# TP1 - Installation Linux sur une VM - V0.4

## Groupe 

1. Yazan (YAD) 		- Noé (NAM) 
2. Siméon (SAR) 	- Gaëtan (GFR)
3. Tristan (TCK) 	- Nicolas (NTN)
4. Matéo (MCN) 		- Thomas (TBT)
5. Noah (NRN) 		- Guillaume (GFE)
6. Benjamin (BSC) 	- Valentin (VBC)
7. Gabriel (GOM) 	- Nikola (NDC)

## But 

Cette manipulation a pour but d'installer une distribution linux [Sparky Linux](https://sparkylinux.org/) dans une machine virtuelle VMware 
Workstation Player, à l’aide d’une image disque (ISO).

## Materiels à disposition 

- VMware Workstation Player - V17
- Image disque (ISO) : sparkylinux-6.4-x86_64-minimalcli.iso

## Création d’une machine virtuelle 

**A.** Lancez VMware Workstation Player (logiciel)  

**B.** Sélectionnez **Create a New Virtual Machine** 

**C-A.** Placez le fichier `.iso` dans une repertoire connu : 

`C:\VosInitiales\VM\ISO`

**C-B.** Indiquez le chemin d’accès de l’image iso comme indiqué sous l’image ci-dessous :

![install image disk](/Images/Install_ISO.jpg) 

**D-A.** Choisissez un nom d'OS : `Linux - Debian 11.x` 

![OS name choice](Images/OS_Choice.jpg) 

**D-B.** Nommez la machine virtuelle : `SparkyLinux-VosInitiales` 

**E.** Creez un disque virtuel -> capcité : **20GB** 

> Remarque 1 : Cocher **store virtual disk a single file**

![Virtual disk](/Images/VirtualDisk.jpg) 

> Remarque 2 : Ci-dessous, la configuration de la VM 

![Virtual disk](/Images/VM_Config.jpg) 

**F.** Lancez la machine virtuelle : **Play virtual machine** 

## Lancement de l'image ISO (Linux - Live CD) 

**G.** Lancement du live CD : 

<img width="784" height="576" alt="Capture d&#39;écran 2026-09-17 154256" src="https://github.com/user-attachments/assets/2b348c4e-41fe-4fbb-9a68-d3b6d8af1745" />

Shell Linux : 
<img width="1928" height="1040" alt="Capture d&#39;écran 2026-09-17 153802" src="https://github.com/user-attachments/assets/748ce6c3-d976-4f70-97f0-e76a47f34412" />
> **ATTENTION** : par défaut, le clavier est configuré est **Clavier Americain**

Q1. disposition du clavier américain ?

querty

Q2. disposition du clavier suisse-romand ?

le clavier suisse-romand est qwertz

Q3. disposition du le clavier français ? 

azery

**H.** Déplacez-vous à la **racine du système** en utilisant la commande suivante : `cd` 

Q4. 
cd$ ou cd /

**I.** Affichez le contenu de la racine avec la commande : `ls –l`	

<img width="1928" height="1040" alt="Capture d&#39;écran 2026-09-17 162325" src="https://github.com/user-attachments/assets/dca2c307-41da-4cac-b779-640b34b426d9" />

Q5. Que signifie l'option `-l` avec la commande `ls` 

L'option -l signifie long listing. Elle permet d'afficher les fichiers et répertoires avec des informations détaillées : permissions, propriétaire, groupe, taille, date de modification

Q6. Décrypter la ligne où se trouve le répertoire **home**    

<img width="1601" height="62" alt="Capture d&#39;écran 2026-09-24 153300" src="https://github.com/user-attachments/assets/8380fc8a-a986-40b5-9f1c-7cc909d8810e" />

d → le répertoire 

rwx → droits du propriétaire

r-x → droits du groupe

r-x → droits des autres utilisateurs

3 → nombre de liens

root → propriétaire

root → groupe

4096 → taille du répertoire

Sep 24 09:00 → date et heure de dernière modification

home → nom du répertoire

**J.** Créez un répertoire de travail nommé « EMSY_VosInitiales» 

Q7. dans quel dossier racine allez-vous le placer (justifiez votre réponse) 

/home/live

home contient les répertoires personnels des utilisateurs, et live est ici le répertoire

Q8. Quelle commande allez-vous utiliser pour faire ceci ?  

mkdir EMSY_TB

**K.** Dans ce répertoire, créez un fichier texte que vous nommerez `TESTSLO_XXX_XXX` et éditez celui en écrivant un texte, exemple : "TP linux by XXX et XXX".
	   Utiliser la commande `vi`

vi TESTSLO_TBT_MCN

Q9. Pouvez-vous édit un fichier uniquement avec la commande `vi` 

Oui c'est possible

Q10. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé ci-dessus existe toujours (justifiez votre réponse) ? 

Non car les modifications sont temporaires et sont perdues lorsque la machine virtuelle est éteinte

**L.** Tapez la commande `ls -l /dev/sda` 

<img width="476" height="151" alt="image" src="https://github.com/user-attachments/assets/a76ad114-93ef-46df-a64a-688518d1b1eb" />


Q11. Que signifie **sda** ? 

sda désigne le premier périphérique de stockage de type disque

Q12. Quelle différence y a-t-il entre le répertoire de la question Q6 et celui du point L (justifiez votre réponse) ?

/home est un dossier dans lequel on peut stocker des fichiers et des dossiers, tandis que /dev/sda représente directement le disque utilisé par le système.

## Installation de SparkyLinux sur la VM

**M.** Installez SparkyLinux

![Placer vos captures d'écrans de l'installation]()

Q13. Quelle est la taille de disque minimum recommandée pour installer la distribution Sparky en mode cli 

2Go

Q14. A quoi sert la partition swap ? Est-ce que ce principe existe-t-il sur les OS Microsoft Windows ? 

une extension de ram quand cest nessesaire

Q15. Quel format pourriez-vous utiliser pour la 3ème partition afin qu’elle soit également accessible depuis un OS Microsoft ? 

fat32

Q16. Durant l’installation, on vous demande deux noms d’utilisateur. A quoi correspondent-ils ? 

le compte administrateur et le comptestandart


**N.** Une fois l’installation de Linux terminée, prenez une capture d’écran du démarrage de votre système (GRUB)

![Placer votre capture d'écran]() 

**O.** Trouvez la ou les lignes de commande permettant de changer le clavier et procédez à la configuiration 

sudo dpkg-reconfigure keyboard-configuration

<img width="856" height="623" alt="Capture d&#39;écran 2026-10-07 084028" src="https://github.com/user-attachments/assets/9fd17f6c-10ab-4a8a-873a-1b97f13206db" />

**P.** Tapez la commande : `nano -version`

<img width="487" height="88" alt="Capture d&#39;écran 2026-10-07 143321" src="https://github.com/user-attachments/assets/4fe2aa12-eff5-4363-a0bc-86888566d763" />


Q17. A quoi sert `nano` ? 
Nano est un éditeur de texte permettant de créer et modifier des fichiers directement depuis le terminal.


**Q.** Testez si l’application `git` est installée sur votre distribution, si ce n’est pas le cas installez un client git. 

Q18. Comment savoir si `git` est déjà installé ? 

en verifiant le resulat de git 

<img width="275" height="44" alt="Capture d&#39;écran 2026-10-07 143036" src="https://github.com/user-attachments/assets/704e5968-2091-49ac-86dc-139734d1b847" />


Q19. Si le client `git` n'est pas installé, quelle(s) commande(s) utilisez-vous pour l’installer ? 

sudo apt update

Q20. Que veut dire `apt` ? 

un outil de linux pour installer et télécharger des mise a jour

Q21. Est-ce que cette commande (`apt`) peut être utilisée sur toutes les distributions Linux (justifiez votre réponse)? 

non Elle est principalement utilisée sur les distributions basées sur Debian

**R.** Créez un sous-répertoire « EMSY_TP1_XXX-YYY » dans le répertoire de votre utilisateur. 
       
**Attention** : Ici on veut que l’utilisateur (vous) ait les droits de lecture, d’écriture et d’exécution.
mkdir EMSY_TP1_XXX-YYY


Q22. Quel est le répertoire utilisateur ?  

/home/brechet

Q23. Quelles sont les commandes pour changer les droits d'utilisateurs (lecture - écriture - execution) ?  

chmod u+rwx EMSY_TP1_XXX-YYYTho

**S.** Dans ce répertoire, tapez la commande : `git clone https://github.com/votreDepot/EMSY_TP1_Source`

***Remarque*** : Il faut au préalable que vous ayez mis en place à cette adresse un fork du dépôt fourni lors de ce TP.

Q24. Qu’observez-vous dans ce répertoire ?

<img width="612" height="144" alt="Capture d&#39;écran 2026-10-07 151814" src="https://github.com/user-attachments/assets/bf3871fb-a811-41dd-afeb-4d212e9f7574" />


**T.** Editez le fichier source `.c` avec l’éditeur de texte « nano ». -> Réalisez un petit programme en C (par exemple de type « Hello world »).

<img width="884" height="726" alt="Capture d&#39;écran 2026-10-07 152936" src="https://github.com/user-attachments/assets/24c491a7-f757-4b46-b86e-f6ba6205d8ea" />


**U.**	Vérifiez si le compilateur `gcc` est bien installé. Notez la version du logiciel
gcc (Debian 10.2.1-6) 10.2.1 20210110
<img width="640" height="135" alt="Capture d&#39;écran 2026-10-07 153458" src="https://github.com/user-attachments/assets/263d61fa-6f2a-4666-9fb9-c6411e9df958" />

**U-A.** Tapez les commandes suivantes :
```Shell 
gcc -Wall -o fichier.o -c fichier.c 
gcc -o fichier fichier.o 
```
Remarque : « fichier » est à remplacer par le nom de votre choix
<img width="631" height="77" alt="Capture d&#39;écran 2026-10-07 154611" src="https://github.com/user-attachments/assets/faaff7ec-293d-4ca2-bf07-e90ad4c8f80f" />


Q25. Quels sont les fichiers qui ont été générés 

EMSY_TP1 ET EMSY_TP1.c

![Placer votre capture d'écran]()

**V.** Entrez la commande suivante : `./fichier`
<img width="454" height="108" alt="image" src="https://github.com/user-attachments/assets/20b0c38e-35da-4dc2-945a-bcc883baea5a" />


Q26. Que se passe-t-il ?

le code que javais tappé c'est lancer



...A compléter...

## Tips 

> Tip 1 : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> Tip 2 :  
> Pour arrêter un Linux proprement : 	`shutdown`  
> Pour forcer l’arrêt d’un système :	`halt` ou `poweroff`  
> Seul un administrateur peut exécuter ces commandes !

> Tip 3 : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> Tip 4 : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)

