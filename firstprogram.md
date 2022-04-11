# Impulse chimera - your first program
Impulse chimera is a new language where you can mix and match languages in creating your program! Based in C++, this language provides access to low level hardware while
still abstracting enough to keep the language high level.


Because of this, making a simple hello world program just doesn't do the language justice. This example will use 3 programming languages, and combine them!


```C++
// file: main.imp

#include <iostream>

using language python;
using language nodejs;

using namespace std;

int main() {

  int number = 2;
  nodejs !!{
    number++
  }!!
  python !!{
    number += 1
  }!!
  
  cout << number; // output: 4
}
```

then compile it using chimeracc

```sh
chimeracc main.imp -o main
./main # output: 4
```


explanation of syntax:

This program appears to be a standard C++ program until you hit nodejs and then two exclamation points. the exclamation points can be replaced with any 
"Unique token" the only requirements are that the token must not appear in the subsection which is scoped.
