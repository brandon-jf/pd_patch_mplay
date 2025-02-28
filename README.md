# pd_patch_mplay
Ce patch Pure Data est un lecteur audio multi-pistes qui permet de jouer jusqu'à 8 fichiers audio en parallèle avec des commandes de contrôle pour chaque piste.
Description

Ce patch Pure Data est un lecteur de playlist permettant la lecture séquentielle ou non de fichiers audio (échantillons .wav). Il intègre une transition douce (crossfade) de 3 secondes entre les pistes, permettant un fondu enchaîné fluide entre les morceaux. Il offre aussi des commandes clavier pour arrêter ou changer de piste efficacement.

Fonctionnalités

Lecture enchaînée des fichiers audio : M1.wav, M2+B1.wav, M3.wav, etc.

Transition fluide : Lors d'un changement de piste, le volume de la piste en cours diminue progressivement pendant 3 secondes, tandis que le volume de la piste suivante augmente.

Commande pour arrêter une piste :

Appuyer sur Espace puis sur la touche de raccourci associée.

Commande pour changer de piste en séquence :

Appuyer sur la touche associée à la piste suivante.

Exemple : Passer de M3 à M4 en appuyant sur E.

Commande pour changer de piste non consécutive :

Appuyer sur Espace + (Touche de la piste courante) + Espace + (Touche de la piste précédant celle choisie).

Exemple : Passer de M7+B3 à M3 : Espace + U + Espace + Z.

Raccourcis clavier

Espace : Active la gestion du changement de piste.

[Touche associée] : Lance la piste correspondante.

Fonctionnement interne

Chaque piste audio est jouée avec l'objet readsf~.

La gestion du volume est assurée par line~ pour permettre une transition douce.

Un système de raccourcis clavier permet de naviguer efficacement entre les pistes.
