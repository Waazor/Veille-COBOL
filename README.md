# Veille-COBOL

# ~~Pourquoi avoir choisi ce langage~~ | Pourquoi ce langage est il interessant ?

Je n'ai pas pu choisir de technologie car j'étais absent durant le cours, le COBOL m'a donc été défini par défaut. Donc, au lieu d'expliquer pourquoi j'ai "choisi" cette technologie, il était plus intéressant de définir en quoi il est pertinent.

- Un langage historique 
- Un langage très utilisé
- Un langage très demandé 
- Un langage robuste et fiable
- Un langage très efficace pour la manipulation de données/calcul à virgule fixe
- Un langage avec des règles de formatage assez spéciales et très structuré 

Cependant, à chaque fois que j'ai pu entendre parler de ce langage, l'avis était toujours négatif.

## Pourquoi est-il historique ? 

**COBOL** ou **CO**mmon **B**uisness **O**riented **L**anguage est créé par une communauté d'organisations gouvernementales et commerciales (CODASYL) en 1959/1960. Il est basé sur [FLOW-MATIC](https://fr.wikipedia.org/wiki/FLOW-MATIC) et [COMTRAN]("https://en.wikipedia.org/wiki/COMTRAN"). Ce langage était l'un des plus (voire le plus) utilisé  dans les années 60 à 80. IBM est le principal fournisseur de solution COBOL.

## Pourquoi est-il toujours très utilisé ?

Il est principalement utilisé dans les secteurs bancaires, assurances et administratifs de grandes échelles. Comme dit précédemment, il était un des langages majeurs des années 60 à 80. Les entreprises (principalement les banques/assurances) datant ayant commencé leurs programmes informatiques l'utilisent toujours. Le secteur dépend donc **GRANDEMENT** du COBOL.

## Pourquoi est il autant critiqué ? 

