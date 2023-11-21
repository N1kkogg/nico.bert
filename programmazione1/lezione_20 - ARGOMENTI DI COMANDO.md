dichiarazione
```go
var x,y []int
```

#### popolazione slice
1 - se si sa la lunghezza
2 - se non si sa la lunghezza
1) `x = make([]int, n)`
2) `x = append(x, 7) x = append(x,2,3,4)`

#### accesso alla slice
`len(x)`
`x[0],... x[n-1]

```go
for i := 0; i<len(x);i++{
	x[i]
}
```

```go
for i, t := range x {
	x[i] lettura/scrittura
	t lettura
}
```

alias due slice che condividono due in tutto o in parte l'array soggiacente

```go
var x, y []int
x = make([]int, 10)
y = x --> alias
```
evitare di avere in giro alias se la slice deve ancora essere modificata (append!!!)


### argomenti da riga di comando

```bash
go build pippo.go
./pippo
./pippo uno due tre
```

# argomenti sono in

```
os.Args []string
```

vediamo un main

os.Args contiene anche il nome del programma

```go
func main() {
	t := some_func(os.Args[1.]) // --> subslicing cosi ignoriamo il primo string
	fmt.Println(t) 
}
```