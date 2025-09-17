# Loo language

Loo is Lua 5.3 but with:
- 0-based indices for tables
- A *continue* statement (which works for while loops, repeat loops, and both types of for loops)
- Inequality operator is `!=` instead of `~=`
- C-style syntax for blocks (curly brackets)

Now you can use Lua but with typical C-like programming language conventions.

## Example

Are you a programmer who likes counting from 0 and likes half-open intervals?
Or are you tired of frequently typing out long words like "do", "end", and
"then" instead of curly brackets?
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

// Let's try out CONTINUE and inequality (!=)
for (i = 0, 8) {
  if (i % 2 != 1) {
    print("even")
    continue
  }
  print(i)
}
```

## Motivation

For programmers used to other languages, this makes it so you don't have to
think about the different ways Lua approaches things and potentially make more
mistakes.

## Notes

The syntax of the `continue` statement mirrors the `break` statement in Lua: it
is not required to be the last statement in a block (unlike the `return`
statement).