Il est très critiqué car il est perçu comme : 
- Ancien (les nouvelles entreprises ne l'utilisent pas et COBOL utilise des systèmes anciens : [mainframes](https://www.ibm.com/fr-fr/topics/mainframe#:~:text=Un%20mainframe%20sert%20de%20serveur,virgule%20flottante%20en%20une%20seconde.))
- Rigide 
- Très verbeux dû à sa ressemblance à l'anglais (300 à 400 mots réservés COBOL avec parfois le même usage)

## Malgrès tous ses défauts, pourquoi est il très demandé ? 

Il est très demandé aujourd'hui malgré tout, car une grande partie des entreprises ayant développé leurs programmes informatiques durant les années de rayonnement du COBOL n'ont pas migré vers des technologies plus récentes, dû à la difficulté de portage du COBOL (architecture très monolithique). Cependant, la communauté COBOListe est très vieillissante (départ à la retraite des experts), car peu de nouveaux développeurs cherchent à apprendre le COBOL (difficile et peu attrayant). La demande commence donc à être bien plus grande que le nombre de nouveaux développeurs COBOL.

## En quoi est-il robuste et fiable ? 

Sa grande rétrocompatibilité le rend assez fiable et il est particulièrement performant pour gérer de grands volumes de transactions et possède un excellent système pour des calculs avec virgule fixe (!=Float) dout sa bonne aptitude pour les anciennes assurances et banques.

## Ses spécificités dans sa structure/formatage

Il est très verbeux et similaire à l'anglais, car il devait être facilement compréhensible à l'époque de sa création, dont par l'armée.

A la base, ce langage était écrit sur des cartes perforées à 80 colonnes (1 carte perforée = 1 ligne de code).

Ce principe de formatage et de 80 colonnes a été garder même après l'usage et le développement via clavier. Chaque instructions doit se finir par un "." et une variable est défini par PIC ou PICTURE et par valeur de hiérarchisation (de 01 à  49 ou par 77)

Les lignes d'un programme COBOL se structures ainsi : 

| Colonne | Utilisation | 
| ------- | ---------- |
|1 - 6 | Numéro de ligne (optionnel, souvent ignoré dans les compilateurs modernes) |
| 7 | Indicateur spécial (* pour un commentaire, / pour un saut de page, - pour une continuation de ligne) |
| 8 - 11 | Zone A (mots-clés principaux comme DIVISION, SECTION, PARAGRAPH) |
| 12 - 72 |Zone B (instructions COBOL) |
| 73 - 80 | Zone de numérotation (souvent utilisée pour l’identification du programme sur cartes perforées, généralement ignorée aujourd’hui) |

Un programme COBOL est divisé par Division : 

| Division | Rôle |
| -------- | ---- |
| IDENTIFICATION DIVISION | Décrit le programme (nom, auteur, date, etc). |
| ENVIRONMENT DIVISION | Définit l’environnement d’exécution (fichiers, configuration). |
| DATA DIVISION | Contient la déclaration des variables et structures de données.
| PROCEDURE DIVISION | Contient la logique du programme (instructions, traitements). |

Voici un Hello World en COBOL que j'ai pu faire sur [Exercism](https://exercism.org/dashboard) pour montrer un exemple : 

```
      * Voici une ligne de commentaire
       IDENTIFICATION DIVISION.
       PROGRAM-ID. hello-world.
       DATA DIVISION.
       WORKING-STORAGE SECTION.
       01 WS-RESULT PIC X(14).
       PROCEDURE DIVISION.
       HELLO-WORLD.
        MOVE "Hello, World! " TO WS-RESULT.
```

# Lien de veille pour cette technologie :

## Informations sur COBOL :

| n° | Lien | Justification |
| --------- | ------- | -------- |
| 1 | [Wikipédia] (https://en.wikipedia.org/wiki/COBOL) | Avoir des informations basiques sur le langage pour bien le comprendre (version anglaise car plus complète) |
| 2 | [YTB : Underscore_ Interview COBOListe](https://www.youtube.com/watch?v=R2B2QetWGag) | Podcast de Micode interviewant un "Jeune" expert de COBOL, ils parlent du COBOL en général (fonctionnement, début) + commentaire donnant leurs expériences |
| 3 | [IBM : début ](https://www.ibm.com/fr-fr/topics/cobol) | IBM étant le fournisseur COBOL le plus présent sur le marché, leur définition/explication de COBOL est très pertinente |
| 4 | [YTB : PODCAST COBOLISTE](https://www.youtube.com/watch?v=MaEneyo6bRY) | Podcast entre un expert et un néophyte COBOL |

## Apprendre à développer en COBOL

| n° | Lien | Justification |
| --------- | ------- | -------- |
| 1 | [Cours COBOL CSIS] (https://www.csis.ul.ie/cobol/) | Cours en anglais COBOL principalement théorique (site datant un peu mais utilisable) |
| 2 | [Curs COBOL Mainframes tech help](https://www.mainframestechhelp.com/tutorials/cobol/introduction.htm) | Cours COBOL hyper complet basé sur la théorie |
| 3 | [Exercism] (https://exercism.org/tracks/cobol) | Site de cours de langage de programmation pratique (je l'utilise aussi pour d'autres langages) |


## Communautés :

Les COBOListes étant une communauté plus vieille et moins "geek" que les autres, il est assez dur de trouver des communautés sérieuses sur les réseaux sociaux comme Discord ou Twitter

| n° | Lien | Justification |
| --------- | ------- | -------- |
| 1 | [Reddit r/cobol](https://www.reddit.com/r/cobol/) | Probablement le plus gros forum parlant de COBOL sur internet |
| 2 | [StackOverflow topic COBOL](https://stackoverflow.com/questions/tagged/cobol) | Voir toutes les questions et problèmes des développeurs COBOL |
| 3 | [Github topic COBOL](https://github.com/search?q=language%3ACOBOL&type=repositories&s=stars&o=desc) | Voir tous les projets en langage COBOL sur GitHub (triés par avis positif) |
| 4 | [LinkedIn communauté : COBOL Programmers](https://www.linkedin.com/groups/70143/) | Communauté professionelle COBOLists |
| 5 | [LinkedIn communauté : Mainframe](https://www.linkedin.com/groups/910927/) | Communauté professionnelle contenant une bonne quantité de COBOLists |
| 6 | [Forum GnuCOBOL](https://sourceforge.net/p/gnucobol/discussion/) | Forum de développement pour COBOL lié à [GnuCOBOL](https://gnucobol.sourceforge.io/) |
| 7 | [Forum Hacker news COBOL](https://hn.algolia.com/?query=cobol&sort=byDate&type=all) | Forum avec comme topic COBOL un peu fermé cherchant à parler principalement avec des experts |
| 8 | [Reddit r/mainframe] (https://www.reddit.com/r/mainframe/) | COBOL utilisant les mainframes comme système/architecture, il est aussi intéressant de regarder régulièrement ce qu'il se dit à ce sujet |
| 9 | [Discord System Z Enthusiasts](https://discord.gg/sze) | Seul discord sérieux que j'ai pu trouver parlant un minimum de COBOL |

## Outils de dev COBOL :

| n° | Lien | Justification |
| --------- | ------- | -------- |
| 1 | [GnuCOBOL](https://gnucobol.sourceforge.io/) | Transcompilateur vers C qui utilise ensuite un compilateur C pour générer du code natif permettant d'exécuter du COBOL hors d'un système [mainframe](https://www.ibm.com/fr-fr/topics/mainframe#:~:text=Un%20mainframe%20sert%20de%20serveur,virgule%20flottante%20en%20une%20seconde.). |
| 2 | [ISO/IEC 1989:2023](https://www.iso.org/standard/74527.html) | Document permettant de lister les normes de code COBOL |
| 3 | [IMB documentation du support](https://www.ibm.com/support/pages/enterprise-cobol-zos-documentation-library#Table642) | Documentation de IBM sur le COBOL |
| 4 | [Librairies VScode topic COBOL](https://docs.rocketsoftware.com/bundle?cluster=true&labelkey=prod_visual_cobol) | Répétories toutes les librairies utiles pour le développement en COBOL |
| 5 | [IA CobolCopilot](https://cobolcopilot.com/) | Une IA d'aide au CODE spécialisé COBOL |
| 6 | [COBOL-Check (tests unitaires)](https://github.com/openmainframeproject/cobol-check) | Outils pour des tests unitaires pour COBOL |
| 7 | [Wikipédia PACBASE](https://fr.wikipedia.org/wiki/Pacbase) | Permet de générer du code en COBOL via une description graphique ou textuelle spécifique à pacbase |
| 8 | [SuperBol](https://superbol.eu/) | Permet d'intégrer/exécuter du code COBOL dans d'autres environnements/applications |


## Autres et liens généraux

| n° | Lien | Justification |
| --------- | ------- | -------- |
| 1 | [Dev.to topic COBOL](https://dev.to/search?utf8=%E2%9C%93&q=COBOL) | Pleins d'articles à lire liés au COBOL (certains ne sont pas en anglais/français et n'ont pas le même degré de pertinence) |
| 2 | [Article COBOL: CloudFlare](https://blog.cloudflare.com/cloudflare-workers-now-support-cobol/) | Explique que, après une demande du New Jersey, le cobol est compilable via leurs serveurs |
| 3 | [Zeste de savoir](https://zestedesavoir.com/tutoriels/685/la-programmation-cobol/) | Site permettant d'avoir des bases sur COBOL, pas spécalisé COBOOL donc peut manquer d'infos |
| 4 | [IBM topic COBOL](https://www.ibm.com/search?lang=fr&cc=fr&q=cobol) | Encore le site IBM, mais avec tous leurs liens COBOL |
| 5 | [la communauté du COBOL] (https://www.lacommunauteducobol.com/cobol/) | Site plutôt complet lié au COBOL, il y a aussi une page FORUM mais pas hyper actif, il sert donc principalement pour de l'informatif |
| 6 | [YTBC : FromZeroToCOBOL](https://www.youtube.com/@fromzerotocobol6023) | Chaîne YouTube hyper complète sur le COBOL en général, principalement pour ses cours et explications |
