# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

Polymorphism means many shapes! 

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

In applying polymorphism we give allow our methods to take many different types of objects.

For example in Java, a method which takes a 'parent' as an argument can also accept any of that parents 'children' as arguments.

3. What can we use to implement polymorphism in Java?

We can implements using inheritance or implenetation of interfaces

4. How many 'forms' can an object take when using polymorphism?

As many as we like! Though the fewer the better.

5. Give an example of when you could use polymorphism.

A program may have a method which requires an object which is able to make a sale, by implementing an interface 'ISell' on any object you may wish to use you can pass an object of type ISell to your method.



# Composition and Aggregation

6. What do we mean by 'composition' in reference to object-oriented programming?

Composition refers to a 'HAS A' relationship in OOP.

7. When would you use composition? Provide a simple example in Java.

You may use composition when an objects members are complex and merit a class to themselves.

```java
public class Car {
    private Engine engine;
    private Gearbox gearbox;

    public Car(){
        this.engine = new Engine();
        this.gearbox = new Gearbox();
    }
}
```

In this example the Car object HAS A Engine and Gearbox, or you could say 'is composed of'.

8. Give a difference between composition and aggregation?

In composition, any members which are classes are created at the time the object is created. In the above example, creating a Car creates a new Engine and Gearbox.

In aggregation the Car would take existing instances of Engine and Gearbox when built. e.g.

```java
public class Car {
    private Engine engine;
    private Gearbox gearbox;

    public Car(Engine engine, Gearbox gearbox){
        this.engine = engine;
        this.gearbox = gearbox;
    }
}
```

9. What is/are the advantage(s) of using composition/aggregation?

The problem with composition is that if the Java garbage collector were to remove an instance of Car, the Engine and Gearbox will also be lost.

In Aggregation, the engine and gearbox objects will be retained if they are being used elsewhere in the program.

Using Compsition also means that each Car will be instantiate with a new Engine and Gearebox that have the same attributes.

10. When using composition, when an object is destroyed, what happens to all the objects it is composed of?

They are lost.

11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?

They are retained!