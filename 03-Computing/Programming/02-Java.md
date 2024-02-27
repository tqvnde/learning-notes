# Java Programming

## videos
* udemy: Professional Java
* udemy: Java Insel
* [youtube Bro Code](https://www.youtube.com/playlist?list=PLZPZq0r_RZOMhCAyywfnYLlrjiVOkdAI1)
* [youtube Coding with John](https://youtu.be/bCPClyGsVhc): Generics

## Talks
* Venkat
* Robert Martin
	* [Functional Programing: What? Why? When?](https://www.youtube.com/watch?v=7Zlp9rKHGD4)


## books
* Head First Java --> Step by Step
* Effective java
* Cay Hostmann Big Java & OO Design 
* The Java Tutorial, A short course on the Basics https://docs.oracle.com/javase/tutorial/
* Java 24 Hours Trainer

## tutorials
* Java Complete References (pdf)
* [Java 11 docs](https://docs.oracle.com/en/java/javase/11/docs/api/index.html)
* https://www.tutorialspoint.com/online_java_compiler.php
* [yet another insignificant programming notes](https://www3.ntu.edu.sg/home/ehchua/programming/index.html)
* [zcode](https://zetcode.com/all/#java)
* [GameTutorial](https://gametutorial.bozjatorium.com/tutorials)

## Topics to learn

### Part I core languages
* OOP I: Classes, Objects, Encapsulations, Abstraction, Interface, Inheritance, Polymorphism  
* OOP II: Advanced --> OOAD, Design patters
* Enums
* Exceptions
* IO
* Regular expressions
* Generics: generic classes, methods, constrains (extends only), multiple generics, wildcard (for collections/wrapper of type parameters  eg. list of , comparable of)
* Optional
* Collections I: Iteration, Cooperation
* Collections II: Data Structures and Algorithms (List, Trees, Maps)
* Lambda, functional 
* Streams 

### Part II utilities
* Concurrency I  Multithreding --> OS
* Concurrency II Parallel
* Networking (Socket)
* Databases I
* Databases II
* GUI I Even driven
* GUI II Images, Animations, Games
* JAR
* Distributed Computing
* XML, Web, Frameworks 


## Topics in details
* [] Enums
	* John https://www.youtube.com/watch?v=wq9SJb8VeyM
	* Bro 
* [x] Exceptions
	* introduction: try, catch, multiple catch, finally
		* Bro: https://www.youtube.com/watch?v=adTDlH0lhaA
		* John: https://www.youtube.com/watch?v=1XAfapkBQjk
	* checked and unchecked exeptions:
		* John: https://www.youtube.com/watch?v=bCPClyGsVhc
	
	* custom exeptions:
		* Bro: https://www.youtube.com/watch?v=XhH93_woZIY
		* John: https://www.youtube.com/watch?v=OIozDnGYqIU&t=17s

* [x] regular expresions
	* https://regex101.com/
	* https://www.tutorialspoint.com/java/java_regular_expressions.htm
	* https://www.w3schools.com/java/java_regex.asp
	* https://www.youtube.com/watch?v=3DDLJOExiWM

* [ ] Generics: generic methods, generic classes, multiple generic parameters, return generics, bound generics, wildcards
	* John: https://www.youtube.com/watch?v=K1iu1kXkVoA
	* Bro: https://www.youtube.com/watch?v=jUcAyZ5OUm0
	* https://www.baeldung.com/java-generics-type-parameter-vs-wildcard
	* https://levelup.gitconnected.com/generics-and-wildcards-in-java-1e678f7792

* [ ] Java Collections
* [ ] Data Structures

* [ ] Lambda expressions	
	* Bro: https://www.youtube.com/watch?v=LEJ1kGHSXdA&t=667s
	* John: https://www.youtube.com/watch?v=tj5sLSFjVj4&t=7s
	* Udemy:Holczer
* [ ] Functional Programming
	* Venkat
		* Functional Programming with Java https://www.youtube.com/watch?v=15X0qFtBqiQ&t=2565s
		* Lambda and Streams https://www.youtube.com/watch?v=1OpAgZvYXLQ&t=6596s
	* Amigoscode
		* Java Functional Programming Full course https://www.youtube.com/watch?v=VRpHdSFWGPs&t=1045s
* [ ] Streams
	* Udemy
	* Joe https://www.youtube.com/watch?v=t1-YZ6bF-g0

* [ ] Multithreading 
	* John: https://www.youtube.com/watch?v=r_MbozD32eo&t=322s
* [ ] Parallel Programming
	* Vencat
		* https://www.youtube.com/watch?v=0hQvWIdwnw4&t=10429s
		* https://www.youtube.com/watch?v=9ueIL0SwEWI
* [ ] Distributed Programming
* [ ] Networking (Socket)

* [ ] Reactive Programming 
* [ ] Design Patterns --> 
	* https://refactoring.guru/design-patterns/java
	* https://sourcemaking.com/design_patterns


* [x] Event Programming
* [ ] Simple GUI


* [ ] XML
* [ ] SQL/JDBC
* [ ] Java2D
* [ ] Simple 2D Games

* [ ] javaFX
* [ ] JNI
* [ ] RMI distributed
* [x] jar: executable and library


  
### Tools
* [Online Compiler](https://www.onlinegdb.com/)
* [codingground Java](https://www.tutorialspoint.com/compile_java_online.php)
* jdk--> add path and classpath  environment variable

#==========================================================================================
# Java Programming OBSOLETED
* [How to create jar file](https://low-orbit.net/java-how-to-create-an-executable-jar-file)
* [zetcode Java all topics](https://zetcode.com/all/#java)
* [zetcode Java GUI](https://zetcode.com/javaswing/) - [code](https://github.com/janbodnar/Java-Swing-Examples)
* [zetcode Java 2D graphics](https://zetcode.com/gfx/java2d/) - [code]()
* [zetcode Java 2D games](https://zetcode.com/javagames/) - [code](https://github.com/TKUIM/zetcode)
* [GameTotorial](https://gametutorial.bozjatorium.com/)
* https://www.mathematik.uni-marburg.de/~thormae/lectures/graphics1/graphics_2_2_eng_web.html#1
* https://web.mit.edu/6.005/www/sp14/psets/ps4/java-6-tutorial/components.html
## 1 - Command line tools
### no package:
src
src/HelloWorld.java
bin
bin/HelloWorld.class

* compile: javac -d bin src/*.java
* run: 
  * java -cp bin HalloWorld
  * cd bin and java HelloWorld
* create jar file cd bin
  * jar cfe HelloWorld.jar HelloWorld HelloWorld.class

### with package
* javac -d bin src/HelloWorld.java
* java -cp bin com.programming.HelloWorld
* (in bin) jar cfe HelloWorld.jar com.programming.HelloWorld com/programming/HelloWorld.class
