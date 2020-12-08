<!-- .slide: id="lesson22" -->

# Basic Frontend - Fall 2020

Lesson 22, Tuesday, 2020-12-08

---

### Recap Copy-by-value

* What's the value of `b`?

```js
let a = 42;
let b = a;
a = 43;
console.log(b);
```

* b is still 42. Primitive values are copied by value!
<!-- .element: class="fragment" -->

---

### Copy-by-reference

* Complex types (Array, Object, Function, ...) are copied by reference:

```js
let person1 = { name: "John" };
let person2 = person1;
person1.name = "Johnny"
console.log(person2.name) // "Johnny"
```

* Both `person1` and `person2` point to the same object. Objects are not copied, but referenced.

---

### Things we did _not_ teach

We did leave out a couple of statements and keywords that you might see in other JavaScript beginners courses:

1. template strings
1. `break`
1. `continue`
1. `switch` statement
1. various operators

---

### Template strings

Template strings start and end with a backtick and can contain JavaScript expressions in a `${}` block:

```js
let name = "John";
let s1 = "Hi, my name is " + name;
let s2 = `Hi, my name is ${name}`;
```

Both s1 and s2 are identical.

---

### `break`

* `break` instantly exits the closest `for` or `while` loop:

```js
for (let i = 0; i < 10; i++) {
    if (i === 8) {
        break;
    }
    console.log(i);
}
```

* Often considered to be "dirty" as it's confusing to exit a loop at arbitrary places

---

### `continue`

* `continue` instantly continues with the next iteration of the loop:

```js
for (let i = 0; i < 10; i++) {
    if (i === 8) {
        continue;
    }
    console.log(i);
}
```

* Often considered to be "dirty" as breaks the established flow of a loop

---

### `switch`

* Switch is a "glorified" `if` statement:

```js
switch (dayOfWeek) {
    case "Monday":
        console.log("today just sucks");
        break;
    case "Friday":
        console.log("almost there!!");
        break;
    case "Saturday":
    case "Sunday":
        console.log("party!!!");
        break;
    default:
        console.log("go to work");
        break;
}
```

---

### Advanced operators

We did learn the following:

* Arithmetic ( `+ - * / % ++ --` )
* Combined (`+=`, `-=`, etc.)
* Logical (`&& || !`)
* Comparison (`=== !== > < <= >=`)

We did _not_ learn the following:

* Ternary (`?`)
* Bitwise (`& | ~ ^ << >> >>>`)

---

# That's it :)

Hope to see some of you as teachers/tutors next year :)