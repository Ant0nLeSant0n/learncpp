### Chapitre 1 - C++ Basics

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

Ceci est un test

