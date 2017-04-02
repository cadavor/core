Das ist der wichtigste Teil einer Haus-Automatisierung: Die Szenarien. Das ist ein richtiges Gedächnis der Haustechnik, was es ermöglicht, mit der wirklichen Welt auf "intelligente" Art zu interagieren.

Die Szenario Seite
==================

Pour y accéder rien de plus simple, il suffit d’aller sur Outils → Scénarios :

![](../images/scenario1.JPG)

Sobald sie darauf sind, sehen sie:

![](../images/scenario.JPG)

Oben findet man eine Reihe von 3 Tasten wieder :

-   **Hinzufügen** : um ein Szenario hinzuzufügen

-   **Szenarien deaktivieren** : um alle Szenarien zu deaktivieren

-   **Variablen anzeigen** : erlaubt die Variablen zu sehen, ihren Wert und den Ort, wo sie verwendet werden

> **Tip**
>
> Die Szenarien in rot sind diejenigen, die deaktiviert sind

> **Tip**
>
> Wie an vielen Orten auf Jeedom, wenn man die Maus ganz nach links bewegt ermöglicht es, ein Schnellzugangsmenü sichtbar zu machen(Sie können es in ihrem Profil immer sichtbar machen).

Es gibt 2 Szenario Modi :

-   **Simple** : permet de faire des scénarios très simples type SI ça ALORS fait ça

-   **Fortschrittlich** : Sie können alles tun, aber es erfordert mehr wissen

Es ist möglich, ein Szenario von einfachen Modus zum erweiterte Modus zu übergeben, aber nicht umgekehrt

Beim Erstellen eines Szenario wird Jeedom nach den Namen und den Typ fragen :

![](../images/scenario2.JPG)

Einfacher Modus
===============

Dies ist der Modus "Einfaches-Interface" :

![](../images/scenario9.JPG)

Hier finden Sie :

-   **Name** : Der Name des Szenarios

-   **Beschreibung** : Sie können eine Beschreibung hinzufügen, was das Szenario macht und zum Beispiel Überwachung

-   **Actif** : définit si le scénario est actif ou non

-   **Exécuter en avant plan** : permet de lancer le scénario directement et non dans un fil d’exécution séparé. Attention cette option peut être dangereuse car elle met en pause toutes les autres actions du scénario. IL NE FAUT JAMAIS l’activer sur un scénario déclenché par une programmation horaire

-   **Dernier lancement** : la date de dernière exécution du scénario

-   **Zustand** : der aktuelle Zustand des Szenarios (laufend, angehalten…)

Oben rechts finden wir :

-   eine Schaltfläche, um einen Text-Export des Szenarios zu machen (praktisch, um es auf dem Forum oder dem Supportteam zu zeigen)

-   eine Schaltfläche, um ein Protokoll des Szenarios zu haben

-   eine Schaltfläche, um das Szenario zu Kopieren

Unten links auf der Seite haben Sie die Ausführungsbedingung des Szenarios :

-   **Szenario** : um anzuzeigen, ob das Skript programmiert (an einer bestimmten Uhrzeit und Datum) oder wenn sie verursacht wird (Wie die Erfassung der Bewegung)

-   **A exécuter** : en mode programmé permet de dire s’il doit être exécuté une fois ou de manière répétée

-   **Datiert** : wenn es nur einmal ausgeführt wird, dann müssen sie das Datum und die Uhrzeit eingeben

-   **Häufigkeit** : im Mehrmals Modus können Sie die Wiederholungsfrequenz wählen

![](../images/scenario10.JPG)

-   **Von** : Im verursacht-Modus können Sie den Befehl der das Szenario auslöst auswählen, indem Sie auf den kleinen Knopf rechts klicken

![](../images/scenario11.JPG)

-   **Condition optionnelle** : permet d’activer ou non un test avant l’exécution du scénario.

![](../images/scenario12.JPG)

-   **Wenn** : Damit können sie die Reihenfolge in der die Bedingung erfüllt ist wählen, indem Sie auf den kleinen Knopf auf der rechten Seite klicken

-   **Ist** : Sie können den Status wählen, der der vorherige Befehl haben muss, damit die Aktion (gemäß den Befehlen können die Optionen wechseln) ausgeführt werden soll

Schließlich, auf der rechten Seite haben Sie die Aktion, hier genügt es einfach "Aktion hinzufügen" anzuklicken

Beispiel, auf Anwesenheit einzuschalten
---------------------------------------

![](../images/scenario13.JPG)

Dies ist ein sehr einfaches Szenario, das schaltet das Licht bei Anwesenheit an

