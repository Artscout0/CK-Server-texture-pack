# Qu'est-ce que c'est ?

Il s'agit d'un repository GitHub qui permet d'ajouter des modèles et des textures personnalisés aux serveurs Minecraft.

## Comment ça marche ?

Tout d'abord, vous créez un modèle et une texture personnalisés. Nous vous suggérons d'utiliser un logiciel comme Blockbench, mais vous pouvez utiliser celui que vous préférez. Ensuite, vous créez un dossier que vous pouvez nommer comme vous le souhaitez. Ouvrez le terminal en faisant un clic droit et en sélectionnant ouvrir dans le terminal, puis entrez la commande suivante :

```bash
git clone https://github.com/Artscout0/CK-Server-texture-pack.git
```

Ajoutez ensuite les textures et modèles pertinents : placez les fichiers .json dans `\assets\minecraft\models\item\models`, et les fichiers .png dans `\assets\minecraft\textures\item\model_texture`.

Ensuite, allez dans `\assets\minecraft\items\`, et ouvrez le fichier `green_dye.json` avec un éditeur de texte, nous recommandons Visual Studio Code ou Notepad++. À l'intérieur, allez dans la section `entries` et ajoutez une ligne qui ressemble à ceci :

```json
{
    "threshold": XX,
    "model": {
        "type": "minecraft:model",
        "model": "item/models/YY"
    }
}
```

Remplacez XX par un nombre et YY par le nom du modèle. Exemple :

```json
{
    "threshold": 1,
    "model": {
        "type": "minecraft:model",
        "model": "item/models/Murasama"
    }
}
```

Cela fera en sorte que le 1er modèle personnalisé pour l'epee en netherite sera le modèle "Murasama".
***N'OUBLIEZ PAS D'AJOUTER UNE VIRGULE À LA FIN DE LA LIGNE PRÉCÉDENTE !***

Si vous souhaitez rendre votre modèle personnalisé portable par un joueur, ajoutez-le dans `carved_pumpkin.json` à la place.
Si vous voulez le rendre mangeable, ce sera dans `golden_carrot.json`.
Si vous voulez ajouter ça a un item different (ça marche que avec les items, pas les blocks), ajoutez le dans le fichier json avec le nom de l'item en question. Si il n'existe pas (encore), soit regardez comment les autres fichiers fonctionnent et ajoutez le manuellement, ou ouvrez une [issue](https://github.com/Artscout0/CK-Server-texture-pack/issues/new), et un jour on le fera a votre place.

Après avoir ajouté tous les modèles personnalisés, nous vous recommandons fortement de tester si le pack de textures fonctionne en copiant l'intégralité du dossier que vous avez créé dans le dossier `.minecraft\resourcepacks` (vous pouvez y accéder en ouvrant vos packs de ressources dans Minecraft et en cliquant sur ouvrir le dossier des packs).

Vous pouvez ensuite activer le pack de textures comme n'importe quel autre.

Ensuite, tenez l'objet que vous avez précédemment choisi (soit la teinture verte ou la citrouille sculptée) dans votre main, et écrivez dans le chat la commande suivante :

```command
/trigger CustomModelData set XX
```

Où XX est le nombre que vous avez précédemment inscrit après "custom_model_data".

Si un message s'affiche disant "vous n'avez pas assez d'expérience", exécutez d'abord la commande suivante :

```command
/xp add @s 10000 levels
puis la commande précédente.
```

Si cela fonctionne et que le modèle et la texture de l'objet deviennent ceux que vous avez créés, parfait ! Cela fonctionne.

Ensuite, vous pouvez push les modifications vers le repository GitHub.
(ce qui consite en gros à publier les modifications que vous apporté au pack)

Pour ce faire, retournez dans le terminal que vous avez précédemment ouvert et écrivez les commandes suivantes :

```bash
git add .
git commit -m "message de commit"
git push origin main
Après cela, tout devrait être en ordre !
```

FAQ :
Q : Que faire si quelque chose ne fonctionne pas ?
R : 1. Verifiez si vous avez ajouté la virgule. 2. Contactez Artscout sur Discord et expliquez-lui le problème. Vous pouvez également lui envoyer un message privé. 3. ouvrez une [issue](https://github.com/Artscout0/CK-Server-texture-pack/issues/new)

Q : Le terminal indique qu'il ne connaît pas git.
R : Installez git, et si cela ne fonctionne pas, reportez-vous à la question 1. Section 2.

Q : Comment créer un modèle ?
R : Je ne suis pas un artiste 3D professionnel, donc je ne sais pas comment créer de bons modèles, mais je vous recommande fortement d'utiliser Blockbench et d'expérimenter en créant des modèles dont vous pourriez avoir besoin et en dessinant des textures pour eux.

note pour art007: commencer par cd CK(tab)
le tab c'est la touch il ne faut pas écrire tab
