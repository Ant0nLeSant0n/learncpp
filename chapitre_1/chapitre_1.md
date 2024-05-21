### Chapitre 1 - C++ Basics

#### 1.1 - Statements and te structure of a program

`statement`  : Type d'instruction qui amène le programme à effectuer une action. Termine par `;`.

`function` : Collection de **statement** exécutée sequentiellement.

`#include <iostream>` : preprocessor directive - indique que nous voulons utiliser le contenu de la library **iostream** (read/write text from/to the console).

 ``` c++
 #include <iostream>

int main()
{
   std::cout << "Hello world!";
   return 0;
}
```

ci-dessus, `std::cout` pour **character output** et l'operateur `<<` permet d'afficher des informations sur la console.

`return` statement : indique que le programme c'est exécuté de façon correcte. Il retourne 0 à notre système d'exploitation, qui signifie "Tout c'est bien passé !".

#### 1.2 - Comments

```c++
// std::cout lives in the iostream library
std::cout << "Hello world!\n";
```
```c++
std::cout << "Hello world!\n";                 // std::cout lives in the iostream library
std::cout << "It is very nice to meet you!\n"; // this is much easier to read
std::cout << "Yeah!\n";                        // don't you think so?
```
```c++
/*
    std::cout << 1;
    std::cout << 2;
    std::cout << 3;
*/
```
#### 1.3 - Introduction to objects and variables
En c++, direct memory access est déprécié. la mémoire est indirectement accessible par d'un objet. 
Un objet est utilisé pour stocker une valeur en mémoire. Une variable est un objet qui a un nom(identifier).

**instantiation** : L'objet va être créé et assigné à une adresse mémoire. L'objet doit être instancié avant qu'il puisse être utlisé pour stocké une valeur.
**instancied object** est aussi appelé **instance**.

``` c++
int a;
double b;
```
``` c++
int a, b;
```
`=` est utilisé pour assigner une variable.


**Initialization** :
```c++
int width { 5 }; // define variable width and initialize with initial value 5
// variable width now has value 5
```
```c++
int a;         // no initializer (default initialization)
int b = 5;     // initial value after equals sign (copy initialization)
int c( 6 );    // initial value in parenthesis (direct initialization)

// List initialization methods (C++11) (preferred)
int d { 7 };   // initial value in braces (direct list initialization)
int e = { 8 }; // initial value in braces after equals sign (copy list initialization)
int f {};      // initializer is empty braces (value initialization) / initialization to value 0
```
>**Best Practice**
>Prefer direct list initialization (or value initialization) for initializing your variables.
>>int a, b( 5 );
>>int c, d{ 5 };


Unused initialized :
```c++
[[maybe_unused]] double pi { 3.14159 };
 ```

 #### 1.5 - Introduction to iostream: cout, cin, and endl

 ```c++
std::cout << "Hello world!"; // print Hello world! to console
  ```
  Nous utilisons std::cout avec **`<<`** **insertion operator** afin d'envoyer le text *Hello World!* a la console pour être affiché.

```c++
std::cout << "x is equal to: " << x;
```
L'enchainement des **`<<`** permet de concatainer du text.

```c++
std::cout << "Hi!" << std::endl; // std::endl will cause the cursor to move to the next line
```S
**`std::endl`** est utilisé afin de sauter une ligne.

>**Best Practice**
> Output a newline whenever a line of output is complete.
