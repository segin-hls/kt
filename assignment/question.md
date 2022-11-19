
1, write a c++ program for LOG class and should use a "enum" for log-level.
   
* log-level should be as following :- 
	* INFO
	* Warn
	* ERROR
	* VERBOSE

* when we create a object we should be able to (select the log  level)
* default it should be set to "ERROR".
	
your main function should be:
```

int main(void)
{
   Log uartLog;
   uartLog.setLevel(Log::Verbos);
   uartLog.info("init of drivers complete ");
   uartLog.warn("drivers are not init properly ");
   uartLog.error("drivers are not installed ");
   uartLog.verbos("drivers for uart 1,2,3 has some error ");
}
```

output should be :-

```
[INFO]: init of drivers complete 
[WARN]: drivers are not init properly 
[ERROR]: drivers are not installed 
[VERBOS]: drivers for uart 1,2,3 has some error 

```

---

2, Split the log class into a library  and implement a Makefile 
* Makefile should contain
	* `make debug`
	* `make release`
	* `make clean`
	* `make clean_debug`
	* `make clean_release`

* debug files should be in a folder called debug & release files should be in folder called release .
* when you type `make`  `make debug`  should get executed
	
			
---
Q3, write a c++ program with base `class shape` which will have 2  functoins
* "shape()" which will take in two args 'width, height' which will be a 							setter function in the base class 			
* "area()" which will calculate the area of the shape

Then this base class will have two derived class `class rectangle` & `class triangle` which will inherit from the  `class shape` 
and there should be function called printArea() like this
```
printArea(Shape *shape);
```
and the funtion should print the area of rectange if rectange was passed as arg or the area of triangle if triangle was passed in.


---

did you goggle the formula for area of rectange & triangle?


`savage_level = answer ? "high":"low"`

		
