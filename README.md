# Cour-sur-java

Le langage Java est un langage de programmation orienté objet, utilisé pour développer des applications sur diverses plateformes. Voici un guide complet sur les concepts clés du Java, de la syntaxe de base aux concepts avancés, avec des exemples pour chaque section.

### 1. **Introduction à Java**

Java a été créé par James Gosling chez Sun Microsystems en 1995. Il est conçu pour être simple, robuste et portable. Les programmes Java sont compilés en bytecode, qui peut être exécuté sur n'importe quelle machine équipée de la machine virtuelle Java (JVM).

### 2. **Structure de base d'un programme Java**

Un programme Java se compose généralement d'une classe contenant une méthode `main`, qui est le point d'entrée de l'application.

**Exemple :**
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### 3. **Types de données et variables**

Java est un langage typé statiquement, ce qui signifie que les types de variables doivent être déclarés.

- **Types primitifs** : `int`, `double`, `char`, `boolean`, etc.
- **Types de référence** : Les objets et les tableaux.

**Exemple :**
```java
int number = 10;
double price = 9.99;
char letter = 'A';
boolean isJavaFun = true;
```

### 4. **Opérateurs**

Java propose plusieurs types d'opérateurs : arithmétiques, relationnels, logiques, etc.

**Exemple :**
```java
int a = 5;
int b = 10;
int sum = a + b;
boolean isEqual = (a == b);
```

### 5. **Structures de contrôle**

Java propose des structures de contrôle pour gérer le flux d'exécution : `if`, `else`, `switch`, `while`, `for`, etc.

**Exemple :**
```java
int number = 20;

if (number > 0) {
    System.out.println("Positive number");
} else {
    System.out.println("Negative number");
}

for (int i = 0; i < 5; i++) {
    System.out.println("Iteration: " + i);
}
```

### 6. **Classes et Objets**

Java est un langage orienté objet. Une classe est un plan pour créer des objets, et un objet est une instance d'une classe.

**Exemple :**
```java
public class Person {
    String name;
    int age;

    // Constructeur
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Méthode
    public void displayInfo() {
        System.out.println("Name: " + name + ", Age: " + age);
    }

    public static void main(String[] args) {
        Person person1 = new Person("Alice", 30);
        person1.displayInfo();
    }
}
```

### 7. **Héritage**

L'héritage permet de créer une nouvelle classe basée sur une classe existante.

**Exemple :**
```java
class Animal {
    void eat() {
        System.out.println("This animal eats food");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.eat();
        myDog.bark();
    }
}
```

### 8. **Polymorphisme**

Le polymorphisme permet d'utiliser une méthode de différentes manières.

**Exemple :**
```java
class Animal {
    void sound() {
        System.out.println("This animal makes a sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("The dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Dog();
        myAnimal.sound();  // Cela appelle la méthode sound() de Dog
    }
}
```

### 9. **Interfaces**

Une interface en Java est une référence abstraite qui est utilisée pour regrouper des méthodes abstraites.

**Exemple :**
```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    public void sound() {
        System.out.println("The dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.sound();
    }
}
```

### 10. **Gestion des exceptions**

La gestion des exceptions est un mécanisme qui permet de gérer les erreurs lors de l'exécution d'un programme.

**Exemple :**
```java
public class Main {
    public static void main(String[] args) {
        try {
            int division = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero");
        } finally {
            System.out.println("This will always execute");
        }
    }
}
```

### 11. **Collections en Java**

Java propose des classes comme `ArrayList`, `HashMap`, `HashSet` pour gérer les collections de données.

**Exemple :**
```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Orange");

        for (String fruit : fruits) {
            System.out.println(fruit);
        }
    }
}
```

### 12. **Gestion des fichiers**

Java permet de lire et écrire des fichiers à l'aide de classes comme `File`, `FileReader`, `FileWriter`.

**Exemple :**
```java
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try {
            FileWriter writer = new FileWriter("example.txt");
            writer.write("Hello, File!");
            writer.close();
        } catch (IOException e) {
            System.out.println("An error occurred");
            e.printStackTrace();
        }
    }
}
```

### 13. **Programmation multi-thread**

Java supporte la programmation concurrente grâce à la classe `Thread` et l'interface `Runnable`.

**Exemple :**
```java
class MyThread extends Thread {
    public void run() {
        for (int i = 0; i < 5; i++) {
            System.out.println(i);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread thread1 = new MyThread();
        thread1.start();
    }
}
```

