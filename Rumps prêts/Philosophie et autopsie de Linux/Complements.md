
# Compléments

## L'histoire de Linux en moins bâclé

### Multics

En 1964, les OS sont encore très rudimentaires et peu performants. L'Université
du MIT et les [laboratoires Bell](https://en.wikipedia.org/wiki/Bell_Labs), se
mettent à créer un nouveau système d'exploitation sensé révolutionner le marché

Il faut dire que ce partenariat a les moyens de faire des recherches aboutis
pour développer cet OS qui se nommera
"[Multics](https://en.wikipedia.org/wiki/Multics)" en référence à sa capacité à
supporter du multitâche.

Malheuresement Multics se révèlera assez peu populaire en raison d'un code trop
complet et trop complexe.

Les laboratoires Bell finiront par se détacher du projet. Deux chercheurs,
[Ken Thompson](https://en.wikipedia.org/wiki/Ken_Thompson) et
[Dennis Ritchie](https://en.wikipedia.org/wiki/Dennis_Ritchie) des laboratoires
Bell relèvent les problèmes de Multics et décident de développer leur propre
OS, [Unix](https://en.wikipedia.org/wiki/Unix).

### Unix

Unix est un franc succès, il arrive à convaicre par sa simplicité et surtout il
est écrit en C (langage crée par le duo de chercheurs au passage) pour sa v4. Il
utilisable sur presque machine, ce qui lui permettra sa grande popularité.

Au départ, Unix n'est pas vraiment un projet officiel. Il souvent fourni à bas
prix aux universitaires, souvent avec le code source pour pouvoir l'étudier.

Ce n'est que plus tard que Unix deviendra un logiciel très onéreux et son code
source protégé. Entre temps, les universitaires ont encore le code source
jusqu'à la version 5 d'Unix. C'est ainsi que quelques chercheurs développeront
d'ailleurs BSD, version dérivée de cette version d'Unix pour la recherche.

### Linux

Linus Torvalds est alors un étudiant briant en Finlande. Il est habitué depuis
un très jeune âge à programmer des ordinateurs. Son professeur d'informatique
code Minix, un dérivé de Unix pour permettre à ses étudiant de l'étudier.

Linus achète alors un ordinateur avec toute ses économies mais se trouve très
vite limité par Minix. Comme Unix est très onéreux, Minix très limité et DOS
lui aussi assez cher, il ne lui reste plus qu'à développer son propre OS. Il
créera alors un petit projet qu'il laissera en ligne pour recueillir les
commentaires.

Son système d'exploitation s'inspire de Unix mais n'en est pas dérivé. Ce sont
bien deux entités différentes.

C'est ici le point de départ de Linux.

Pour en savoir plus allez voir ce [documentaire](https://youtu.be/79_IMeks4wY),
vraiment allez voir ça, c'est un peu vieux mais vraiment bien fait.

## "Tout est un fichier"

Comme nous l'avons vu, ce précepte est centrale dans la conception de Linux.
Il part du principe que tout est une suite de bytes et que donc tout peut
être apparenté au même protocole. Cela offre toute la flexibilité à Linux pour
s'installer absolument partout et être facilement utilisable une fois ce que
l'on a compris ce que cela veut dire.

### Exemple d'application de ce principe

Quand vous executez n'importe quel programme, vous pouvez retrouver son PID
dans `/proc`. Si vous listez avec `ls -l /proc/<PID>` vous pourrez alors
constater que c'est un répertoire donc vous pouvez y aller avec `cd`.
A l'intérieur de ce repértoire vous retrouverez tout les attributs de votre
programme. Avec `ls -l /proc/<PID>/cwd` vous allez pouvoir trouver où le
programme a été executé et avec `ls -l /proc/<PID>/exe` vous donnera le chemin
vers le programme.

Dans `/dev` vous pouvez retrouver vos périphériques et quelques autres fichier
intéressants comme stdin, stdout, stderr qui doivent vous rappeller vos cours
de C. Si vous essayez de voir le type de fichier de vos périphérique avec
`ls -l`, vous observez que le type est Block. Ainsi vous pouvez manipuler ces
fichiers Block pour les utiliser.

En somme, vos répertoires sont des fichiers, vos processus sont des fichiers,
vos périphériques sont des fichiers : absolument tout est des fichiers.

## Architecture de fichiers

Ici on va lister les répertoires que l'on trouve à la racine de Linux et leur
utilité.

| Nom      | Utilité                                                          |
| -----    | ---------------------------------------------------------------- |
| /proc    | Retrouvez l'ensemble des processus en cours sur votre machine ici|
| /root    | Il n'y a rien pour vous ici. C'est le home du superutilisateur.  |
| /etc     | Retrouvez les fichiers de configuration de tout vos programmes.  |
| /var     | Contient des fichiers voué à grandir (logs, crash reports, etc)  |
| /boot    | Ici réside votre bootloader,vous ne voudriez pas le blesser, non?|
| /mnt     | Vide. Vous pouvez y monter vos clef USB ou autres si besoin.     |
| /usr     | Trouvez tous les binaires, bibliothèques, documentation, etc...  |
| /sys     | Trouvez ici des informations sur votre système (batterie, etc...)|
| /srv     | Vous y trouverez pour vos données serveurs (http, etc...)        |
| /run     | Dossier sur la ram, permet de laisser des informations sur procs |
| /dev     | Retrouvez tout vos périphériques et stdin, stdout et stderr.     |
| /opt     | Mettez y les programmes que vous installez vous-même.            |
| /home    | On retrouve ici les répertoires personnels de vos utilisateurs.  |
| /tmp     | Répertoire poubelle, jetez y tout et tout disparaîtra au reboot. |
| /lib(64) | Répertoires avec des bibliothèques dedans. Vous n'y touchez pas !|
| /bin     | On y trouve les programmes les plus basiques de Linux (cat, ...) |
| /sbin    | Programmes basique pour la réparation du système (en user root)  |
| /media   | Pareil que /mnt mais plus utilisé par les systèmes par défaut    |

## Sources

- [Linux wikipédia](https://en.wikipedia.org/wiki/Linux)
- [Linux n'est pas Unix ! L'histoire et l'origine des deux OS](https://youtu.be/baxmRgeX7-E) - Cocadmin
- ["Everything is a file" in UNIX](https://youtu.be/dDwXnB6XeiA) - Stevie Jay
- [Nom de code Linux [FR] - DOCUMENTAIRE](https://youtu.be/79_IMeks4wY)
