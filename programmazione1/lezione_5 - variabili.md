
le variabili sono l'astrazione che rappresenta la memoria

**variabili**:
(proprietà statiche)
- nome
- tipo
- scopo
- valore --> proprietà dinamica

proprietà statica dipendente dalla sintassi e comprese dal compilatore
proprietà dinamica cambia durante l'esecuzione

### DICHIARAZIONE DI VARIABILE
`var id,id,id tipo`

`var x,y int`
`var f float64`


```go
package main

import "fmt"

func main(){
	var x,y int

	
}
```


`fmt.Scan(&x)`


`fmt.Print()`

`fmt.Println()`

---

### assegnamento

variabile = espressione


`var x,y int`
`x = 3`
`y = x`
`y = (x+1)*4`
`x = (x+1)*(x+1)`

```go
package main

import "fmt"

func main() {
	var x,y,z int
	x=5
	y=(x+1)+z*3
	x = y*x
	z = x+y
	fmt.Println(x,z)
}
```


espressioni int

-- costanti int
37, -2, -15, 1257
-- variabili int
-- operatori
- +
- -
- *
- / --> divisione intera
- % ---> modulo

`(4+3)*3`

`((4+3)*7)/3`
`((4+3)*7)%3`

```go
var x,y
fmt.Scan(&x)
y = x%10
fmt.Println(y)
```


```go
package main

import "fmt"

func main() {
    var x, y int
    fmt.Scan(&x)
    y = ((x / 10) % 10)
    fmt.Println(y)
}
```

### assegnamenti multipli

`x,y = y,x`

scambia contenuto di due variabili

### short assignment

`nome := espressione`

dichiarare + assegnare una varibile

