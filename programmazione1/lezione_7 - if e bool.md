

```go

```

## condizione = espressione bool

espr. numeriche (`>, <, <=,==,!=`) espr. numeriche

operazioni relazionali 

```go
var x,y int
var b1,b2 bool
x = 13
y = 47
b1 = x > y
b2 = true
b3 = 4 * x  >= y
b4 = b3
```

the default value of a new bool variable is False

operatori bool
-  logici `&&` and `||`or  --> (binari perché si applicano a 2 valori)
- `!` not --> unario

AND = `&&` --> congiunzione logica

| AND | false | true |  
| -------- | -------- | -------- |  
| false | false | false |  
| true | false | true |

OR = `||` --> disgiunzione logica

| OR | false | true |  
| -------- | -------- | -------- |  
| false | false | true |  
| true | true | true |

NOT = `!`

| NOT |  |  |  
| -------- | -------- | 
| false | true
| true | false


```go
x := 15
y := 20
z := 5

b1 := (x > y) && (z == 5)
b2 := (x <= y) && (z == 5)
b3 := !b1
b4 := !!b3
b5 := b1 && b1
b6 := (b1 && b2) == (b2 && b1)
b7 := ((b1 && b2) && b3) == (b1 && (b2 && b3))

// leggi di assorbimento
b8 := a && (a || b) == a
b9 := a || (a && b) == a
```

## leggi di De Morgan

- 1
```go
!(a && b) == (!a) || (!b)
```

- 2
```go
!(a || b) == (!a) && (!b)
```

```go
if !(x > 5 || y <= x){
}
```

equivale a

```go
if x <= 5 && y > x {
}
```

- Applicare la legge di De Morgan a 

```go
!(x * x > z && (x > 0 || y < 0))
```

equivale a

```go
!(x * x > 2) || !(x > 0 || y < 0 )
x * x <= 2 || ( !( x > 0) && !(y < 0))
x * x <= 2 || (x <= 0 && y >= 0)
```