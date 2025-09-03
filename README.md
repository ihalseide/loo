# Loo language

Are you a programmer who likes counting from 0 and likes half-open intervals?
Or are you tired of frequently typing out long words like "do", "end", and "then"?
With this replacement for Lua, your scripts can look like this instead:

```javascript
/*
This is a multi-line
comment
*/
function zero() {
  // Let's try out 0-based indices
  t = {1,2,3}
  print("t[0] = "..t[0])
}

zero() // should print out 1
```

Now you can make Lua follow typical C-like programming language conventions.
Loo is Lua 5.3 but with 0-based indices, C-style syntax for blocks.
(And, soon to be added, a *continue* statement).

## TODO

- add **continue** keyword & statement
