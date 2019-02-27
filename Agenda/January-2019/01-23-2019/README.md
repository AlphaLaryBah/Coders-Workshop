# Recursion

[Slides](https://slides.com/bbyunis/coder-s-workshop)

## Challenge 1: repeater

> Write a function that takes an input character and returns that character repeated 5 times using recursion. For example, if the input is '**g**', then the output should be '**ggggg**'.

```javascript
console.log(typeof repeater); // 'function'
console.log(repeater("g")); // 'ggggg'
console.log(repeater("j")); // 'jjjjj'
```

[solve in JavaScript](https://repl.it/@andy_young/repeaterjs)

[solve in Python](https://repl.it/@andy_young/repeaterpy)

---

## Challenge 2: getLength

> Get the length of an array using recursion without accessing its length property.

```javascript
console.log(getLength([1])); // -> 1
console.log(getLength([1, 2])); // -> 2
console.log(getLength([1, 2, 3, 4, 5])); // -> 5
console.log(getLength([])); // -> 0
console.log(getLength([undefined])); // -> 1
```

[solve in JavaScript](https://repl.it/@andy_young/getLengthjs)

[solve in Python](https://repl.it/@andy_young/getLengthpy)

---

## Challenge 3: fibonacci

> The Fibonacci numbers are the numbers in the following integer sequence (Fn):

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, ...

such as

F(n) = F(n-1) + F(n-2) with F(0) = 0 and F(1) = 1.

Given a number, say prod (for product), we search two Fibonacci numbers F(n) and F(n+1) verifying

`F(n) * F(n+1) = prod`

`21 * 34 = 714`

Your function productFib takes an integer (prod) and returns an array:

`productFib(714) // should return [21, 34, true]`

If you don't find two consecutive F(m) verifying F(m) \* F(m+1) = prod, you will return

`[F(m), F(m+1), false]`

F(m) being the smallest one such as F(m) \* F(m+1) > prod.

Examples:

```javascript
productFib(714); // should return [21, 34, true],
// since F(8) = 21, F(9) = 34 and 714 = 21 * 34

productFib(800); // should return [34, 55, false],
// since F(8) = 21, F(9) = 34, F(10) = 55 and 21 * 34 < 800 < 34 * 55
```
[See Codewars.com (JavaScript)](https://www.codewars.com/kata/product-of-consecutive-fib-numbers/javascript)

[See Codewars.com (Python)](https://www.codewars.com/kata/product-of-consecutive-fib-numbers/python)

## :feelsgood: Hard Mode: Rotate for a Max
Take a number: `56789`. Rotate left, you get `67895`.

Keep the first digit in place and rotate left the other digits: `68957`.

Keep the first two digits in place and rotate the other ones: `68579`.

Keep the first three digits and rotate left the rest: `68597`. Now it is over since keeping the first four it remains only one digit which rotated is itself.

You have the following sequence of numbers:

`56789 -> 67895 -> 68957 -> 68579 -> 68597`

and you must return the greatest: `68957`.

Calling this function max_rot (or maxRot or ... depending on the language)

```javascript
maxRot(56789); // should return 68957
maxRot(38336384); // should return 83638433
```

Hint: Try breaking this algorithm into more than one function.

---

### Resources

[Fib num wiki](http://en.wikipedia.org/wiki/Fibonacci_number)

[Visualize Python or JavaScript Execution](http://www.pythontutor.com/visualize.html#mode=edit)
