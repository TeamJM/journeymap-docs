# **Traduire le mod**

Si vous souhaitez contribuer à JourneyMap, une bonne façon de le faire est de traduire la documentation et le mod. Cela peut aider les personnes qui ne parlent pas ou qui ne savent pas lire l'anglais à pouvoir lire la documentation de JourneyMap ou à jouer au mod JourneyMap dans leur propre langue.

Les instructions sur la manière de traduire la documentation peuvent être trouvées [ici](translate-docs.md).

## **I. Vérifiez les fichiers de langue actuels**

Ce dépôt Git contient les derniers fichiers de langue pour JourneyMap : **[Fichiers de Langue JourneyMap](https://github.com/TeamJM/journeymap-lang)**.

- Si votre fichier de langue est dans le dépôt, consultez-le et vérifiez son exactitude.
- Si votre fichier de langue **n'est pas** dans le dépôt, votre langue n'a pas encore été traduite pour JourneyMap.

## **II. Instructions pour créer/utiliser le fichier de langue**

Si votre fichier de langue n'existe pas encore :

1. Copiez le fichier `en_us.json`
2. Renommez-le selon le [Code de Locale](https://minecraft.wiki/w/Language) utilisé par Mojang
3. Assurez-vous qu'il est enregistré avec un encodage UTF-8 (pas ASCII ou un format ISO)

Le fichier .json **doit être enregistré en UTF-8** en utilisant un éditeur de texte qui peut gérer les caractères UTF-8 comme [Notepad Plus](https://notepad-plus-plus.org/).

Si votre langue utilise un jeu de caractères qui doit être géré avec des caractères Unicode, vous pouvez les taper directement dans le fichier. Il n'est **plus nécessaire** d'utiliser des codes de référence de caractères numériques hexadécimaux Unicode (NCR) (comme \u0202).

**Exemple** : `"jm.common.saving_map_to_file": "Sauvegarde de la carte %1$s dans un fichier..."`

<span style="color: red">**Incorrect**</span>: <code>"jm.common.saving_map_to_file": "\u8282\u80FD %1$s \u6620\u5C04\u5230\u6587\u4EF6..."</code>

<span style="color: green">**Correct**</span>: <code>"jm.common.saving_map_to_file": "节能 %1$s 映射到文件..."</code>

## **III. Comment traduire le fichier .json**

- Ouvrez votre nouveau fichier .json dans un éditeur de texte capable de gérer les caractères UTF-8 comme [Notepad Plus](https://notepad-plus-plus.org/). Vous verrez une série de **clés** et de **phrases** séparées par un signe égal (:). Par exemple :

`"jm.common.chat_announcement": "&sect;eJourneyMap:&sect;f %1$s"`
`"jm.common.mapgui_only_ready": "Appuyez sur [&sect;b%1$s&sect;f]. (Serveur Web désactivé.)"`

Les lignes d'exemple ci-dessus ont les **clés** "jm.common.chat_announcement" et "jm.common.mapgui_only_ready".

- Traduisez chaque **phrase** de l'anglais vers votre langue, mais ne modifiez PAS les clés de message. (Ne changez que le texte qui vient **après** le signe égal ("=").)

**Exemple** : <code>"example.key": "Ceci est une phrase."</code>

<span style="color: green">**Correct**</span>: <code>"example.key": "Ceci est une phrase."</code>

<span style="color: red">**Incorrect**</span>: <code>"example.llave": "Ceci est une phrase."</code>

- Beaucoup de phrases contiennent un ou plusieurs **paramètres** numérotés. Par exemple : "%1$s", "%1$d", "%2$s", etc. Ce sont des espaces réservés qui seront remplacés par une valeur lorsque le message sera affiché. Vous pouvez réorganiser ces paramètres si cela est requis par les règles de grammaire de votre langue. Par exemple :

`"jm.common.player_location=Location": "%1$s , %2$s  | Élévation :  %3$s  (  %4$s  ) | Biome :  %5$s"`

Lorsque la phrase ci-dessus est utilisée par JourneyMap, les paramètres seront remplacés par des informations de localisation réelles, comme ceci :

`Location: 23,-98 | Élévation: 32 (2) | Biome: Désert`

- Si une phrase manque dans un fichier de langue existant, elle sera préfixée par un "#" et avoir "???" comme phrase. Vous devez supprimer le préfixe "#" et fournir la phrase correcte.

**Exemple** : <code># "example.key": "???"</code>

<span style="color: green">**Correct**</span>: <code>"example.key": "Ceci est une phrase."</code>

- N'ajoutez pas de sauts de ligne (retours chariot) ou de HTML dans aucune des phrases.

- Ne traduisez pas et ne retirez pas les combinaisons de caractères spéciaux utilisées par Minecraft pour changer de couleur. (&sect;b, &sect;f, &sect;e, etc.)

## **IV. Comment tester votre traduction**

1. Utilisez un programme zip comme 7-Zip pour ouvrir votre fichier mod JourneyMap*.jar.
2. Naviguez jusqu'à `/assets/journeymap/lang` et ajoutez votre fichier de langue (s'il est nouveau) ou remplacez l'ancien.
3. JourneyMap utilisera la langue que vous sélectionnez dans Minecraft. Sélectionnez votre langue dans Minecraft, et JourneyMap utilisera votre nouvelle traduction.
4. Veuillez tester votre traduction dans Minecraft autant que possible. Ne vous inquiétez pas d'essayer de provoquer des messages d'erreur, mais essayez de tester autant que possible, y compris les contrôles de la carte en plein écran (et les info-bulles), les Options (et les info-bulles), et les contrôles de la carte Web pour confirmer qu'ils fonctionnent.

## **V. Comment soumettre votre traduction**

[Suivez les instructions sur Github](https://github.com/TeamJM/journeymap-lang#how-to-translate-journeymap)

**Merci beaucoup pour votre travail acharné !**