# resumeJava

# resume java perso

**Type de variable**
- int = 500; (nombre entier)
- double = 12.2; (nombre décimaux)
```java
int a = 10;
int b = 4;
double c = a / double b; // => 2.5  C'est du casting ( conversion d'une valeur dans un autre type)
```
- boolean nomVariable = true;
- char = "a"; ( un caractère )
- String = "texte";
- final int NOM_CONSTANTE = 340; ( une constante )
- float = 245.28; (nombre décimal moins précis que double. Float ne dépasse pas les 7 chiffres après la virgule )

##Lecture saisie utilisateur et afficher message de type String

```java
System.out.println("Veuillez entrer votre nom");
Scanner sc = new Scanner(System.in); // System.in : flux d'en trée de la console ( la lecture du clavier )
String nom = sc.nextLine(); // nextLine récupère le contenu. Si j'avais écris un entier dedans; Ex : 32 ENTER le scanner reçoit "32\n" . 
System.out.println(annee);
```
##Lecture saisie utilisateur et afficher message de type int

```java
        System.out.println("Veuillez entrer une année");
        Scanner sc = new Scanner(System.in);
        int annee = sc.nextInt(); // Quand je tape 32 ENTER le scanner reçoit "32\n" .
        System.out.println(annee);
```

##Conversion

**String**
```java
      int a =Integer.parseInt("9"); // integer en chiffre => 9
      double b = Double.parseDouble("100"); // => 100.0
      float e = Float.parseFloat("100"); // => 100.0
      short c = Short.parseShort("100"); // => 100
      Long d = Long.parseLong("123456789"); // => 123456789  
```
**Nombre vers string**
```java
int chiffre = 123;
String s = String.valueOf(chiffre); // valueOf est une méthode qui converti différents type de valeur en string
```

##StringFormat() - Mise en forme du texte
```java
String nom = "toi";
String phrase = String.format(" Bonjour %s", nom);
System.out.println(phrase); // => Bonjour toi
```





