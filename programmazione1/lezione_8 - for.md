
**stabilire se la prima cifra dopo la virgola di un floating point è pari**

```go

```

**stabilire se la somma delle cifre di un numero di tre cifre è > 10 **

```go

```

**stabilire se una data (s,m,a) è corretta**

```go
package main

import "fmt"

func main() {
    var giorno, mese, anno int
    fmt.Scan(&giorno, &mese, &anno)
    if giorno < 0 || giorno > 31 || mese <= 0 || mese > 12 {
	    fmt.Println("Sbagliata")
    } else if mese == 11 ||  mese == 4 || mese == 6 || mese == 9 {
	    if giorno == 31 {
		    fmt.Println("Sbagliata")
	    } else {
		    fmt.Println("giusto")
	    }
    } else if mese == 2 {
	    bisestile := (anno % 100 != 0 && anno % 4 == 0) || anno % 400 == 0
	    var gf int
	    if bisestile {
		    gf = 29
	    } if giorno <= gf {
		    fmt.Println("Giusto")
	    } else {
		    fmt.Println("Sbagliata")
	    }
    } else {
	    fmt.Println("Giusto")
    }
}
```


**RIPETERE I PRINT NON è PRATICO! SAREBBE MEGLIO CREARE UNA FUNZIONE CHE RITORNA TRUE O FALSE A SECONDA DEGLI IF E POI FARE UN UNICO PRINT**


# LE STRUTTURE DI ITERAZIONE

## ciclo for unario

```go
for (condizione) {
	codice
}
```


contatore a decremento
```go
var x int
fmt.Scan(&x)
for x >= 0 {
	fmt.Println(x)
	x--
}
```

**MCD**
metodo non efficiente
```go
var x, y int
fmt.Scan(&x, &y)
var m int // --> minimo (x, y)
if x <= y {
	m = x
} else {
	m = y
}
for x % m != 0 || y % m != 0 {
	m--
}
```

**metodo efficiente con il teorema di Euclide**

```go
var x, y int
fmt.Scan(&x, &y)
var r int

r = x % y

for r != 0 {
	x = y
	y = r
	r = x % y
}
fmt.Println(y)
```

## ciclo for ternario

```go
for a; b; c {
	blocco
}
```

ex.
```go
var x, n int
fmt.Scan(&n)
for x = 3; x < n; x+= 3 {
	fmt.Println(x)
}
```

```go
for i := 1; i <= 10 ; i++ {
	fmt.Print("*")
}
```


```go
for i := 10; i <= 0 ; i-- {
	fmt.Print("*")
}
```




