# LAB 1 – HelloToast : Manipuler les composants et les événements

Ce projet est une application Android simple développée en Java. Elle permet d'afficher un message temporaire (Toast) et d'incrémenter un compteur numérique affiché à l'écran.

 ## Objectifs du Lab

 •Apprendre à manipuler les composants de base : TextView et Button.
 
 •Comprendre l'organisation d'une interface avec LinearLayout.
 
 •Apprendre à lier le code Java à l'interface XML.
 
 •Gérer les événements de clic (setOnClickListener).

##  Étapes de réalisation

### Étape 1 – Création du projet

•Nom du projet : HelloToast

•Langage : Java

•API minimum : 24 (Android 7.0)

•Modèle : Empty Activity

## Étape 2 – Conception de l’interface (XML)

L'interface est définie dans le fichier res/layout/activity_main.xml. Nous utilisons un LinearLayout vertical pour organiser les éléments

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">

    <!-- Texte affichant la valeur du compteur -->
    <TextView
        android:id="@+id/text_count"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="0"
        android:textSize="36sp"
        android:layout_marginBottom="24dp" />

    <!-- Bouton pour afficher un Toast -->
    <Button
        android:id="@+id/button_toast"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Afficher un message"
        android:layout_marginBottom="12dp" />

    <!-- Bouton pour incrémenter le compteur -->
    <Button
        android:id="@+id/button_count"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Incrémenter le compteur" />
</LinearLayout>

## Étape 3 – Logique Java (MainActivity.java)

Le comportement de l'application est géré dans app/src/main/java/sg/vantagepoint/hellotoast/MainActivity.java.

Fonctionnalités implémentées :

•findViewById() : Récupération des composants graphiques.

•setOnClickListener() : Détection des clics sur les boutons.

•Toast.makeText() : Affichage du message "Bonjour !".

•String.valueOf(count) : Mise à jour du texte du compteur

## 📸 Aperçu Final

🎥 **[Cliquez ici pour voir la démonstration vidéo de l'application]()**

### Fonctionnement :
*   **Initialisation** : L'interface affiche le compteur à 0.
*   **Action Toast** : Le bouton déclenche un message "Bonjour !".
*   **Action Count** : Chaque clic sur le bouton "Incrémenter" met à jour le `TextView` dynamiquement.
