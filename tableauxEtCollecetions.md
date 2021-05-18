# Tableau et collection en java

## Les tableaux

### Initialiser mon tableau 

```java
int[] tableauEntier = new int[] {1,2,3,4,5,6,7,8,9,10};
```
### La taille du tableau
```java
System.out.println(tableauEntier.length); // => 10
```
### Copier un tableau
```java
int[] tableau2 = Arrays.copyOf(tableauEntier)
```
### Parcourir mon tableau

#### Avec for
```java
for(int i= 0; i< tableauEntier.length; i++) {
    System.out.print(i + " "); // => 1 2 3 4 5 6 7 8 9 10
}
```

#### Avec for each
```java
for(int element : tableauEntier) {
    System.out.print(element + " "); // => 1 2 3 4 5 6 7 8 9 10
}
```

### Parcourir tableau à deux dimentions
```java
int[][] nombres = { {1, 2, 3, 4}, {5, 6, 7} };
for (int i = 0; i < nombres.length; ++i) {
    for(int j = 0; j < nombres[i].length; ++j) {
        System.out.print(nombres[i][j]);
    }
} // => 1234567
```
## Les collections 

### différence entre List et collection

La liste est une interface et l'ArrayList est une classe du framework Java Collection. La liste crée un tableau statique et l'ArrayList crée un tableau dynamique pour stocker les objets. Ainsi, la liste ne peut pas être étendue une fois qu'elle est créée, mais en utilisant ArrayList, nous pouvons étendre le tableau si nécessaire.

Il est préférable d'utiliser l'interface de liste si vous souhaitez profiter du polymorphism (plusieurs signature pour une même méthode ). À l'avenir, si nous devons implémenter l'interface, nous n'aurons pas besoin de changer le programme.

### List
- C'est une interface
- Les éléments sont ordonnés
- A un index qui permet d'accéder aux éléments

```java
List<Type> nomListe = new Type de liste
List<String> personnes = new ArrayList<String>();
```
> ! Si on ne spécifie pas un *paramètre de type*, vous pourrez sotquer *n'importe quel* objet. 
> Cependant, lorsque vous accédez à un élément de la liste, vous allez devoir effectuer une conversion de type (ou cast ) afin de pouvoir l'utiliser. 
>Toute erreur risque de provoquer le plantage de votre programme.

#### Ajouter un élément

```java
personnes.add("toi"); 
personnes.add("moi");
personnes.add("Et tout ceux qui le veulent");
personnes.add("A remplacer");
personnes.add(0 , "Je veux être devant"); // avec choix de position

System.out.println(personnes);
// -> [Je veux être devant, toi, moi, Et tout ceux qui le veulent, A remplacer]
```

#### Remplacer un élément
`personnes.set(4, "A supprimer");` -> Remplace le 5ème élément qui se trouve à la position 4 par "A supprimer"
-> `[Je veux être devant, toi, moi, Et tout ceux qui le veulent, A supprimer]` 

#### Supprimer un élément
`personnes.remove(5);` -> supprimer le dernier élément 
-> `[Je veux être devant, toi, moi, Et tout ceux qui le veulent]`

#### Taille de la lise
`personnes.size();` -> 4

#### Supprimer tous les éléments
`personne.clear();`

#### Parcourir une liste
Plusieurs solutions :
```java
// 1. 
for (String element : personnes) {
    System.out.print(element + " / ");
} // => Je veux être devant / toi / moi / Et tout ceux qui le veulent / 

//2. 
for(int i=0; i<personnes.size(); i++) {
    System.out.print(personnes.get(i) + " / ");
}
```

#### Copier une liste