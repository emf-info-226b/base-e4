# Évaluation : Lecture, Transformation et Écriture d'un Fichier Texte en Java

## Objectif

L'objectif de cette évaluation est de permettre à l'étudiant de démontrer ses compétences en lecture, manipulation et écriture de fichiers texte en Java. Vous devrez lire un fichier texte contenant des données d'inscription, effectuer une transformation sur ces données, puis écrire les résultats dans un nouveau fichier texte.

## Détails du fichier d'inscription

Le fichier d'inscription contient des informations sur plusieurs personnes. Chaque ligne du fichier correspond à une personne et est composée de plusieurs colonnes séparées par des virgules. Les colonnes suivantes sont présentes dans le fichier :

1. **Nom** : Le nom de la personne (String)
2. **Prénom** : Le prénom de la personne (String)
3. **Date de naissance** : La date de naissance au format `yyyy-MM-dd` (String)
4. **Email** : L'adresse email de la personne (String)
5. **Téléphone** : Le numéro de téléphone (String)

Exemple de ligne dans le fichier :
```
Dupont,Jean,1990-05-12,jean.dupont@example.com,0791234567 
Martin,Alice,1985-11-23,alice.martin@example.com,0789876543
```

## Tâches à réaliser

### 1. Lecture du fichier texte
Vous devez lire un fichier texte nommé `files/inscriptions.txt`, dans lequel se trouvent les données d'inscription. Chaque ligne du fichier contient une personne, avec les informations séparées par des virgules.

### 2. Transformation des données
Pour chaque personne, vous devrez transformer les données comme suit :
- Transformer la date de naissance pour qu'elle soit au format `dd.MM.yyyy` au lieu de `yyyy-MM-dd`.
- Vérifier que l'adresse email est valide (elle doit contenir un "@"), si l'e-mail n'est pas valide, la ligne ne sera pas importée.
- Ajouter une colonne "Sigle" à la fin de chaque ligne, qui définit le sigle de la personne. Le format est le suivant : 3 premiers caractères du nom en majuscule, suivi de 2 premiers caractères du prénom en minuscule, suivi du l'année. Ex : Dupont Jean 1990 correspond à DUPje1990.

### 3. Écriture dans un nouveau fichier texte
Vous devez ensuite écrire les données transformées dans un nouveau fichier texte nommé `files/exportation.txt`. Chaque ligne du fichier doit contenir les informations transformées de la personne, avec les colonnes suivantes : Sigle, Nom, Prénom, Date de naissance, Email.

Exemple de ligne dans le fichier modifié :
```
DUPje1990,Dupont,Jean,12.05.1990jean.dupont@example.com
MARal1985,Martin,Alice,23.11.1985,alice.martin@example.com
```

### 4. Écriture dans un nouveau fichier binaire
Vous devez ensuite écrire les données dans un nouveau fichier binaire nommé `files/inscriptions.ser`. Toutes les données doivent être stockées dans ce fichier binaire.
Au redémarrage de l'application, si le fichier `files/inscriptions.ser` est existant, le programme affiche dans la console le contenu de ce fichier.

## Contraintes techniques

- Utilisez la classe `BufferedReader` pour lire le fichier et la classe `BufferedWriter` pour écrire le fichier.
- Un worker spécifique doit être présent pour permettre de lire et d'écrire des fichiers
- Le fichier de sortie doit conserver le même format que le fichier d'entrée, avec les données transformées correctement.

## Critères d'évaluation

- Capacité à lire correctement le fichier texte d'entrée.
- Correctitude des transformations appliquées aux données.
- Capacité à gérer les erreurs (fichier non trouvé, format de date incorrect, email invalide, etc.).
- Structure et clarté du code Java (utilisation de fonctions, lisibilité, commentaires).
- Respect des contraintes techniques.

## Instructions pour soumettre

1. Clonez ce dépôt sur votre machine locale.
2. Implémentez votre solution dans un fichier Java nommé `Application.java`.
3. Testez votre programme avec différents fichiers d'inscription.
4. Lorsque vous êtes satisfait de votre solution, poussez votre code sur GitHub.

Bonne chance !


