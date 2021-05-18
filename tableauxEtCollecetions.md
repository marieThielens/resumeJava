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
## Les collections - List
- C'est une interface
- Les éléments sont ordonnés
- A un index qui permet d'accéder aux éléments
- Accepte les doublons
- Ne peut pas être instantié

```java
List<String> personnes = new ArrayList<String>();
```
