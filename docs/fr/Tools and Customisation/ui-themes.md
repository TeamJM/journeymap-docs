## **Aperçu**

L'apparence des barres d'outils peut être modifiée à l'aide du bouton Thème UI (icône d'une palette de peinture). Vous pouvez également créer de nouveaux thèmes avec vos propres images, icônes et couleurs.

## **Thèmes Disponibles**

- [Vault](https://minecraft.curseforge.com/projects/journeymap/files/2303051) (Fallout Pipboy)

**Si vous créez un thème vraiment sympa et souhaitez le partager avec le monde, envoyez un message privé à techbrew sur MinecraftForums (ou tweetez [@JourneyMapMod](https://twitter.com/journeymapmod) sur Twitter).**

## **Comment Créer un Thème UI : Début Facile**

1. Copiez **.minecraft/journeymap/icon/theme/Victorian** et collez la copie dans le dossier **/theme** avec un nouveau nom, par ex. : ("MonThème")
2. Dans votre nouveau dossier de thème :
    1. Supprimez **Purist.theme.json**
    2. Renommez **Victorian.theme.json** en quelque chose de nouveau (Ex : "MonThème.theme.json")
    3. Modifiez votre nouveau fichier theme.json avec un éditeur de texte et changez le nom du répertoire, le nom du thème et les propriétés de l'auteur pour correspondre à votre dossier et fichier.
    4. Parcourez les images dans votre répertoire de thème et voyez comment elles se rapportent aux boutons et barres d'outils dans JourneyMap.
    5. Remplacez les images dans votre répertoire de thème par vos propres créations - sauf pour les images dans **icon/**, et assurez-vous que vos remplacements soient de la même taille que celles que vous remplacez.
3. Utilisez le bouton Thème UI dans la Carte Plein Écran (avec l'icône d'une palette de peinture) pour passer à votre nouveau Thème.
4. Partagez votre thème avec d'autres en compressant simplement votre dossier de thème et en le leur donnant. Lorsqu'ils le décompressent dans **.minecraft/journeymap/icon/theme/**, ils peuvent l'utiliser en appuyant sur le bouton Thème UI.

## **Comment Créer un Thème UI : Conseils Avancés**

Le fichier theme.json utilise des conventions très similaires aux feuilles de style en cascade (CSS). Les images comme les icônes de bouton peuvent être colorées à l'aide de couleurs hexadécimales RGB standard, tout comme vous le feriez en CSS.

Les tailles d'image n'ont pas besoin d'être exactement les mêmes que celles que vous trouverez dans le thème Victorian. Cependant, vous devrez modifier le fichier theme.json et commencer à changer les dimensions des images pour correspondre à votre création.

Créez des images 2x plus grandes que les tailles que vous spécifiez dans le fichier theme.json. Cela permet d'avoir des écrans à plus haute résolution et aux personnes utilisant l'échelle GUI Auto (ou Grande) de Minecraft de disposer toujours de boutons de bonne apparence.

## **Comment Désigner un Thème UI par Défaut dans les Modpacks**

Les modpacks peuvent fournir un thème pour les utilisateurs en créant un dossier de thème exactement comme ci-dessus. Si un auteur de modpack le souhaite, il peut également désigner ce thème comme le thème par défaut pour les utilisateurs qui utilisent JourneyMap 5 pour la première fois.

Cela peut être fait en créant ce fichier : .minecraft/journeymap/icon/theme/default.theme.config

Le contenu du fichier fournit le nom du dossier du thème, le nom du fichier json et le nom désigné dans le fichier json, comme suit :

```json
 {
  "directory": "Victorian",
  "filename": "Victorian",
  "name": "Victorian"
 }
```

## **Code et Commentaires pour les Thèmes**

Chaque fichier theme.json est lu par JourneyMap via GSON et crée une simple hiérarchie de classes Java utilisée pour construire les éléments de l'interface utilisateur. **Vous ne pouvez pas changer la structure des fichiers json de quelque manière que ce soit, seulement modifier les valeurs fournies.**

Voici le code source de la classe Java utilisée pour générer les fichiers theme.json. Les commentaires sont destinés à vous donner un aperçu de l'utilisation de chaque propriété :

```java
 /**
  * Spécification du thème pour JourneyMap 5.0
  */
 public class Theme implements Comparable<Theme>
 {
    /**
     * Version actuelle de cette spécification
     */
    public static final int VERSION = 1; 
 
    /**
     * Auteur du thème.
     */
    @Since(1)
    public String author; 
 
    /**
     * Nom du thème.
     */
    @Since(1)
    public String name; 
 
    /**
     * Nom du répertoire parent des fichiers de thème.
     */
    @Since(1)
    public String directory; 
 
    /**
     * Spécifications des conteneurs pour les images dans le répertoire /container.
     * Actuellement juste Toolbar.
     */
    @Since(1)
    public Container container = new Container(); 
 
    /**
     * Spécifications du contrôle UI pour les images dans le répertoire /control.
     * Actuellement : Button & Toggle.
     */
    @Since(1)
    public Control control = new Control(); 
 
    /**
     * Spécifications de la carte FullMap pour les images dans le répertoire /fullscreen.
     */
    @Since(1)
    public Fullscreen fullscreen = new Fullscreen(); 
 
    /**
     * Taille générale pour toutes les icônes dans le répertoire /icon
     */
    @Since(1)
    public ImageSpec icon = new ImageSpec(); 
 
    /**
     * Spécifications de la minimap circulaire pour les images dans le répertoire /minimap/circle.
     */
    @Since(1)
    public Minimap minimap = new Minimap(); 
 
    /**
     * Classe de conteneur pour les images dans /container.
     */
    public static class Container
    {
        /**
         * Spécifications pour les images de la barre d'outils dans /container.
         */
        @Since(1)
        public Toolbar toolbar = new Toolbar(); 
 
        /**
         * Classe Toolbar pour les images de la barre d'outils dans /container.
         */
        public static class Toolbar
        {
            /**
             * Spécifications pour les images de la barre d'outils horizontale.
             */
            @Since(1)
            public ToolbarSpec horizontal = new ToolbarSpec(); 
 
            /**
             * Spécifications pour les images de la barre d'outils verticale.
             */
            @Since(1)
            public ToolbarSpec vertical = new ToolbarSpec(); 
 
            /**
             * Classe ToolbarSpec. Une barre d'outils se compose d'une image de début, d'une
             * image intérieure répétée (une répétition par bouton) et d'une image de fin.
             * <p/>
             * Les noms de fichiers attendus par le chargeur de Thème sont :
             * toolbar_begin.png, toolbar_inner.png, toolbar_end.png
             */
            public static class ToolbarSpec
            {
                /**
                 * True pour utiliser les images du thème, faux pour invisible.
                 */
                @Since(1)
                public boolean useThemeImages; 
 
                /**
                 * Préfixe de nom de fichier. Exemple : "h" pour horizontal, "v" pour vertical.
                 */
                @Since(1)
                public String prefix = ""; 
 
                /**
                 * Marge en pixels autour de la barre d'outils.
                 */
                @Since(1)
                public int margin; 
 
                /**
                 * Espacement en pixels entre les boutons de la barre d'outils.
                 */
                @Since(1)
                public int padding; 
 
                /**
                 * Dimensions de l'image pour le début de la barre d'outils.
                 */
                @Since(1)
                public ImageSpec begin; 
 
                /**
                 * Dimensions de l'image pour la section intérieure répétée de la barre d'outils.
                 */
                @Since(1)
                public ImageSpec inner; 
 
                /**
                 * Dimensions de l'image pour la fin de la barre d'outils.
                 */
                @Since(1)
                public ImageSpec end;
            }
        }
    } 
 
    /**
     * Classe de contrôle pour les images dans /control
     */
    public static class Control
    {
        /**
         * Spécifications pour un bouton normal.
         */
        @Since(1)
        public ButtonSpec button = new ButtonSpec(); 
 
        /**
         * Spécifications pour un bouton bascule.
         */
        @Since(1)
        public ButtonSpec toggle = new ButtonSpec(); 
 
        /**
         * Spécification pour un bouton.
         * Les noms de fichiers attendus par le chargeur de Thème sont :
         * on.png, off.png, hover.png, disabled.png
         */
        public static class ButtonSpec
        {
            /**
             * True pour utiliser les images du thème. Faux pour utiliser la texture de bouton du pack de ressources actuel.
             */
            @Since(1)
            public boolean useThemeImages; 
 
            /**
             * Largeur du bouton.
             */
            @Since(1)
            public int width; 
 
            /**
             * Hauteur du bouton.
             */
            @Since(1)
            public int height; 
 
            /**
             * Préfixe de nom de fichier. Facultatif.
             */
            @Since(1)
            public String prefix = ""; 
 
            /**
             * Style de format de chaîne (

style CSS). 
             * Utilisé pour le texte sur les boutons.
             */
            @Since(1)
            public String fontStyle; 
        }
    } 
 
    /**
     * Spécifications de la carte FullMap.
     * Images attendues dans le répertoire /fullscreen
     */
    public static class Fullscreen
    {
        /**
         * Taille par défaut pour l'image FullMap.
         */
        @Since(1)
        public ImageSpec defaultSize; 
 
        /**
         * Spécifications pour le marqueur.
         * Images dans le répertoire /fullscreen/marker
         */
        @Since(1)
        public MarkerSpec marker; 
 
        /**
         * Images du marqueur sur la carte.
         */
        public static class MarkerSpec
        {
            /**
             * True pour utiliser les images du thème, faux pour invisible.
             */
            @Since(1)
            public boolean useThemeImages; 
 
            /**
             * Taille des marqueurs pour le mode hors ligne.
             */
            @Since(1)
            public int offlineSize; 
 
            /**
             * Taille des marqueurs pour le mode en ligne.
             */
            @Since(1)
            public int onlineSize; 
        }
    } 
 
    /**
     * Spécifications de la minimap.
     * Images dans le répertoire /minimap
     */
    public static class Minimap
    {
        /**
         * Images de la minimap.
         */
        public Circle circle; 
 
        /**
         * Images de la minimap circulaire.
         */
        public static class Circle
        {
            /**
             * True pour utiliser les images du thème, faux pour invisible.
             */
            @Since(1)
            public boolean useThemeImages; 
 
            /**
             * Taille de la minimap.
             */
            @Since(1)
            public int size; 
 
            /**
             * Taille de l'image pour les icônes dans le répertoire /icon.
             */
            @Since(1)
            public ImageSpec icon; 
        }
    } 
 
    /**
     * Spécifications de l'image de l'icône.
     */
    public static class ImageSpec
    {
        /**
         * Largeur de l'image.
         */
        @Since(1)
        public int width; 
 
        /**
         * Hauteur de l'image.
         */
        @Since(1)
        public int height; 
 
        /**
         * Préfixe du nom de fichier. Exemple : "icon-" pour les icônes.
         */
        @Since(1)
        public String prefix = ""; 
    }
    
    /**
     * Fonction de comparaison pour le tri.
     */
    @Override
    public int compareTo(Theme o)
    {
        return 0;
    }
 }
```