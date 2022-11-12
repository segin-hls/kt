# KT c++ (not for noobs)*



## HelloWorld in c++

```
#include <iostream> // <- preprocessor Statement // header files
int main(void) // <-entery point
{
   std::cout << "HelloWorld" << std::endl; // <- code 
}
```

## Function OverLoading
```
#include <iostream> // <- preprocessor Statement // header files
#include <string>

using std::cout;

void printHello(void)
{
   cout << "HelloWorld!" << std::endl; // <- code 
}
void printHello(std::string name)
{
   std::cout << "Hello " << name << std::endl; // <- code 
}

int main(void) // <-entery point
{
    printHello();
    printHello("Luffy");

}
```

## RangeBasedForLoop

```
#include <iostream>
#include <vector>

int main(void)
{
    int arr[] = {1,2,3,4};
    std::vector <int> victor = {1,2,3,4,5,6};

    for(auto i : victor)
        std::cout << i << "\t";
    
    std::cout << std ::endl; 

    return 0;
}
```

## Lambada

```
#include <iostream>
#include <vector>
// #include <algorithm>

void forEach(std::vector <int>& values, void(*func)(int))
{
    for(int va : values)
        func(va);
}


int main (void)
{
    std::vector <int> values = {0,1,2,3,4,5};
    forEach(values, [](int value){std::cout << "Values" << std::endl;});
    forEach(values, [](int value){std::cout << value << std::endl;});
}

```
## Template

```
#include <iostream>

template <typename T >

void __print( T val)
{
    std::cout << val << std::endl;
}

int main()
{
    __print<int>(10);
    __print("Luffy");
    __print(3.15f);
}

```

## Class

```
#include <iostream>

namespace ply {
class Player //  "Player" <- this is obj 
{
    public:
        int m_x, m_y;   
        int m_speed;

    void Move(int xa, int ya) 
    {
        //do some stuff
        x += xa;
        y += ya;
        std::cout << "player moved" << std::endl;

    }
};
};


int main()
{
    ply::Player player; //   <- this is called instance

    player.x = 5;
    player.y = 7;
    player.speed = 1000;

    player.Move(10,10);

}

# Makefile

## main.cpp
```
#include "helloWorld.h"

int main ()
{
    SRC::PrintH per;
    per.printHello();
    per.printHello("luffy");
}

```

## helloWorld.h

```
#ifndef HELLO_WORLD_H
#define HELLO_WORLD_H


#include <iostream>
#include <string>

namespace SRC { 

class PrintH 
{

public:
    void printHello();
    void printHello(std::string name);
};

}


#endif
```
## helloworld.cpp
```
# include "helloWorld.h"


void SRC::PrintH::printHello()
{
    std::cout << "Hello World!" << std::endl;
}

void SRC::PrintH::printHello(std::string name)
{
    std::cout << "Hello " << name << std::endl;
}
```
##makefile
```
CXX=g++
INCDIRS=-I
OPT=-o0
CXXFLAGS=$(INCDIRS) $(OPT)
CXXFILES=main.cpp helloWorld.cpp
OBJECTS=main.o helloWorld.o
BINARY= bin 
	
all: $(BINARY)
$(BINARY): $(OBJECTS)
	$(CXX) -o $@ $^
	
%.o:%.cpp
	$(CXX) $(CXXFLAGS) -c -o $@ $^
clean:
	rm -rf $(BINARY) $(OBJECTS)
```
