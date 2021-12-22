# OOPs-Notes
java opps notes  

Agenda of OOPs ::  

1. Class
2. Object
3. Data Hiding
4. Abstraction
5. Encapsulation

6) Relationship :-  IS - A relation (Inheritance )
                  a)  Single Inheritance
                  b)  multilevel Inheritance
                  c) Multiple inheritance
                  d) Cyclic Inheritance
                
                HAS - A realtion
                a) Aggregation
                b) Composition
                
7. Method Signature 
8. Polymorphism  :  
8.1) Overloading 
8.2) Overiding

9. static control flow
10. instance control flow 
11. Constructor 
12. Coupling
13. Cohension
---------------------------------------------------------------------

Class :-   Blueprint of an Object
           Logical Representation of an Object.
           
           Simple Example of Class

class Test
{

   int x; // instance variable 
   
public static void main(String[] args)
{
   int y; // local variable
   static int x=0; // static variable
   
   System.out.println("Hello");
}
}
           
Object :  Instance of a class is nothing but Ojbect . Object are real entity which exists in our life.

----------------------------------------------------------

3) Data Hiding :=> 

Our internal data should not go out directly that is outside person can't access 
our internal data directly.
 By using private modifier we can implement data hiding
 Note: recommended modifier for data members is private
 
 4) Abstraction : 

Hide internal implementation and just highlight the set of services, is called 
abstraction.
 By using abstract classes and interfaces we can implement abstraction.
 
Example : 
-----------
By using ATM GUI screen bank people are highlighting the set of services what they 
are offering without highlighting internal implementation.

abstract class Animal {
  // Abstract method (does not have a body)
  public abstract void animalSound();
  // Regular method
  public void sleep() {
    System.out.println("Zzz");
  }
}

// Subclass (inherit from Animal)
class Pig extends Animal {
  public void animalSound() {
    // The body of animalSound() is provided here
    System.out.println("The pig says: wee wee");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig(); // Create a Pig object
    myPig.animalSound();
    myPig.sleep();
  }
}


-------------------------------------------------------------------- ----------------------------------------- -----------------------

Encapsulation :

Binding of data and corresponding methods into a single unit is called 
Encapsulation .
If any java class follows data hiding and abstraction such type of class is said to 
be encapsulated class.

Encapsulation=Datahiding+Abstraction
                
The main advantages of encapsulation are : 
1. We can achieve security.
2. Enhancement will become very easy.
3. It improves maintainability and modularity of the application.
4. It provides flexibility to the user to use system very easily

Simple Example of Encapsulation :

public class Test {
   private String name;
   private String idNum;
   private int age;

   public int getAge() {
      return age;
   }

   public String getName() {
      return name;
   }

   public String getIdNum() {
      return idNum;
   }

   public void setAge( int newAge) {
      this.age = newAge;
   }

   public void setName(String newName) {
      this.name = newName;
   }

   public void setIdNum( String newId) {
      this.idNum = newId;
   }
}
public class RunEncap {

   public static void main(String args[]) {
       Test T = new Test();
       T.setName("Guru");
       T.setAge(19);
       T.setIdNum("17");

   System.out.print("Name : " + T.getName() + " Age : " + T.getAge());
   }
}
                
Tightly Encapsulation :

A class is said to be tightly encapsulated if and only if every variable of that class 
declared as private whether the variable has getter and setter methods are not , and 
whether these methods declared as public or not, these checkings are not required to
perform. nothing but Tightly Encapsulated class.

Example:

Which of the following classes are tightly encapsulated? 
class A {
int x=10; //not  if parent class var not private then no child class tightly encapsulated class.
}
class B extends A {
private int y=20; //not
}
class C extends B {
private int z=30; //not
}

Note: if the parent class is not tightly encapsulated then no child class is tightly 
encapsulated.

Fully Encapsulated Class  :- 

If any class members declared as private then class is known as Fully Encapsulated class wether methods are private or not.
Example of Fully Encapsulated: 

class Test
{
private int x;
private int y;
public static void main(String[] args)
{
    sop("hello");
}
}

------------------------
 
 
            
         
