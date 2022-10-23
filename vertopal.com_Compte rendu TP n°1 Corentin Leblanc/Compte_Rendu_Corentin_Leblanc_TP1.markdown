**Compte rendu TP n°1 : Prise en main de Shell**

**<ins>Manuel :</ins>**

1 -- Le rôle de la commande « **which** » est de localiser une commande.

2 -- Lors de la consultation d'une page du manuel, on peut rechercher un
terme grâce à la commande « **man which --k mot_cherché** » ou en se servant de "**/option**".

3 -- On peut quitter le manuel en appuyant sur la touche « **q** ».

4 -- Cette section parle de « Jeu » comme on peut le constater grâce à
la capture d'écran ci-dessous(man 6 intro).

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image1.png)

**<ins>Navigation dans l'arborescence des fichiers :</ins>**

Ci-dessous on retrouvera les différentes étapes à réaliser dans le TP.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image2.png)

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image3.png)

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image4.png)

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image5.png)

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image6.png)

Nous n'avons pas la permissions d'accéder à ce dossier.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image7.png)

La commande « **sudo cd /root** » n'est pas reconnue. C'est une commande
intégrée du shell, elle ne peut pas être directement exécutée. Rien ne
peut être inscrit devant « **cd** ». La commande "**sudo**" ne s'applique pas aux primitives du Shell.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image8.png)

A partir du dossier personnel, j'ai donc créée l'arborescence demandée.
Je me suis servis des commande « **mkdir nomdudossier** » pour les
dossiers et « **touch nomdufichier** » pour les fichiers.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image9.png)

Je ne peux pas supprimer « **Fichier1** » car c'est un dossier.

La commande qui permet de supprimer un dossier se nomme « **rmdir
nomdufichier** », il faut par contre que le dossier soit vide ou "**rm -r**" si le dossier n'est pas vide.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image10.png)

Lorsque l'on applique cette commande à Dossier2, ce n'est pas possible
car c'est un répertoire.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image11.png)

Voici comment supprimer en une seule commande Dossier2 et son contenu.
Le paramètre « **-R** » est ici pour supprimer les fichiers/dossiers
récursifs (qui se trouve à la suite du chemin). La commande "**rm -rf Dossier2**" est également valable.

**<ins>Commandes importantes :</ins>**
1 -- La commande « **date** » permet d'afficher l'heure. La commande
« **time** » permet de voir le temps réel, le temps de l'utilisateur
et le temps du système. Les deux dernières données peuvent être
modifié alors que le temps réel ne peut être modifié.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image12.png)

2 --![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image13.png)
On peut donc en déduire que les
fichiers commençant par un point sont des fichiers cachés.

3 -- Le programme ls se situe dans « **/usr/bin/ls** ».

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image14.png)

> 4 -- Voilà le résultat de la commande « **ll** ». Il n'existe pas
> d'entrée de manuel pour cette commande. La commande « alias ll » m'a
> permis d'en savoir plus sur la nature de celle-ci, on constate que
> c'est un dérivé de la commande « **ls** » mais avec des options
> supplémentaires. C'est un alias ou un raccourci pour la commande "**ls -alF**"
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image15.png)
>
> 5 -- La commande qui permet d'afficher les fichiers contenus dans le
> dossier **/bin** est « **ls /bin** ». Je peux faire cette commande
> même sans être dans le répertoire **/bin** car elle est dans les
> chemins de variables locales **\$PATH**.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image16.png)

> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image17.png)
> 
> 6 -- La commande « **ls ..** » permet de visualiser ce qui se trouve
> dans le dossier qui se trouve un cran en arrière(le dossier parent).
>
> 7 -- La commande qui donne le chemin complet du dossier courant est
> « **pwd** » (Path Work Directory).
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image18.png)
>
> 8 -- La commande « **echo 'bip' \> plop** » exécutée deux fois va
> écrire bip une première fois dans un fichier nommé « **plop** » puis
> va écraser le dernier bip et l'écrire à nouveau, il n'y aura donc qu'un bip dans le fichier.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image19.png)
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image20.png)
> 9 -- La commande « **echo 'bip' \>\>
> plop** » exécutée deux fois va cette fois ci écrire un deuxième bip à
> la suite du premier du fait de l'apparition d'un deuxième chevron.
>
> 10 -- La commande « **sleep 10 \| echo 'toto'** » affiche dans un
> premier temps le toto puis ensuite attend 10 secondes avant de nous
> rendre la main, le pipe n'attend donc pas la fin de la première commande pour commencer à traiter la deuxième.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image21.png)
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image22.png)
> 11 -- La commande file sert à déterminer le type d'un fichier.
>
> 12 -- On constate que si l'on modifie le contenue du fichier
> **original** alors le contenue du fichier **lien_phy** va lui aussi
> changer. Le fichier **lien_phy** existe toujours même si on supprime
> le fichier **original**. Ainsi lien_phy permet encore d'accéder au fichier car c'est un lien physique
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image23.png)
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image24.png)
>
> 13 -- Après modification du contenu du fichier **lien_phy**, la
> modification se fait également sur le fichier **lien_sym**. Après
> suppression du fichier **lien_phy**, le fichier **lien_sym** n'est
> plus accessible comme en témoigne la capture d'écran ci-dessous car c'est un lien symbolique.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image25.png)
>
> 14 -- Les raccourcis clavier qui permettent d'interrompre et reprendre
> le défilement à l'écran sont « **CTRL + S** » pour interrompre le
> défilement d'un fichier trop volumineux et « **CTRL + Q **» pour
> reprendre le défilement.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image26.png)
> 
> 15 -- Je me suis servi de la commande
> « **head -5 /var/log/syslog** » pour afficher les 5 premières lignes,
> « **tail -15 /var/log/syslog** » pour afficher les 15 dernières lignes
> et enfin un mélange des deux pour afficher les lignes de 10 à 20,
> « **tail -0 /var/log/syslog \| head -20 /var/log/syslog** »
> ou encore "**head -20 /var/log/syslog | tail -11**".
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image27.png)
> 
> 16 -- La commande « **dmesg \|less** »
> permet d'afficher le contenu du buffer(message) du noyau, je n'ai cependant pas
> la permission de voir son contenu. L'option less permet d'afficher
> page par page.
>
> 17 -- Le fichier **/etc/passwd** contient les noms d'utilisateurs, les
> mots de passes cryptés et le numéro d'identification d'utilisateur. La
> commande « man passwd » permet d'accéder à la page de manuel de ce
> fichier, plus précisémentà la section 5("**man 5 passwd**").
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image28.png)
>
> 18 -- Voici la commande qui permet d'afficher seulement la première
> colonne triée par ordre alphabétique inverse. Je me suis servis de la
> commande awk avec notamment comme paramètre le « **-F:** », les deux
> points délimitant les colonnes. Le « **\$1** » est pour afficher la
> première colonne uniquement et le « **sort --r** » pour trier dans
> l'ordre alphabétique inverse. Autre solution avec la commande "**cut -d: -f1 /etc/passwd | sort -r**".
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image29.png)
>
> 19 -- La commande qui nous donne le nombre d'utilisateurs ayant un
> compte sur cette machine est « **compgen --u** ». Autre solution avec la commande "**wc -l /etc/passwd**"
> qui va compter le nombre de lignes du fichier /etc/passwd et donc le nombre de users)
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image30.png)
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image31.png)
>
> 20 -- Grâce à la commande « **man --k conversion \| wc --l** » j'ai pu
> obtenir le nombre de pages de manuel comportant le mot clé conversion
> dans leur description.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image32.png)
>
> 21 -- Pour trouver tous les fichiers se nommant **passwd** présent sur
> la machine j'utilise la commande « **find / -name 'passwd'** ».
>
> 22 -- Pour enregistrer la liste des fichiers trouvés dans le fichier
> nommé « **\~/list_passwd_files.txt** », je me suis servi de la
> commande « **find / -name \'passwd\' 2\>&1
> \~/list_passwd_files.txt** » et pour rediriger les erreurs dans un
> fichier spécial **/dev/null** j'ai utilisé la commande « **find /
> -name \'passwd\'2\> /dev/null** ». Autre solution avec la commande 
> "**find / -name passwd 1> ~/list_passwd_files.txt 2> /dev/null**".
>
> 23 -- Pour chercher ou est défini l'alias ll vu précédemment, j'ai
> utilisé la commande « **grep --r ls --alF \*** » ou encore "**grep -r "alias ll"**".
>
> 24 -- Voici l'utilisation de la commande « **locate** » pour trouver
> le fichier qui se nomme **history.log**.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image33.png)
>
> 25 -- J'ai commencé par créer un fichier dans mon dossier personnel
> puis j'ai utilisé **locate** pour le trouver. Il n'apparaît pas car il n'est pas encore indexé dans la base 
> de données. L'indexation peut être forcé avec la commande "**updatedb**".
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image34.png)

Remarque : La commande « **rm** » ne marche pas avec des tuyaux (\|) (en
entrée standard). Il faut donc se servir de la commande xarg.

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image35.png)

**<ins>Exercice 3. Découverte de l'éditeur de texte nano</ins>**

1 -- Pour copier le fichier /var/log/syslog dans mon dossier personnel
sous le nom de log.txt j'ai utilisé la commande « **cp /var/log/syslog
log.txt** » puis « **nano log.txt** »

![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image36.png)

2 -- J'ai ensuite utilisé le Ctrl + W puis Ctrl + R pour trouver le mot
à remplacer. J'ai ensuite renseigné le mot à remplacer et le mot qui le
remplace.

3 -- J'ai sélectionné les 10 premières lignes grâce à Maj.Gauche +
Flèche du bas, puis Ctrl + K pour couper ces lignes. Je suis allé à la
fin du fichier puis fait Ctrl + U pour coller le résultat.

4 -- Pour annulez cette action j'ai utilisé Alt + U.

5 -- Pour quitter puis enregistrer le fichier, j'ai utilisé le Ctrl + X
et j'ai appuyé sur la touche Y.

**<ins>Exercice 4. Personnalisation du shell</ins>**

> 1 -- J'ai créé une copie de ce fichier grâce à la commande « **cp
> \~/.bashrc .bashrc_bak** »
>
> 2 -- J'ai décommenté la ligne « **force_color_prompt=yes** » puis
> enregistrer et quittez le fichier nano.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image37.png)
>
> 3 -- Voilà le résultat après l'exécution de la commande « source
> .bashrc », la couleur de l'invite de commande à bien changer.
>
> ![](vertopal_b96c91bea8414a4097a9c39cc1082c93/media/image38.png)
>
> 4 -



Correction Annales:

![image](https://user-images.githubusercontent.com/104362418/197400383-16c13a9a-9fdd-4ba2-9a8d-58c00d35e0a3.png)

"**Unzip < copies.zip 2>> /var/log/syslog | analyse 2> erreurs.analyse.log | correction 2> erreurs_correction.log | tee notes.csv | moyenne**"
