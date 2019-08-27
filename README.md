
# Infix Operators

## Using Infix Operators
In Scala, a method with one argument can be called as an infix operator

Using that rule, that’s what makes:


```scala
1.+(2)
```




    res47: Int = 3
    



Look like…​


```scala
1 + 2
```




    res48: Int = 3
    



## Creating your own infix operator

Therefore, in Scala, if we create our class like the following:


```scala
class Foo(x:Int) {
   def bar(y:Int) = x + y
}
```




    defined class Foo
    



and we want to invoke it, we can call it not only like this:


```scala
val foo = new Foo(40)
foo.bar(10) //non-infix
```




    foo: Foo = Foo@4a614812
    res49: Int = 50
    



but like this:


```scala
val foo = new Foo(40)
foo bar 10  // Called infix
```




    foo: Foo = Foo@60c14a11
    res50: Int = 50
    



## Infix Operator Conclusion

* If a method has one argument you can call it in an infix manner
* This is called an infix operator