### 14. **Conclusion**

Java est un langage riche et puissant, largement utilisé dans le développement d'applications de bureau, web, mobiles, 
et pour des systèmes embarqués. Les concepts présentés ici ne sont que la 
base ; il existe de nombreux autres 
aspects plus avancés de Java comme les expressions lambda, les flux (streams),
la gestion des bases de données, etc.


Voici les solutions en Java pour chaque exercice :

### Exercice 1 : Affichage de paires de nombres

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 2; i <= 20; i += 2) {
            System.out.println(i);
        }
    }
}
```

### Exercice 2 : Somme des entiers avec `while`

```java
public class Main {
    public static void main(String[] args) {
        int somme = 0;
        int i = 1;

        while (i <= 10) {
            somme += i;
            i++;
        }

        System.out.println("La somme des entiers de 1 à 10 est : " + somme);
    }
}
```

### Exercice 3 : Inverser un nombre avec `do-while`

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un nombre entier : ");
        int nombre = scanner.nextInt();
        int nombreInverse = 0;

        do {
            int chiffre = nombre % 10;
            nombreInverse = nombreInverse * 10 + chiffre;
            nombre /= 10;
        } while (nombre > 0);

        System.out.println("Le nombre inversé est : " + nombreInverse);

        scanner.close();
    }
}
```

### Exercice 4 : Trouver le maximum d'une série d'entiers

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int max = Integer.MIN_VALUE;

        System.out.println("Entrez 5 nombres entiers :");
        for (int i = 0; i < 5; i++) {
            int nombre = scanner.nextInt();
            if (nombre > max) {
                max = nombre;
            }
        }

        System.out.println("Le plus grand nombre est : " + max);

        scanner.close();
    }
}
```

### Exercice 5 : Compter les paires de chiffres dans un nombre

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un nombre entier : ");
        int nombre = scanner.nextInt();
        int countPaires = 0;

        while (nombre > 0) {
            int chiffre = nombre % 10;
            if (chiffre % 2 == 0) {
                countPaires++;
            }
            nombre /= 10;
        }

        System.out.println("Le nombre de chiffres paires est : " + countPaires);

        scanner.close();
    }
}
```

Ces programmes utilisent les boucles `for`, `while` et `do-while` pour effectuer des tâches variées telles que l'affichage de nombres, la somme, l'inversion de nombres, la recherche du maximum et le comptage de chiffres pairs. Assurez-vous de tester ces programmes avec différentes entrées pour vérifier leur bon fonctionnement.





 Voici des solutions en Java pour chacun des exercices :

