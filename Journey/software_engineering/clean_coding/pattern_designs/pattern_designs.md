# Introduction

### What is a pattern design

    The pattern designs are common solutions for frequent  problems

A pattern consist on

- Purpose to explain the problem and the solution
- Motivation explain deep on details
- Structure shows the parts of the pattern and how it relates with others
- Example

## Clasification

- Creationals
- Structurals
- Behavior

## Creationals

The Creational patterns are design patterns that deal with object creation mechanisms, trying to create objects in a manner suitable to the situation.

Some common Creational patterns include:

- Singleton: Ensures a class has only one instance and provides a global point of access to it.

```ts
class Singleton {
  private static instance: Singleton;

  private constructor() {}

  public static getInstance(): Singleton {
    if (!Singleton.instance) {
      Singleton.instance = new Singleton();
    }
    return Singleton.instance;
  }
}
```

- Factory Method: Defines an interface for creating an object but lets subclasses alter the type of objects that will be created.

```ts
interface Product {
  operation(): string;
}

class ConcreteProductA implements Product {
  public operation(): string {
    return "Result of ConcreteProductA";
  }
}

class ConcreteProductB implements Product {
  public operation(): string {
    return "Result of ConcreteProductB";
  }
}

abstract class Creator {
  public abstract factoryMethod(): Product;

  public someOperation(): string {
    const product = this.factoryMethod();
    return `Creator: The same creator's code has just worked with ${product.operation()}`;
  }
}

class ConcreteCreatorA extends Creator {
  public factoryMethod(): Product {
    return new ConcreteProductA();
  }
}

class ConcreteCreatorB extends Creator {
  public factoryMethod(): Product {
    return new ConcreteProductB();
  }
}
```

- Abstract Factory: Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
- Builder: Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
- Prototype: Creates new objects by copying an existing object, known as the prototype.