> **Tip**
>
> Ce scénario sera déclenché aussi bien lors de la détection d’une présence que lors du relâchement (fin de présence), il est donc nécessaire de tester la valeur de la présence (ici déclenchée)

Vergessen Sie nicht die gleiche Art von Szenario zu machen, aber das Licht auszuschalten, wenn niemand anwesend ist

Erweiterter Modus
=================

Hier ist ein Beispielszenario im erweiterten Modus :

![](../images/scenario3.JPG)

Oben finden wir den allgemeinen Teil wieder :

-   **Name**

-   **Gruppe** : hilft Szenarien zu organisieren

-   **Aktiv** : Ob das Szenario aktiv oder inaktiv sein soll

-   **Sichtbar** : Ob das Szenario sichtbar oder nicht sichtbar sein soll

-   **Eltern-Objekt** : Die Wahl zu einem übergeordneten Objekt zugewiesen zu werden oder nicht

-   **Zeitüberschreitung Sekunden (0 = unbegrenzt)** : Die maximal erlaubte Ausführungszeit

-   **Déclencheurs** : Ensuite vient la partie des déclencheurs qui peuvent soit être un ou plusieurs événements et/ou une programmation (une heure donnée, une fréquence… Cette partie s’écrit à l’aide d’une syntaxe type crontab accessible via la touche, un assistant est disponible en cliquant sur ?. Attention vous pouvez avoir au maximum 28 déclencheurs sur un scénario.

-   **Action** : En haut à droite on retrouve quelques actions utiles comme le lancement forcé du scénario (pour test),la suppression du scénario, la sauvegarde, la génération d’un template (voir le chapitre dédié), l’export, l’arrêt forcé d’un scénario (si en cours), log des dernières exécutions (très pratique pour vérifier le déroulement exact du scénario), la duplication.

-   **Execution en avant plan** : permet de lancer le scénario directement et non dans un fil d’exécution séparé. Attention cette option peut être dangereuse car elle met en pause toute les autres actions du scénario. IL NE FAUT JAMAIS l’activer sur un scénario déclenché par une programmation horaire ou un scénario contenant des actions de type sleep

-   **Enchaîner les commandes sans attendre** : permet d’enchaîner les suites d’actions sans attendre le retour et donc la vérification de la bonne exécution (attention actuellement seuls les plugins openzwave et script sont compatibles)

-   **Pas de log** : indique au scénario de ne pas écrire dans les logs (permet de le rendre un peu plus rapide)

-   **Zustand** : aktueller Zustand des Szenarios

Im unteren Teil kommt das Szenario selbst mit einer Schaltfläche zum hinzufügen von Blöcken :

![](../images/scenario4.JPG)

-   **wenn/dann/sonst** : Grundstein für das erreichen einer Bedingung

-   **Action** : bloc permet de lancer une action simple sans aucune condition ou autre avant

-   Schleifen : ermöglicht Schleifen auf 1 definierte Nummer (oder einen Wert eines Sensors oder Zufallszahl)

-   **Dans** : permet de lancer une action dans X minute(s) (0 est une valeur possible). La particularité c’est que les actions sont lancées en arrière plan, elles ne bloquent donc pas la suite du scénario. C’est donc un bloc non bloquant.

-   **A** : erlaubt, Jeedom zu sagen, die Aktionen des Blocks A zu einer bestimmten Stunde zu starten (in der Form hhmm). Dieser Block ist nicht blockierend

-   **Code** : ermöglicht, direkt im PHP Code zu schreiben (demande certaines connaissances et peut être risqué mais permet de n’avoir plus aucune contrainte).

-   **Kommentar** : ermöglicht, Kommentare zu seinem Szenario hinzufügen

> **Tip**
>
> Devant chaque bloc (en dessous de la double flèche verticale qui permet de déplacer les blocs) vous avez un petit coche pour désactiver complètement le bloc sans pour autant supprimer celui-ci (permet de faire des tests pour le réactiver plus tard par exemple)

> **Note**
>
> Sur les blocs de type Si/Alors/Sinon vous avez devant des flèches circulaires, elles permettent d’activer ou non la répétition des actions si l'évaluation de la condition donne le même résultat que la précedente évaluation

Pour les conditions, Jeedom essaye de faire en sorte qu’on puisse les écrire le plus possible en langage naturel tout en restant souple. On a donc un bouton permettant de sélectionner un équipement puis on écrit la condition. Il existe une liste de tags permettant d’avoir accès à des variables issues du scénario ou d’un autre, à l’heure, à la date, à un nombre aléatoire….

![](../images/scenario5.JPG)

Die erste Schaltfläche erlaubt es, einen Befehl zu suchen :

![](../images/scenario6.JPG)

Sobald der Befehl ausgewählt wurde, fragt Jeedom, was Sie testen möchten:

![](../images/scenario7.JPG)

En fonction du type vous aurez différentes possibilités, vous pouvez ensuite mettre d’autres tests et les lier avec un "ou" ou un "et". Ainsi avec cet assistant vous pouvez construire votre condition.

> **Tip**
>
> Si vous cliquez sur "Ne rien mettre" Jeedom va juste écrire la commande dans le champ condition en vous laissant la main pour la suite.

Le deuxième bouton quant à lui permet d’aller chercher un scénario pour, par exemple, tester si celui-ci est en cours (voir partie "Condition ou valeur d’une commande d’action")

Pour les actions, on peut exécuter soit une action d’une commande (les options de celle-ci apparaitront sur sa droite), soit une commande d’affectation de variable ou de pause(très pratique pour simuler la présence surtout couplée à la génération d’une durée aléatoire) ou même d’action sur un autre scénario (start, stop, activer, désactiver).

Hier finden Sie die folgenden Optionen :

![](../images/scenario8.JPG)

In der Reihenfolge :

-   Schaltfläche zum Verschieben der Aktion (Doppelpfeile), klicken Sie einfach darauf und halten die Taste gedrückt und bewegen dann den Block

-   eine Schaltfläche zum Löschen der Aktion

-   eine Schaltfläche zum vorübergehenden deaktivieren der Aktion

-   eine Schaltfläche zum suchen eines Aktionsbefehls

-   un bouton pour les actions spécifiques, avec à chaque fois la description de cette action

Auslöser
--------

Es gibt bestimmte Auslöser (außer jene, die durch die Befehle geliefert wurden) :

-   **\#start\#** : löst Jeedom (neu)start aus,

-   **\#begin\_backup\#** : Ereignis, das zu Beginn des Backups gesendet wird.

-   **\#end\_backup\#** : Ereignis, das am Ende des Backups gesendet wird.

-   **\#begin\_update\#** : Ereignis, das zu Beginn des Updates gesendet wird.

-   **\#end\_update\#** : Ereignis, das am Ende des Updates gesendet wird.

-   **\#begin\_restore\#** : Ereignis, das zu Beginn der Wiederherstellung gesendet wird.

-   **\#end\_restore\#** : Ereignis, das am Ende der Wiederherstellung gesendet wird.

Vous pouvez aussi déclencher un scénario sur mise à jour d’une variable en mettant : variable(nom\_variable) ou en utilisant l’api http décrite ici : [https://github.com/jeedom/core/blob/beta/doc/fr\_FR/api\_http.asciidoc\#pilotage-des-scénarios](https://github.com/jeedom/core/blob/beta/doc/fr_FR/api_http.asciidoc#pilotage-des-scénarios)

> **Tip**
>
> Hier haben Sie auch eine Schaltfläche, um einen Befehl zu suchen

Bedingung oder Wert eines Aktionsbefehls
----------------------------------------

Sie können irgendein Symbol entsprechend für die Operatoren benutzen :

-   == : gleich,

-   \> : größer,

-   \>= : größer oder gleich

-   \< : kleiner,

-   ⇐ : kleiner oder gleich

-   != : unterschiedlich,

-   matches : contient (ex : [Salle de bain][Hydrometrie][etat] matches "/humide/" ),

-   not ( … matches …) : ne contient pas (ex : not([Salle de bain][Hydrometrie][etat] matches "/humide/")),

Sie können jede Operation mit den folgenden Operatoren kombinieren:

-   && / ET / et / AND / and : und,

-   || / OU / ou / OR / or : oder,

    -   |\^ / XOR / xor : entweder oder

Außerdem können Sie mit den folgenden Tags:

> **Tip**
>
> Ein Tag wird während der Ausführung des Skripts durch seinen Wert ersetzt.

-   **\#seconde\#** : Sekunde,

-   **\#heure\#** : Stunde (Bsp. : 17 als 17h15),

-   **\#minute\#** : Minute (Bsp. : 15 als 17h15),

-   **\#jour\#** : Tag,

-   **\#mois\#** : Monat,

-   **\#annee\#** : Jahr,

-   **\#time\#** : Stunde und Minute (Bsp. : 1715 als 17h15),

-   **\#timestamp\#** : gibt die Anzahl der Sekunden seit dem 1. Januar 1970,

-   **\#date\#** : Monat und Tag (Bsp. : 1215 als 15 Dezember),

-   **\#semaine\#** : Nummer der Woche (Bsp. : 51),

-   **\#sjour\#** : den Namen des Wochentages (Bsp. : Samstag),

-   **\#njour\#** : Nummer des Tages von 0 (Sonntag) bis 6 (Samstag),

-   **\#smois\#** : den Namen des Monats (Bsp. : Januar),

-   **\#IP\#** : Interne Jeedom IP,

-   **\#hostname\#** : Name der Jeedom Maschine,

-   **\#trigger\#** : Name des Befehls, der das Szenario auslöst.

Sie haben auch die folgenden Tags und vieles mehr, wenn Ihr Szenario durch eine Interaktion ausgelöst wurde :

-   **\#query\#** : Interaktion, die das Szenario auslöst,

-   **\#profil\#** : Profil des Benutzers, der das Skript ausgelöst hat (kann leer sein).

Lorsqu’un scénario est déclenché par une interaction, celui-ci est forcément exécuté en mode rapide.

Mehrere Funktionen sind für die Geräte verfügbar :

-   **average**(commande,période) et **averageBetween**(commande,start,end) : donnent la moyenne de la commande sur la période (period=[month,day,hour,min] ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php)) ou entre les 2 bornes demandées (sous la forme Y-m-d H:i:s ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

    -   Ex : average(\#[Salle de bain][Hydrometrie][Humidité]\#,1 hour) : renvoie la moyenne de la commande sur la dernière heure

    -   Ex : averageBetween(\#[Salle de bain][Hydrometrie][Humidité]\#,2015-01-01 00:00:00,2015-01-15 00:00:00) : renvoie la moyenne de la commande entre le 1 janvier 2015 et le 15 janvier 2015

-   **min**(commande,période) et **minBetween**(commande,start,end) : donnent le minimum de la commande sur la période (period=[month,day,hour,min] ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php)) ou entre les 2 bornes demandées (sous la forme Y-m-d H:i:s ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

    -   Ex : min(\#[Salle de bain][Hydrometrie][Humidité]\#,15 min) : renvoie le minimum de la commande sur les 15 dernières minutes

    -   Ex : minBetween(\#[Salle de bain][Hydrometrie][Humidité]\#,2015-01-01 00:00:00,2015-01-15 00:00:00) : renvoie le minimum de la commande entre le 1 janvier 2015 et le 15 janvier 2015

-   **max**(commande,période) et **maxBetween**(commande,start,end) : donnent le maximum de la commande sur la période (period=[month,day,hour,min] ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php)) ou entre les 2 bornes demandées (sous la forme Y-m-d H:i:s ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

    -   Ex : max(\#[Salle de bain][Hydrometrie][Humidité]\#,7 day) : renvoie le maximum de la commande sur les 7 derniers jours

    -   Ex : maxBetween(\#[Salle de bain][Hydrometrie][Humidité]\#,2015-01-01 00:00:00,2015-01-15 00:00:00) : renvoie le maximum de la commande entre le 1 janvier 2015 et le 15 janvier 2015

-   **duration**(commande, valeur, période) et **durationbetween**(commande,valeur,start,end) : donnent la durée en minutes pendant laquelle l'équipement avait la valeur choisie sur la période (period=[month,day,hour,min] ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php)) ou entre les 2 bornes demandées (sous la forme Y-m-d H:i:s ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

    -   Ex : duration(\#[Salon][Prise][Etat]\#,1,Today) : renvoie la durée en minutes pendant laquelle la prise était allumée depuis le début de la journée.

    -   Ex : durationBetween(\#[Salon][Prise][Etat]\#,0,Last Monday,Now) : renvoie la durée en minutes pendant laquelle la prise était éteinte depuis lundi dernier.

-   **statistics**(commande,calcul,période) et **statisticsBetween**(commande,calcul,start,end) : donnent le résultat de différents calculs statistiques (sum, count, std, variance, avg, min, max) sur la période (period=[month,day,hour,min] ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php)) ou entre les 2 bornes demandées (sous la forme Y-m-d H:i:s ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

    -   Ex : statistics(\#[Salle de bain][Hydrometrie][Humidité]\#,std,1 mois) : renvoi [l'écart-type](http://fr.wikipedia.org/wiki/%C3%89cart_type) de température sur un mois.

-   **tendance**(commande,période,seuil) : donne la tendance de la commande sur la période (period=[month,day,hour,min] ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

-   Ex : tendance(\#[Salle de bain][Hydrometrie][Humidité]\#,1 hour,0.1) : renvoie 1 si en augmentation, 0 si constant et -1 si en diminution Le seuil permet de definir la sensibilité, attention le calcul du seuil utilise la calcul de [moindre carrés](http://fr.wikipedia.org/wiki/M%C3%A9thode_des_moindres_carr%C3%A9s)

-   **stateDuration**(commande,[valeur]) : donne la durée en secondes depuis le dernier changement de valeur. Retourne -1 si aucun historique n’existe ou si la valeur n’existe pas dans l’historique. Return -2 si la commande n’est pas historisée

    -   Ex : stateDuration(\#[Salle de bain][Hydrometrie][Humidité]\#) : renvoie 300 si cette valeur est la depuis 5min

-   **lastChangeStateDuration**(commande,valeur) : donne la durée en secondes depuis le dernier changement d'état à la valeur passée en paramètre.Attention, la valeur de l'équipement doit être historisée.

    -   Ex : lastChangeStateDuration(\#[Salle de bain][Hydrometrie][Humidité]\#,0) : renvoie 300 si cette valeur est passée à 0 la dernière fois il y a 5 minutes (même si depuis sa valeur a changé).

-   **lastStateDuration**(commande,valeur) : donne la durée en secondes pendant laquelle l'équipement a dernièrement eu la valeur choisie. Attention, la valeur de l'équipement doit être historisée.

    -   Ex : lastStateDuration(\#[Salle de bain][Hydrometrie][Humidité]\#,0) : renvoie 300 si la valeur 0 est là depuis 5 minutes ou si elle a été là pendant 5 minutes précédemment.

-   **stateChanges**(commande,[valeur], période) et **stateChangesBetween**(commande, [valeur], start, end) : donnent le nombre de changements d'état (vers une certaine valeur si indiquée, ou au total sinon) sur la période (period=[month,day,hour,min] ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php)) ou entre les 2 bornes demandées (sous la forme Y-m-d H:i:s ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

    -   Ex : stateChanges(\#[Salon][Prise][Etat]\#,1,Today) : renvoie le nombre d’allumages (passage à 1) de la prise aujourd’hui

    -   Ex : stateChangesBetween(\#[Salon][Prise][Etat]\#,0,2015-01-01 00:00:00,2015-01-15 00:00:00) : renvoie le nombre d’extinctions (passage à 0) de la prise entre le 1 janvier 2015 et le 15 janvier 2015

-   **lastBetween**(commande,start,end) : donne la dernière valeur enregistrée pour l'équipement entre les 2 bornes demandées (sous la forme Y-m-d H:i:s ou [expression PHP](http://php.net/manual/fr/datetime.formats.relative.php))

    -   Ex : lastBetween(\#[Salle de bain][Hydrometrie][Humidité]\#,Yesterday,Today) : renvoie la dernière température enregistrée hier.

-   **variable**(mavariable,valeur par défaut) : récupération de la valeur d’une variable ou de la valeur souhaitée par défaut

    -   Ex : variable(plop,10) renvoie la valeur de la variable plop ou 10 si elle est vide ou n’existe pas

-   **scenario**(scenario) : liefert den Status des Szenarios

-   Bsp. : scenario(\#[Badezimmer][Licht][Auto]\#) : giebt zurück 1 läuft, 0 wenn gestoppt, -1 wenn deaktiviert, -2 wenn das Szenario nicht gefunden wurde und -3 wenn die Bedingung nicht konsistent

-   **lastScenarioExecution**(scenario) : gibt die Zeit in Sekunden seit dem letzten Start das Szenarios

    -   Bsp. : lastScenarioExecution(\#[Badezimmer][Licht][Auto]\#) : giebt zurück 300, das Szenario wurde in diesem Fall zum letzten Mal vor 5min gestartet

-   **collectDate**(cmd,[format]) : renvoie la date de la dernière donnée pour la commande donnée en paramètre, le 2ème paramètre optionel permet de spécifier le format de retour (détails [ici](http://php.net/manual/fr/function.date.php)). Un retour de -1 signifie que la commande est introuvable, et -2 que la commande n’est pas de type info

    -   Bsp. : collectDate(\#[Badezimmer][Hydrometrie][Luftfeuchtigkeit]\#) : Rückgabe 2015-01-01 17:45:12

-   **valueDate**(cmd,[format]) : renvoie la date de la dernière donnée pour la commande donnée en paramètre, le 2ème paramètre optionel permet de spécifier le format de retour (détails [ici](http://php.net/manual/fr/function.date.php)). Un retour de -1 signifie que la commande est introuvable, et -2 que la commande n’est pas de type info

    -   Ex : valueDate(\#[Salle de bain][Hydrometrie][Humidité]\#) : renverra 2015-01-01 17:50:12

-   **eqEnable**(equipement) : renvoie l'état de l'équipement (actif ou non)

    -   Ex : eqEnable(\#[Aucun][Basilique]\#) : renvoie -2 si l'équipement est introuvable, 1 si l'équipement est actif et 0 s’il est inactif

-   **report** : permet d’exporter une vue au format (PDF,PNG, JPEG ou SVG) et de l’envoyer par le biais d’une commande de type message. Attention si votre accès internet est en https non signé cette fonctionalité ne marchera pas, il faut du http ou https signé.

Les périodes et intervalles de ces fonctions peuvent également s’utiliser avec [des expressions PHP](http://php.net/manual/fr/datetime.formats.relative.php) comme par exemple :

-   *Now* : maintenant

-   *Today* : 00:00 aujourd’hui (permet par exemple d’obtenir des résultats de la journée si entre *Today* et *Now*)

-   *Last Monday* : lundi dernier à 00:00

-   *5 days ago* : il y a 5 jours

-   *Yesterday noon* : hier midi

-   Etc.

Voici un exemple pratique pour comprendre les valeurs retournées par ces différentes fonctions :

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prise ayant pour valeurs :</th>
<th align="left">000 (pendant 10 minutes) 11 (pendant 1 heure) 000 (pendant 10 minutes)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>average(prise,période)</p></td>
<td align="left"><p>Renvoie la moyenne des 0 et 1 (peut être influencée par le polling)</p></td>
</tr>
<tr class="even">
<td align="left"><p>min(prise,période)</p></td>
<td align="left"><p>Renvoie 0 : la prise a bien été éteinte dans la période</p></td>
</tr>
<tr class="odd">
<td align="left"><p>max(prise,période)</p></td>
<td align="left"><p>Renvoie 1 : la prise a bien été allumée dans la période</p></td>
</tr>
<tr class="even">
<td align="left"><p>duration(prise,1,période)</p></td>
<td align="left"><p>Renvoie 60 : la prise était allumée (à 1) pendant 60 minutes dans la période</p></td>
</tr>
<tr class="odd">
<td align="left"><p>duration(prise,0,période)</p></td>
<td align="left"><p>Renvoie 20 : la prise était éteinte (à 0) pendant 20 minutes dans la période</p></td>
</tr>
<tr class="even">
<td align="left"><p>statistics(prise,count,période)</p></td>
<td align="left"><p>Renvoie 8 : il y a eu 8 remontées d'état dans la période</p></td>
</tr>
<tr class="odd">
<td align="left"><p>tendance(prise,période,0.1)</p></td>
<td align="left"><p>Renvoie -1 : tendance à la baisse</p></td>
</tr>
<tr class="even">
<td align="left"><p>stateDuration(prise)</p></td>
<td align="left"><p>Renvoie 600 : la prise est dans son état actuel depuis 600 secondes (10 minutes)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>stateDuration(prise,0)</p></td>
<td align="left"><p>Renvoie 600 : la prise est éteinte (à 0) depuis 600 secondes (10 minutes)</p></td>
</tr>
<tr class="even">
<td align="left"><p>stateDuration(prise,1)</p></td>
<td align="left"><p>Renvoie une valeur comprise entre 0 et stateDuration(prise) (selon votre polling) : la prise n’est pas dans cet état</p></td>
</tr>
<tr class="odd">
<td align="left"><p>lastChangeStateDuration(prise,0)</p></td>
<td align="left"><p>Renvoie 600 : la prise s’est éteinte (passage à 0) pour la dernière fois il y a 600 secondes (10 minutes)</p></td>
</tr>
<tr class="even">
<td align="left"><p>lastChangeStateDuration(prise,1)</p></td>
<td align="left"><p>Renvoie 4200 : la prise s’est allumée (passage à 1) pour la dernière fois il y a 4200 secondes (1h10)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>lastStateDuration(prise,0)</p></td>
<td align="left"><p>Renvoie 600 : la prise est éteinte depuis 600 secondes (10 minutes)</p></td>
</tr>
<tr class="even">
<td align="left"><p>lastStateDuration(prise,1)</p></td>
<td align="left"><p>Renvoie 3600 : la prise a été allumée pour la dernière fois pendant 3600 secondes (1h)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>stateChanges(prise,période)</p></td>
<td align="left"><p>Renvoie 3 : la prise a changé 3 fois d'état pendant la période</p></td>
</tr>
<tr class="even">
<td align="left"><p>stateChanges(prise,0,période)</p></td>
<td align="left"><p>Renvoie 2 : la prise s’est éteinte (passage à 0) deux fois pendant la période</p></td>
</tr>
<tr class="odd">
<td align="left"><p>stateChanges(prise,1,période)</p></td>
<td align="left"><p>Renvoie 1 : la prise s’est allumée (passage à 1) une fois pendant la période</p></td>
</tr>
</tbody>
</table>

Une boîte à outils de fonctions génériques peut également servir à effectuer des conversions ou calculs :

-   **rand**(1,10) : pour un nombre aléatoire de 1 à 10

-   **randomColor**(min,max) : donne une couleur aléatoire compris entre 2 bornes ( 0 ⇒ rouge, 50 ⇒ vert, 100 ⇒ bleu)

    -   Ex : randomColor(40,60) : pour avoir une couleur aléatoire proche du vert

-   **trigger**(commande) : permet de connaître le déclencheur du scénario ou de savoir si c’est bien la commande passée en paramètre qui a déclenché le scénario

    -   Ex : trigger(\#[Salle de bain][Hydrometrie]) : 1 si c’est bien \\[Salle de bain][Hydrometrie][Humidité]\# qui a déclenché le scénario sinon 0

-   **triggerValue**(commande) : permet de connaitre la valeur du déclencheur du scénario

    -   Ex : triggerValue(\#[Salle de bain][Hydrometrie]) : 80 si l’hydrométrie de \\[Salle de bain][Hydrometrie][Humidité]\# est de 80 %

-   **round**(valeur,[decimal]) : permet un arrondi au dessus, [decimal] nombre de décimales après la virgule

    -   Ex : round(\#[Salle de bain][Hydrometrie][Humidité]\# / 10) : renverra 9 si le pourcentage d’humidité et 85

-   **odd**(valeur) : permet de savoir si un nombre est impair ou non. Renvoi 1 si impair 0 sinon

    -   Ex : odd(1) : renverra 1

-   **median**(commande1,commande2….commandeN) : renvoie la médiane de valeur

    -   Ex : median(15,25,20) : renverra 20

-   **time\_op**(time,value) : permet de faire des opérations sur le temps, avec time=temps (ex 1530) et value=valeur à ajouter ou à soustraire en minutes

    -   Ex : time\_op(\#time\#, -90) : s’il est 16h50 renverra : 1650 - 0130 = 1520

-   **formatTime**(time) : permet de formater le retour d’une chaine \#time\#

    -   Ex : formatTime(1650) : renverra 16h50

-   **floor**(time/60) : permet de convertir des secondes en minutes, ou des minutes en heures (floor(time/3600) pour des secondes en heures)

    -   Ex : floor(130/60) : renverra 2 (minutes si 130s, ou heures si 130m)

Action
------

En plus des commandes domotiques vous avez accès aux actions suivantes :

-   **sleep** : pause de x seconde(s)

-   **wait** : attend jusqu'à ce que la condition soit valide (maximum 2h), le timeout est en seconde(s)

-   **variable** : création/modification d’une variable ou de la valeur d’une variable

-   **scenario** : permet le contrôle des scénarios, la partie tags permets d’envoyer des tags au scénario, ex montag=2

-   **stop** : arrête le scénario

-   **icon** : permet de changer l’icône de représentation du scénario

-   **gotodesign** : change le design affiché sur tous les navigateurs par le design demandé

-   **log** : permet de rajouter un message dans les logs

-   **message** : permet d’ajouter un message dans le centre de message

-   **equipement** : permet de modifier les propriétés d’un équipement visible/invisible actif/inactif

-   **jeedom\_poweroff** : demande à Jeedom de s'éteindre

-   **scenario\_return** : Retourne un texte ou une valeur pour une intéraction par exemple

-   **event** : Permet de modifier la valeur d’une commande

-   **alert** : permet d’afficher un petit message d’alerte sur tous les navigateurs qui ont une page jeedom ouverte. Vous pouvez en plus choisir 4 niveaux d’alerte

-   **popup** : permet d’afficher un popup qui doit absolument être validé sur tous les navigateurs qui ont une page jeedom ouverte.

-   **ask** : permet d’indiquer à jeedom qu’il faut poser une question à l’utilisateur. La réponse est stockée dans une variable, il suffit ensuite de tester sa valeur. Pour le moment seuls les plugins sms et slack sont compatibles. Attention l’action ask est bloquante, tant qu’il n’y a pas de réponse ou que le timeout n’est pas atteint le scénario attend. Voila un exemple d’utilisation :

Bild:… / Bilder/scenario20. JPG]

Code
----

Achtung, Tags sind nicht in einem Block des Code-Typs verfügbar.

Befehle (Sensoren und Aktoren)  
-   **cmd::byString(\$string)**;

    -   Liefert das entsprechende Befehlsobjekt

    -   \$string ⇒ Link zum gewünschten Befehl : \#[objekt][gerät][befehl]\# (Bsp. : \#[Wohnung][Alarm][Aktiv]\#)

-   **cmd::byId(\$id)**;

    -   Liefert das entsprechende Befehlsobjekt

    -   \$id ⇒ Id des gewünschten Befehls (siehe Allgemein⇒Anzeige)

-   **\$cmd→execCmd(\$options = null)**;

    -   Den Befehl ausführen und das Ergebnis ausgeben

    -   \$options ⇒ Optionen für die Befehlsausführung (kann spezifisch für das Plugin sein), Grundoption :

        -   Subtyp des Befehls :

            -   message ⇒ `$option = array('title' => 'titre du message , 'message' => 'Mon message');`

            -   color ⇒ `$option = array('color' => 'Farbe in Hexadezimal');`

            -   slider ⇒ `$option = array('slider' => 'gewünschten Wert von 0 bis 100');`

Log  
-   **log::add(*filename*,*level*,*message*)**;

    -   filename ⇒ Name der Protokolldatei

    -   level ⇒ [debug],[info],[error],[event]

    -   message ⇒ Nachricht in Protokoll schreiben

Szenario  
-   **\$scenario-\>getName()**;

    -   Liefert den Namen des aktuellen Szenarios

-   **\$scenario-\>getGroup()**;

    -   Liefert die Szenariengruppe

-   **\$scenario-\>getIsActive()**;

    -   Liefert den Status des Szenarios

-   **\$scenario-\>setIsActive(\$active)**;

    -   Ermöglicht das Szenario zu aktivieren oder deaktivieren

    -   \$active ⇒ 1 aktiv , 0 nicht aktiv

-   **\$scenario-\>setOnGoing(\$onGoing)**;

    -   Erlaubt zu sagen, ob das Szenario im Gange ist oder nicht

    -   \$onGoing ⇒ 1 läuft, 0 gestoppt

-   **\$scenario-\>save()**;

    -   Änderungen speichern

-   **\$scenario-\>setData(\$key, \$value)**;

    -   Daten speichern (Variable)

    -   \$key ⇒ Schlüsselwert (int oder string)

-   \$value ⇒ Wert der gespeichert werden soll (int, string, array oder object)

-   **\$scenario-\>getData(\$key)**;

    -   Daten abfragen (Variable)

    -   \$key ⇒ Schlüsselwert (int oder string)

-   **\$scenario-\>removeData(\$key)**;

    -   Daten löschen

-   **\$scenario-\>setLog(\$message)**;

    -   Schreibt eine Nachricht in das Protokoll des Szenarios

-   **\$scenario-\>persistLog()**;

    -   Force l'écriture du log (sinon il est écrit seulement à la fin du scénario). Attention ceci peut un peu ralentir le scénario

Die Variablen
=============

Vous pouvez en cliquant sur le bouton variable voir toutes les variables existantes sur votre système, changer leur valeur, les supprimer, en ajouter et voir dans quel scénario elles sont utilisées :

![](../images/scenario14.JPG)

Szenario Vorlagen
=================

Fonctionalité permettant de transformer un scénario en template pour par exemple l’appliquer sur un autre Jeedom ou le partager sur le Market. C’est aussi à partir de là que vous pouvez récupérer un scénario du Market

![](../images/scenario15.JPG)

Dann sehen Sie dieses Fenster :

![](../images/scenario16.JPG)

Hier haben sie folgende Möglichkeiten :

-   D’envoyer un template à Jeedom (fichier JSON préalablement récupéré)

-   De consulter la liste des scénarios disponibles sur le Market Eine Vorlage von dem laufenden Szenario zu erschaffen (vergessen nicht, einen Namen zu vergeben)

-   Sie sehen die zur Zeit vorhandenen Vorlagen auf Ihrem Jeedom

Par un clic sur un template vous obtenez :

![](../images/scenario17.JPG)

Oben können sie :

-   **Partager** : partager le template sur le Market

-   **Löschen** : Vorlage löschen

-   **Herunterladen** : erlaubt, die Vorlage in Form einer JSON-Datei abzuspeichern, um es als Beispiel auf ein anderes Jeedom zu schicken

Darunter haben Sie den Teil, um Ihre Vorlage auf das laufende Szenario anzuwenden.

> **Tip**
>
> Etant donné que d’un Jeedom à l’autre ou d’une installation à une autre les commandes peuvent être différentes, Jeedom vous demande la correspondance des commandes entre celles présentes lors de la création du template et celles présentes chez vous.

Il vous suffit de remplir la correspondance des commandes puis de faire appliquer

Die Protokolle
==============

Sie können zum Ausführungsprotokoll eines Szenarios gelangen, indem Sie auf die Schaltfläche "Log" klicken :

![](../images/scenario17.JPG)

Sie erhalten :

![](../images/scenario19.JPG)

En haut vous pouvez rafraîchir le log, le télécharger ou le supprimer. La taille des logs n’est pas limitée en exécution mais en nombre de lignes (en fonction de la valeur mise dans la configuration de Jeedom)
