---
layout: post
title:      "Object Orentation (OO)"
date:       2021-01-25 10:17:17 +0000
permalink:  object_orentation_oo
---

Over the past few months, we have been learning to code using Ruby and JavaScript across different frame works. As a programming language there is one main similarity between Ruby and JavaScript which is that they are both Object Oriented languages. Object Orientation is a programming model that enables us to create a single entity (an object) that has both data and behaviors, it helps us write more organized and reusable code. 

**Ruby as Object Oriented Language**
 
Ruby is an object-oriented programming language, which means it manipulates programming constructs called objects. Almost everything in Ruby is an object. Objects have methods and attributes, which are just data. Class variables are attached to the class in which they are declared. A class variable should be declared with two @ symbols and are called Instance variables which hold a value specific to each instance of that class, not to all members of the class itself. A *new* class instance can be created by calling the .new method of the class. Arguments to the class’ *initialize* method can be passed in to the .*new* call. An i*nitialize* method is used to generate new instances of the class. It is usually the first method of a class.  
Defining a class in Ruby :  [sources](https://www.codecademy.com/learn/learn-ruby/modules/learn-ruby-object-oriented-programming-part-i-u/cheatsheet)
```

class Child
  @@children = 0
  def initialize(name, birth_year)
    @name = name
    @birth_year = birth_year
    @@children +=1
  end
 
  def self.children_added
    return @@children
  end
 
end
 
naomi = Child.new("Naomi", 2006)
bertha = Child.new("Bertha", 2008)
 
puts Child.children_added 
```



**JavaScript as Object Oriented Langauge **

JavaScript has prototype-based object orientation. Although we can create objects in many ways, class syntax is the newest way to do so.  Even with the addition of classes, JavaScript is prototype-based rather than class-based. In prototype-based languages our instances inherit from a working JavaScript object. There are a few ways that we can generate JS objects but all of them generate objects that align with prototypical Object Orientation.

*  Literal Syntax
*  Factory Functions
*  Constructor Functions
*  Classes

[Class-base vs Function-based languauges](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Details_of_the_Object_Model#class-based_vs._prototype-based_languages)
```
Defining a Class in JavaScript 
class Employee {
  constructor() {
    this.name = '';
    this.dept = 'general';
  }
}
Defining a Function in JavaScript 
function Employee() {
    this.name = '';
    this.dept = 'general';
}

```
In conclusion, using Object Orienanted Programming  makes things easier if you’re writing a non-trivial program. BecauseObject Orienanted Programming is all about how you design & organize your code. You create classes that represent concepts in your program. And each class is responsible for doing something.

