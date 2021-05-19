# Etapes à suivre ( Basé sur l'aquarium )

## Le fichier models

- Créer un dossier models dans le dossier src 
- Créer un fichier Aquarium ( new / javaClass / Poisson) 
- Je vais mettre le nom de mes poissons dans un dossier enums / fichier poissonsEnum

## Fichier PoissonsEnum

Enum est une classe spéciale qui représente un groupe de constante. Ici l'espèce de mes poissons.
- Créer un dossier enums
- Dans ce dossier créer un fichier poissonsEnum ( new / enum / poissonEnum) 

```java
public enum PoissonsEnum {
    THON,
    SAUMON,
    POISSON_ROUGE
}
``` 

## Dossier interface / Fichier Ipoisson

Là où une classe abstraite doit être étendue et spécialisée, une interface nous dit juste que telle classe possède telle propriété, indépendamment de ce qu'elle représente.
Il y aura donc de la declaration de méthode.

- Créer un dossier interface
- Créer un fichier Ipoisson ( new / interface / Ipoisson)

```java
interface Ipoisson {
    public void parler();
}
```
## Fichier Poisson ( models )

