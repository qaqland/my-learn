# fn

```
(fn.print_add (i64.a i64.b) i64
    c = (.math.add a b)
    .fmt.print c
    .return c
)
```

# var

```
(any.d fix.bool.e) = (1024 false)
```

# strings

```

-- short
str.f = "hello"

-- long
str.g = [[
{{ f -}}
world]]

```

# tables

```
map.(str i64).h = {
    "其" = 1
    "shi" = 250
}

.h.append ("哼啊～" 114514)
i64.length = h.len
```

# arrays

```
array.i64.i = (1 2 3 4 5 6)
```

