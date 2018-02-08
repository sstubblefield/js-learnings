# Advanced JavaScript Concepts

* Chrome DevTools
* Specification
	- ES6
* Object Constructors
* Babel vs TypeScript
  * TypeScript - subset of js, bleeding edge js
* Closures
  * Closures get involved when a returned function isn't self-contained.
  ```javascript
  function youSayGoodbye() {
    alert('Good Bye!');

    function andISayHello() {
      alert('Hello!');
    }

    return andISayHello();
  }
  ```
  * When JavaScript detects that an inner function relies on variables stored by an outer function, **it ensures those variables are available even if the other function goes away**.
  * A closure is a function that relies on its outer function's context.

* Functional Programming
  * A Functions-first paradigm, a code style
  * higher-order functions - map, reduce, filter, instead of "for"
    * https://danmartensen.svbtle.com/javascripts-map-reduce-and-filter
  * Immutable - data that can't be changed
    * mutation - non-*function*al
    * persistent data structures for efficient immutability
      * Mori, Immutable.js
      * structural sharing
        * adding to an array for immutability vs creating a new array with the changed indexes
* Global Namespace
* IIFE & Modules
  * IIFE - *Immediately Invoked Function Expression*
    * http://benalman.com/news/2010/11/immediately-invoked-function-expression/
    * Give it a descriptive name
	* function scoping
  ```javascript
  // Before
  var foo = "foo";

  // function bob ( ) {
  //   var foo = "foo2";
  //   console.log(foo);
  // };
  // bob(); // bob, () - function

  (function IIFE(bar) {
    var foo = "foo2";
    console.log(foo);
  })(foo); // alias for bar

  console.log(foo);
  ```

* Prototypes
	* Prototypical Inheritance
* Functions
	* Anonymous Function
  * Named Function
* this Keyword

* coercion
* object wrappers