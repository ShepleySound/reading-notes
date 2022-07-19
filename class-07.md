# Class 07

## Domain Modeling

1. Explain why we need domain modeling.  
Domain modeling allows us to better understand problems by modeling them using real-world entities and those entities' relationships and responsibilities. It involves creating conceptual models that helps developers turn problems into solutions, and solutions into code.

## HTML Table Basics

1. Why should tables not be used for page layouts?  
The markup for using tables to handle page layout is pretty complex, and is not only unintuitive, but is also a big hassle for screen readers. CSS has layout techniques that are far more efficient and do not require overcomplicating the page's markup.
2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.  
   - `<thead>` wraps around a table row to identify it as containing the table's column headers.
   - `<tbody>` wraps around most of the rest of the table rows to identify them as the body of the table.
   - `<tfoot>` wraps around a set of rows, typically to summarize the rest of the rows or provide a final set of information that does not fit in with the body.

## Introducing Constructors

1. What is a constructor and what are some advantages to using it?  
A constructor is contained inside of an object's definition, and allows us to define default properties and methods of an object, and to then create instances of that object. If we had a `Dog` constructor, we could then create a copy of that defined object using `const newDog = new Dog();`. Constructors make it easier to create objects that share properties, but whose properties contain unique values.
2. How does the term `this` differ when used in an object literal versus when used in a constructor?  
When used in an object literal, `this` refers to that *specific* object. If used inside of an object called `menu`, it will refer to that `menu` object. <br>When using constructors, we are creating new *instances* of an object. In this case, `this` refers to the object instance.

## Object Prototypes Using a Constructor

1. Explain prototypes and inheritance via an analogy from your previous work experience.  
2. 
The idea of inheritance and prototypes actually pairs really well with electronic sound design. For example, a synthesizer could be modeled using an object, and the modules inside of the synthesizer can be further broken down into smaller objects.  

Every synthesizer needs some sort of way to start and stop notes. These `start()` and `stop()` methods could be defined on the prototype of the `Synthesizer`, and so every instance of Synthesizer would receive those methods and know how to use them.  

There are many types of synthesizers, but, as stated earlier, they share many modules and features. Every `Synthesizer` has at least one `oscillator` (which produces sound) and some form of `amplitude` module (which controls the volume of the sound). Using the prototype methods from before and these two basic modules, we could create a very basic `Synthesizer` object constructor!

To go deeper, we could move towards creating a traditional `Monosynth`. We would set it to inherit from the `Synthesizer`, and then we would need to add a `filter` (Which lets us 'shape' the tone). If we create an object using this new constructor, we would get an object whose type is `Monosynth`, but that inherits properties and methods from the `Synthesizer` class/constructor.