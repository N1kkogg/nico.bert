
# string

- sequenze di caratteri
- ""

se la stringa è ASCII
```go
var s string
s = "pippò"
len(s)
s[i]
```

le stringhe sono IMMUTABILI

```go
for i,e := range s{

}
```

concatenazione

2 string

```go
var x,y string
x = "pippo"
y = x + " è formato"
x = "Garibaldi"
y = x + " è tornato"
```

### SUBSTRING

```go
var x,y string
x = "Garibaldi"
y = x[3:6]
```

`y = "iba"`

perchè è dall'index 3 all'index 6


### strings library useful

strins.Index