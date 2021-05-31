# Etapes à suivre ( Basé sur l'aquarium très simplifié)
- Des poissons : un nom , un age 
- des methodes : parler et dormir (interface )
- 3 espèces différentes de poisson ( énum + model (saumon, poissonRouge, thon) )

## Le dossier models ( fichier Poisson.java)

- Créer un dossier models dans le dossier src 
- Créer un fichier Aquarium ( new / javaClass / Poisson) 
- Je vais mettre le nom de mes poissons dans un dossier enums / fichier poissonsEnum

## Fichier PoissonsEnum

Enum est une classe spéciale qui contient un ensemble de "varibale" constante. Ici l'espèce de mes poissons.
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

Là où une classe abstraite doit être étendue et spécialisée, une interface nous dit juste que telle classe possède telle propriété. Les méthodes que la classe va utiliser
Il y aura donc de la declaration de méthode.

- Créer un dossier interface
- Créer un fichier Ipoisson ( new / interface / Ipoisson)
- Mettre les méthodes que mon poisson ( utilisé après dans models / Poisson.java )

```java
public interface Ipoisson {
    public void parler();
    public void dormir();
}
```
## Fichier Poisson ( models )

- implement : étendre l'interface Ipoisson. **extends** = étendre une classe. **implements** = étendre une interface

```java
package maison.models;
import maison.enums.PoissonsEnum; // importer mes enum
import maison.interfaces.Ipoisson; // Importer mon interface

// extends = étendre une classe / implements : étendre une interface
public abstract class Poisson implements Ipoisson {

    private PoissonsEnum espece; // Je vais chercher mon enum et j'appelle ma variable espece.
    private String nom;
    private int age;

    // Encapsulation = protéger mes champs
    // getters : ce que l'utilisateur pourra voir
    public int getAge(){ return this.age; } // la méthode get renvoie la valeur de la variable age
    public String getNom() { return this.nom; } // return poisson1.age
    public PoissonsEnum getEspece() { return this.espece; } // Je prends l'espèce de mon enum

    // setters : ce qui pourra être modifié par l'utilisateur
    public void setAge(int age) { this.age = age; } // poisson1(objetCourant).age : paramètre
    public void setNom(String nom ) { this.nom = nom; }
    public void setEspece(PoissonsEnum espece) { this.espece = espece; }

    @Override //  définir une méthode qui est héritée de la classe parente.
    public void parler() {
        System.out.println("Glou glou");
    }
    @Override
    public void dormir() {
        System.out.println("Zzzzzz");
    }

    // constructeur
    public Poisson(String nom, PoissonsEnum espece, int age) {
      //  super(); // Etendre le constructeur enfant au parent
        setAge(age);
    }
}
```

