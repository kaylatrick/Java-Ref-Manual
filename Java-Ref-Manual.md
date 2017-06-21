# Java Reference Manual

## values //K
raw data assigned to a variable

Ex: '4' is a value being assigned to variable x below.
var x = 4;

## operations //L
## variables //T
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
## arrays //K
## the uses of . [] {} ; //L
## access modifiers (public, private, protected) //T
## exceptions //K
## generics //L
## abstract classes, abstract methods //T
## enums //K
## anonymous inner classes, lambdas //L
## important classes of the standard library //T
