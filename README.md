# Loo language

Loo is Lua 5.3 but with:
- 0-based indices for tables
- A *continue* statement
- Inequality operator is `!=` instead of `~=`
- WIP: Increment and decrement statements (var++ and var--)
- C-style syntax for blocks (curly brackets)

Now you can use Lua but with typical C-like programming language conventions.

## Example

Are you a programmer who likes counting from 0 and likes half-open intervals? Or
are you tired of frequently typing out long words like "do", "end", and "then"?
With this replacement for Lua, your scripts can look like this instead:

```javascript
/*
This is a multi-line
comment
*/
function first(t) {
  print("t[0] = " .. t[0])
}

// Let's try out 0-based indices
t = { 1, 2, 3}
first(t) // prints out 1
```

## Motivation

For programmers used to other languages, this makes it so you don't have to
think about the different ways Lua approaches things and potentially make more
mistakes.

Also, shouldn't adding 1 or subtracting 1 from a variable be easy for a
*scripting* language? This is why increment and decrement statements have been
added. Note that these operations are statements and not expressions (which is a
break with how C does it).
