```go
var s *string

s = "pippo"
p = &s

fmt.Println(s)
fmt.Println(p)
fmt.Println(*p)
fmt.Println(len(*p))
fmt.Println(s)
```

```go
var x int
var p *int
var q **int
x = 15
p = &x
q = &p
(**q)++
fmt.Println(x)
```

```go
var x int
var p *int
var q **int

x = 7
p = &x
q = &p
*p = 50
**q = *p - (x+1)
(*p)++
(**q)++
fmt.Println(x)
```

# new
```go
new (T)
```

alloca uno spazio di memoria per il tipo T

```go
var p *int
p = new (int)
*p = 7
fmt.Println(*p)
```


```go
var x int
var p *int
var q **int
x = 7
p = &x
q = &p
p = new (int)
*p = 50
q = new (*int)
*q = &x
**q = 5
*q = new (int)
**q = 12
fmt.Println(x, *p, **q)
```

```go


```