### Exercice 1 : Trier un tableau d'entiers

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] tableau = {5, 2, 9, 1, 5, 6};
        
        // Trier le tableau en ordre croissant
        Arrays.sort(tableau);
        
        // Afficher le tableau trié
        System.out.println("Tableau trié : " + Arrays.toString(tableau));
    }
}
```

### Exercice 2 : Filtrer les éléments paires d'un tableau

```java
public class Main {
    public static void main(String[] args) {
        int[] tableau = {1, 2, 3, 4, 5, 6};
        
        // Filtrer et afficher les éléments paires
        System.out.print("Éléments paires : ");
        for (int nombre : tableau) {
            if (nombre % 2 == 0) {
                System.out.print(nombre + " ");
            }
        }
    }
}
```

### Exercice 3 : Trouver le maximum et le minimum d'un tableau

```java
public class Main {
    public static void main(String[] args) {
        int[] tableau = {3, 5, 7, 2, 8};
        
        // Initialiser max et min avec la première valeur du tableau
        int max = tableau[0];
        int min = tableau[0];
        
        // Trouver le maximum et le minimum
        for (int nombre : tableau) {
            if (nombre > max) {
                max = nombre;
            }
            if (nombre < min) {
                min = nombre;
            }
        }
        
        // Afficher les résultats
        System.out.println("Max: " + max);
        System.out.println("Min: " + min);
    }
}
```

### Exercice 4 : Rechercher un élément dans un tableau trié

```java
import java.util.Arrays;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        int[] tableau = {1, 3, 5, 7, 9};
        
        // Demander à l'utilisateur d'entrer un nombre
        Scanner scanner = new Scanner(System.in);
        System.out.print("Entrez un nombre à rechercher : ");
        int nombreRecherche = scanner.nextInt();
        
        // Rechercher le nombre dans le tableau
        int index = Arrays.binarySearch(tableau, nombreRecherche);
        
        // Afficher le résultat
        if (index >= 0) {
            System.out.println("Index : " + index);
        } else {
            System.out.println("Le nombre n'est pas présent dans le tableau.");
        }
        
        scanner.close();
    }
}
```

### Exercice 5 : Supprimer les doublons d'un tableau

```java
import java.util.Arrays;
import java.util.HashSet;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        int[] tableau = {1, 2, 2, 3, 4, 4, 5};
        
        // Utiliser un Set pour éliminer les doublons
        Set<Integer> set = new HashSet<>();
        for (int nombre : tableau) {
            set.add(nombre);
        }
        
        // Convertir le Set en tableau
        Integer[] tableauSansDoublons = set.toArray(new Integer[0]);
        
        // Afficher le tableau sans doublons
        System.out.println("Tableau sans doublons : " + Arrays.toString(tableauSansDoublons));
    }
}
```

Ces programmes couvrent des opérations courantes sur les tableaux en Java, y compris le tri, le filtrage, la recherche, et la suppression de doublons. Assurez-vous de tester ces programmes pour vérifier leur bon fonctionnement avec différentes entrées.




Voici des solutions en Java pour chacun des exercices :

### Exercice 1 : Méthode de Calcul de la Somme

```java
public class Main {
    // Méthode pour calculer la somme de deux entiers
    public static int sum(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        // Appel de la méthode avec différents paramètres et affichage des résultats
        int result1 = sum(5, 7);
        int result2 = sum(10, 15);
        
        System.out.println("La somme de 5 et 7 est : " + result1);
        System.out.println("La somme de 10 et 15 est : " + result2);
    }
}
```

### Exercice 2 : Méthode de Vérification de Parité

```java
public class Main {
    // Méthode pour vérifier si un nombre est pair
    public static boolean isEven(int number) {
        return number % 2 == 0;
    }

    public static void main(String[] args) {
        // Utilisation de la méthode pour vérifier plusieurs nombres
        System.out.println("4 est pair : " + isEven(4));
        System.out.println("7 est pair : " + isEven(7));
        System.out.println("10 est pair : " + isEven(10));
        System.out.println("13 est pair : " + isEven(13));
    }
}
```

### Exercice 3 : Méthode de Calcul de la Factorielle

```java
public class Main {
    // Méthode pour calculer la factorielle d'un nombre entier positif
    public static int factorial(int n) {
        if (n == 0) {
            return 1;
        }
        int result = 1;
        for (int i = 1; i <= n; i++) {
            result *= i;
        }
        return result;
    }

    public static void main(String[] args) {
        // Test de la méthode avec différents nombres
        int result1 = factorial(5);
        int result2 = factorial(7);
        
        System.out.println("La factorielle de 5 est : " + result1);
        System.out.println("La factorielle de 7 est : " + result2);
    }
}
```

### Exercice 4 : Méthode de Surcharge

```java
public class Calculator {
    // Méthode pour multiplier deux entiers
    public static int multiply(int a, int b) {
        return a * b;
    }

    // Méthode surchargée pour multiplier deux nombres à virgule flottante
    public static double multiply(double a, double b) {
        return a * b;
    }

    public static void main(String[] args) {
        // Test des méthodes de multiplication
        int result1 = multiply(3, 4);
        double result2 = multiply(3.5, 4.2);
        
        System.out.println("Le produit de 3 et 4 est : " + result1);
        System.out.println("Le produit de 3.5 et 4.2 est : " + result2);
    }
}
```

### Exercice 5 : Méthode de Manipulation de Chaînes

```java
public class Main {
    // Méthode pour inverser une chaîne de caractères
    public static String reverseString(String str) {
        StringBuilder reversed = new StringBuilder(str);
        return reversed.reverse().toString();
    }

    public static void main(String[] args) {
        // Utilisation de la méthode pour inverser plusieurs chaînes
        String result1 = reverseString("hello");
        String result2 = reverseString("world");
        
        System.out.println("Chaîne inversée de 'hello' : " + result1);
        System.out.println("Chaîne inversée de 'world' : " + result2);
    }
}
```

Ces programmes en Java démontrent différentes fonctionnalités telles que les méthodes de calcul, la vérification de la parité, le calcul de la factorielle, la surcharge de méthodes et la manipulation de chaînes. Assurez-vous de tester ces programmes pour vérifier leur bon fonctionnement avec différentes entrées.

