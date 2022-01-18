# fn

```
fn.print_add (i64.a i64.b) -> i64
    fmt.println (a b)
    c = math.add (a b)
    return c
#

fn.i64_add (i64.a i64.b) => math.add (a b) #
```
函数以 `fn.` 开始为声明，接收一个参数（组） 
-> 后两个参数 
=> 后一个参数
考虑到左大括号的位置问题，使用 # 来表示结束
`#` == `()`

# var

```
(any.d fix.bool.e) = (1024 false)

-- wrong: any.k
```
变量声明以【类型 dot 名字】进行 
`any` 代表类型自动推导，所以不能单独使用
`fix` 相当于 immutable

# string

```

-- short
str.f = "hello"

-- long
str.g = [[
{{ f -}}
world]]

str.j = string.add (f g)
```

# comment

```
-- short comment single line

-- [[
    long comment
]]

-- [===[
    another long comment
]===]
```

# map & array

```
map.h = {
    "其" = 1
    "shi" = 250
}

fmt.println (h["shi"] h[[其]])

h.append ("哼啊～" 114514)

i64.length = h.len      -- x.len() x.len len(x) 理论效果相同

array.i64.i = {1 2 3 4 5 6}

fmt.println i[-1]
```

# control

```
for (any.k any.v) = h.each
    fmt.println (k v)
#

if 5 > 4 > 3
    fmt.println true
#

i64.foo_max = (a > b)?(a):(b)

when (a b)
    (1 2) => fmt.println (1 2) 
             continue    
        #
    (2 2) => fmt.println (2 2) #
    ($ $) => fmt.println "other" #
#

```
`for` == `index` + `when` 
`when` == `fn` + `if` + `goto` 
没有 `else` 

# struct
```
type.sell
    str.name
    i64.money
#
--[[
    above equal below
    type.sell (str.name i64.money)
]]

sell.cat = {"😺" 100}

impl.sell.print => fmt.println (this.name this.money) #

```

---

lisp 的语法让人非常年难受，比 markdown 还难受