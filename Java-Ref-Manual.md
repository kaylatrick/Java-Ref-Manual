# Java Reference Manual

## values //K
raw data assigned to a variable

Ex: '4' is a value being assigned to variable x below.
var x = 4;

## operations //L
## variables //T
A variable is a piece of memory that store a data value.
Example:
int dataValue;
dataValue = 100;
int myInfo = 200;

## if else //K
If / else statements are conditional statements. The condition must be true in order to execute code within the if brackets {}, otherwise, the code within the else brackets {} will be executed.

  Ex:
  var x = 4;
  if (x > 3) {
    console.log("X is greater than 3!");
    } else {
      console.log("X is not greater than 3.");
    }
  }

## while //L
## for //T
The for statement (Loop) provides a compact way to iterate over a range of
values until a particular condition is met.
Example:
for(int i=1; i<3; i++){
System.out.println("Count is: " + i);
}

The output is:
Count is: 1
Count is: 2
Count is: 3

## primitive types //K

- int
- boolean: true/false
- long:
- short
- byte:
- float
- double
- char

## reference types //L
## classes / instances //T
A class is nothing but a blueprint or a template for creating different objects which defines
its properties and behaviors.
Example:
class Employee {
	int age;
	double salary;
	int position;
}

## instance fields //K
a field belonging to a class whose value only applies to one instance of the class

Ex: "name" and "numLives" are static fields.
class Cat {
  public String name;
  public int numLives;
  public Cat(name, numLives) {
    name = this.name;
    numLives = this.numLives;
  }
  public int getNumLives() {
    return this.numLives;
  }
  public static void main(String[] args) {
    Cat c = new Cat("Smokey", 16);
    int cNumLives = c.getNumLives();
    System.out.println(cNumLives);
  }
}

## instance methods //L
## static fields //T
Static fields are used to share information among multiple objects of a class.
A static field of a class is often referred to as a class variable because static
field is associated with a class and not with individual instances of the class.
A static field gets memory only once for the whole class no matter how many objects
of a class are created. To declare a static field, prefix the field declaration
in the class with the static modifier. Its syntax is, static datatype fieldName;
Example:
class Student8{
   int rollno;
   String name;
   static String college ="IUPUI";

   Student8(int r,String n){
   rollno = r;
   name = n;
   }
 void display (){System.out.println(rollno+" "+name+" "+college);}

 public static void main(String args[]){
 Student8 s1 = new Student8(111,"Karan");
 Student8 s2 = new Student8(222,"Bob");

 s1.display();   // Output: 111 Karan IUPUI
 s2.display();  //  Output: 222 Bob IUPUI
 }

## static methods //K
a method that applies to the entire class and does not change amongst instances

Ex:
public static Connection insertConnect() {
  // SQLite connection string
  String url = "jdbc:sqlite:TwitterClone.db";
  Connection conn = null;
  try {
    conn = DriverManager.getConnection(url);
  } catch (SQLException e) {
    System.out.println(e.getMessage());
  }
  return conn;
}

## this //L
## constructors //T
A constructor is used to initialize the object.  A constuctor looks like a method and is
sometimes called a constructor method.
However, unlike a method a constructor does not have a reutrn value, not even void.
Also a constructor must have the same name as the class.
There are two types of constructors:
1. Default constructor (no-arg constructor)
	a) Its syntax is, <class_name>(){}  
	Example -
	class Bike1	{  
		Bike1(){System.out.println("Bike is created");
	}  
	public static void main(String args[])	{  
		Bike1 b=new Bike1();  
	}  
}   
2. Parameterized constructor
	a) Its sytax is as follows:
	constructorName (listOfArguments)  {
		[constructor body]
	}
Example:
public class Employee	{
	public int age;
	public double salary;
	public Employee()  {
	}
	public Employee(int age 8, double salary 3500)  {
		age = 8;
		salary = 3500;
	}
}

## "new" operator //K
operator that creates a new instance of a class

