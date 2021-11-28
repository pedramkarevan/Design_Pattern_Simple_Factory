# Design_Pattern_Simple_Factory

Simple Factory Design Pattern
It is a creational design pattern; means that we are going to use this pattern when we are creating objects of a class.

What problem builder design pattern solves?

Multiple types can be instantiated and the choose is based on some simple criteria.

If (key. equalsIgnoreCase(“test”)) {
	//create test object
} else if (key. equalsIgnoreCase(“prod”)) {
	//create prod object
}

In this type of code simple factory is often used to work in exactly the same factory.

-	We simply move to the instantiating logic to a separate class and most commonly to a static method of this class.

-	It is a simple method that encapsulates object instantiation. Nothing complex goes on in that method.


UML Diagram:

We have a product class and it can be an interface or abstract class and we will have, multiple subclasses that implement our product interface or abstract class. Next up, we have a static simple factory, typically it is a separate class and inside of we have a static method that accept the parameter and depending upon the value of this parameter, we will decide which class to instantiate.

Step by step Implementation:

  1-	Creating separate class for our simple factory
  
      a-	Add a method which return desire object
      
          -	It is static method and accept some argument to decide which class instantiate
          
          -	You can provide additional arguments which will be used to instantiate objects
          
Design Consideration

  -	Simple factory will in turn may use other design pattern like builder to construct objects. So you are free to use any other design patterns inside of your method that instantiate objects
  -	In case you want to specialize your simple factory in sub classes, you need factory method design pattern instead.
