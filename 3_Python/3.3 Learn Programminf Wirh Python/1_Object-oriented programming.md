### Understanding Classes

The relationship between classes and objects is like the relationship between a blueprint and a building. The blueprint defines where the walls should be, but the house is made of bricks and mortar.

With a class, you can **instantiate** objects based on that blueprint. Those objects have the same **structure.**

A class contains **state** and **behavior.**

**State** refers to data or variables. A Person class might have a “name” variable, for instance.

A class’s **behavior** is simply a set of things that the class can do. This behavior is held in **methods,** which are identical in concept to functions.

For example, the Person class illustrated below is a blueprint specifying that a person has a name and can walk:

The blueprint has a “gap” for the person’s name. That’s because the blueprint itself is not a _real_ thing that exists in the world. When you make **(instantiate)** a person from that blueprint, the real person has a name.

The blueprint Person also has the method Walk(), which means all of the people made from that blueprint do as well (i.e., they all come with the behavior of walking).

### Differences between ***Method*** and a ***Function*** ?

**A method is part of a Class/Object**, while a function is independent of them. Methods can take parameters, modify the object's internal state, call other methods or functions, and return values.

>You **“call”** a function or method when you use it in code. For example, the line  `x = add(2, 3)`  calls the  `add`  function with the parameters 2 and 3.

Since a method is part of a class, it’s also part of an object that’s created from that class. The only difference between a function and a method is that methods are part of a class/object.