Ex:
class Cat {
  public String name;
  public int numLives;
  public Cat(name, numLives) {
    name = this.name;
    numLives = this.numLives;
  }
  public int getNumLives() {
    return this.numLives;
  }
  public static void main(String[] args) {
    Cat c = new Cat("Smokey", 16); //This creates a new Cat instance
    int cNumLives = c.getNumLives();
    System.out.println(cNumLives);
  }
}

## inheritance //L
## super //T
The super keyword in java is a reference variable which is used to refer immediate
parent class object. Whenever you create the instance of subclass, an instance
of parent class is created  implicitly which is referred by super reference variable.
For Example:  It is used if parent class and child class have same fields
	class Animal{  
	String color="white";  
	}  
	class Dog extends Animal	{  
	String color="black";  
	void printColor(){  
	System.out.println(color);  //prints color of Dog class  
	System.out.println(super.color);  //prints color of Animal class  
	}  
}  
	class TestSuper1{  
	public static void main(String args[])	{  
	Dog d=new Dog();  
	d.printColor();  
}}  
This output is:
black
white

## overloading //K
occurs when two or more methods in one class have the same method name (by inheritance) but different parameters

Ex:
class Animal {
  public int getSpeedMPH() {
    return 4;
  }
}
class Cheetah extends Animal {
  public int getSpeedMPH() {
    return 20;
  }
  public int getSpeedMPH(x) { //this is overloading
    return 20 + x;
  }
}

## overriding //L
## packages //T
A java package is a group of similar types of classes, interfaces and sub-packages.
Package in java can be categorized in two form, built-in package and user-defined package.
There are many built-in packages such as java, lang, awt, javax, swing, net, io, util, sql etc.

## interfaces //K
contains a set of methods that can be implemented by any class that contains those common methods

Ex:
interface Cat {
  int numLives();
  void meow();
  int jumpThisHigh(age);
}

class Mainecoon implements Cat {

}

## casting //L
## instanceof operator //T
The instanceof operator is used to test whether the object is an instance of the specified type
(class or subclass or interface). The instanceof is also known as type comparison
operator because it compares the instance with  type. It returns either true or false.
If we apply the instanceof operator with any variable that has null value, it returns false.
Example:
	class Dog1{  
	public static void main(String args[])	{  
 	Dpg1 d=new Simple1();  
	System.out.println(s instanceof Dog1);    //true  
	}  
}  

## arrays //K
## the uses of . [] {} ; //L
## access modifiers (public, private, protected) //T
Access modifiers determine control accessibility to classes, interfaces, fields,
constructors and methods.
1. The access modifier "public" is used to make a class member visible to the world.
For example:
 public class Dog {
    public String name;

     public void bark() {
        System.out.print("Gow Gow!");
    }
}
2. The access modifier "protected" is used to make a class member protected
that can only be accessed within its own package.
For Example:
package animal;

public class Dog {
    protected void waveTail() {
        System.out.print("Waving my tail...");
    }
}
3. The access modifier "private" is only accessiable from within the enclosing class.  
No Nothing outside the class can access a private member.
For Example:
package animal;

public class Dog {

    private String breed;

    public Dog() {
        breed = "Bull";
    }
}

## exceptions //K
## generics //L
## abstract classes, abstract methods //T
An abstract class is a class that is declared abstract—it may or may not include abstract methods.
Abstract classes cannot be instantiated, but they can be subclassed.
An abstract method is a method that is declared without an implementation (without braces,
and followed by a semicolon), like this:
For Example:
1. Declaration using abstract keyword
   abstract class AbstractDemo{
2. Concrete method: body and braces
   public void myMethod(){
      //Statements here
   }
3. Abstract method: without body and braces
   abstract public void anotherMethod();
}

## enums //K
## anonymous inner classes, lambdas //L
## important classes of the standard library //T
The most important classes are Object, which is the root of the class hierarchy,
and Class, instances of which represent classes at run time.
