# Introduction to Generics

## Learning Objectives
- Know what generics are
- Understand when we would use generics
- Understand how to make a simple generic class

## Task
Answer the following questions:
1. What is one benefit of using generics in Java classes?
- They make classes more flexible. If you need to create an object of a certain class that uses a different type from what is specified in the class, this isn't possible. One solution would be to create a second nearly identical class with one difference, being the property type, which is not DRY code and is hard to maintain. Generics can allow different types for a certain property, therefore the code is more flexible, as well as being more DRY and easier to maintain.

2. Name an example of a generic class that we have used in Java?
- ArrayLists are a generic class, which allow different types of objects can be specified.

3. What is the syntax for declaring a generic class?
- Declare a generic class with type placeholder variable(s) in between angle brackets: <T> or <E>. Then make use of placeholder in the class.

```
class Account<T> {
  private T id;
  private String name;

  public Account(T id, String name) {
    this.id = id;
    this.name = name;
  }
```

4. At what point does the generic type get specified?
- The generic type is specified when an instance of it is created, and the object name is put in place of the placeholder. At compile time, there are not two copies of the code - one generic and one specific; there is only one.

5. Can generic types be of primitive type?
- Generic types must be objects, therefore they cannot be primitive types.

6. Can a generic class take more than one type parameters?
- Yes, generic classes can take more than one type parameter. They must both be declared in the angle brackets separated by a comma, e.g.:

```
class Account<T, V> {
  private T id;
  private V name;

  public Account(T id, V name) {
    this.id = id;
    this.name = name;
  }
```
