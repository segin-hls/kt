Write c++ program for LOG class and should use a "enum" for log-level.
   
* log-level should be as following :- 
	* INFO
	* WARN
	* ERROR
	* VERBOSE

* when we create a object we should be able to (select the log  level)
* default it should be set to "ERROR".
	
main function should be:-
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
