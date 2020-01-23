<img alt="Logo" src="http://coderslab.pl/svg/logo-coderslab.svg" width="400">

# Java Prework - Snippety
> Krótkie kawałki kodu, które pokazują zależności, rozwiązują popularne problemy oraz pokazują, jak używać niektórych funkcji.


#### 1. Jakie zasady zachowujemy przy tworzeniu zmiennych?

Nazwy zmiennych powinny rozpoczynać się od litery `[a-zA-Z]` lub znaku podkreślenia `_` a zawierać dodatkowo mogą cyfry `[0-9]`.  
Pamiętamy, aby nazwy były opisowe.

#### 2. Konwersja String do int oraz int do String
```
String a = String.valueOf(2);   //integer do string
int i = Integer.parseInt(a); //string to int
```
Zwróć uwagę, że nie ma tutaj obsługi wyjątków.

#### 3. Jakie są rodzaje komentarzy w `java`?

 ```java
//komentarz jednolinijkowy


/*
 * komentarz
 * wielo- 
 * linijkowy
 */

komentarz dokumentacyjny
/** Main start method */
```

#### 4. Jak prawidłowo obliczać modulo (resztę z dzielenia)?

Koszyk z jabłkami przykładem działania modulo.

Obliczmy `12 % 4` (czytamy 12 modulo 4, a nie 12 modulo z 4):

```
Mamy 12 jabłek i chcemy dać każdemu po 4:

Dajemy Markowi 4 jabłka, zostaje nam 8.
Dajemy Jurkowi 4 jabłka, zostaje nam 4.
Dajemy Tomkowi 4 jabłka, zostaje nam 0.

Nie mamy wystarczającej liczby jabłek, aby dać kolejnej osobie 4 jabłka.
Nie pozostało nam ani jedno, więc nasza reszta z dzielenia to 0.
```

Obliczmy `11 % 3`:

```
Mamy 11 jabłek i chcemy dać każdemu po 3:

Dajemy Markowi 3 jabłka, zostaje nam 8.
Dajemy Jurkowi 3 jabłka, zostaje nam 5.
Dajemy Tomkowi 3 jabłka, zostają nam 2.

Nie mamy wystarczającej liczby jabłek, aby dać kolejnej osobie 3 jabłka.
Pozostały nam 2 jabłka, więc nasza reszta z dzielenia to 2.
```

Obliczmy `3 % 7`:

```
Mamy 3 jabłka, a chcemy dać każdemu po 7.

Nie mamy wystarczającej liczby jabłek, aby dać Markowi 7 jabłek.
Pozostały nam 3 jabłka, więc nasza reszta z dzielenia to 3.
```

Obliczmy `2 % 8`:

```
Mamy 2 jabłka, a chcemy dać każdemu po 8.

Nie mamy wystarczającej liczby jabłek, aby dać Markowi 8 jabłek.
Pozostały nam 2 jabłka, więc nasza reszta z dzielenia to 2.
```

#### 5. Jakie formy może przyjąć funkcja warunkowa `if` `else`?

1. Sama funkcja `if`
    ```java
    if (number > 5) {
       System.out.println("ok");
    }
    ```
   
2. Funkcja `if` z `else`
    ```java
    if (number > 5) {
      System.out.println("ok");
    } else {
       System.out.println("not ok");
    }
    ```   

3. Funkcja `if` z `else if`
    ```java
    if (number > 5) {
        System.out.println("ok");
    } else if (number > 3) {
        System.out.println("also ok");
    }
    ```   
   
4. Funkcja `if` z `else if` i `else`
    ```java
    if ( number > 5 ) {
        System.out.println("ok");
    } else if (number > 3) {
        System.out.println("also ok");
    } else {
        System.out.println("not ok");
    }
    ```   
   
5. Funkcja `if` z wieloma `else if` i `else`
    ```java
    if( number > 5 ) {
        System.out.println("ok");
    } else if (number > 3) {
        System.out.println("also ok");;
    } else if (number > 1) {
        System.out.println("another ok");
    } else {
        System.out.println("not ok");
    }
    ```  


#### 6. W jaki sposób użyć `break` do zatrzymania pętli przed warunkiem stopu?

```java
for (int i = 1; i < 500; i++) {
    System.out.println(i);
    if (i % 4 == 0){ //jeśli ten warunek zostanie spełniony
        break; //break przerwie pętlę for
    }
}
```


#### 7. Czy można wywołać pętlę `for` bez wszystkich 3 parametrów?

Tak, nic nie stoi na przeszkodzie, aby pominąć np. warunek stopu:

```java
for (int i=0; ; i++){
    //...
}
```

Taka pętla domyślnie będzie nieskończona, ponieważ nie ma warunku, który ją zatrzyma, oznacza to,  
iż w bloku pętli musimy dopisać warunek, który skorzysta z `break` i zatrzyma pętlę.  

Analogicznie sytuacja wygląda z pozostałymi argumentami, w skrajnym przypadku pętla może wyglądać tak:

```java
for (;;) {
    //...
}
```

Taka pętla, również jest nieskończona, a ewentualny warunek stopu oraz zmianę po pojedynczej iteracji musimy wykonać bezpośrednio w bloku pętli.


#### 8. Jak przeiterować po elementach tablicy?

Poniżej 2 sposoby:

```java
int[] myInt = new int[10];
for (int i=0; i<myInt.length; i++){
}
```

Można również użyć konstrukcji:
```
for (int item : myInt) {
    System.out.println("is: " + item);
}
```

#### 9. Jak pobrać ostatni i pierwszy element z tablicy?

```java
int[] myInt = {1, 3, 5, 7, 9};
int first = myInt[0];
int last = myInt[myInt.length-1];
System.out.println(first);
System.out.println(last);
```
