# proposal-dot-last
`.last()` proposal for JavaScript 

## Motivation and use cases
In many languages there is an Enumerable#last method which allows you to return the last element of a sequence/ordered list of elements. Currently, to obtain the last item of an array you have to perform: 

```javascript
let array = [1,2,3,4,5];
const lastItem = array[array.length-1];
```

Examples of popular languages that already implement this method: 

- [Enumerable.Last (C#, C++, F#, VB)](https://msdn.microsoft.com/en-us/library/bb358775(v=vs.110).aspx?cs-save-lang=1&cs-lang=vb#code-snippet-1)

- [Ruby Array#last](https://ruby-doc.org/core-2.3.3/Array.html#last)

- [Clojure](https://clojuredocs.org/clojure.core/last#example-542692c8c026201cdc326a2c)

- [PHP `end()`](http://php.net/manual/en/function.end.php)


Developers should have a more erganomic, clear method of accessing the last item in aformentioned sequence. 

## Proposed Solution
 
A `.last()` method for Array.prototype (TODO: Maybe Collection?). 

```js
let someArray = [1,2,3,4,5,6,7,8];

console.log(someArray.last()) //would output 8
```
Overall this strives to promote readibility and syntactic sugar for dev erganomics.

### Empty, null, or undefined 
In an empty, null, or undefined property, it should return `undefined` (?)


