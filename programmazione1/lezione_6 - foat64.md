##### ES. PER CASA
data una data (giorno,
mese) calcolare quanti giorni mancano a Natale (assumendo che i mesi siano tutti di 30 giorni)
```go
package main

import "fmt"

const GIORNI_ANNO = 360
const NATALE = GIORNI_ANNO - 5

func main() {
	var giorno, mese, giorni_totale int
	
    fmt.Print("Dammi una data (mese, giorno): ")
    fmt.Scan(&mese, &giorno)
    giorni_totale = (mese*30 + giorno) % GIORNI_ANNO
    fmt.Println(NATALE - giorni_totale%NATALE)
}
```


*fmt.Scan consuma un carattere per indicare la fine dell'input (per esempio quando si fa `\n`) quel carattere può essere qualsiasi*


## float64

- dato un imponibile e un aliquota percentuale, calcola l'IVA 

```go
package main
import "fmt"

func main(){
	var imponibile, aliquota, iva, totale float64
	fmt.Scan(&imponibile, &iva)
	iva = imponibile * aliquota / 100.0
	totale = imponibile + iva
	fmt.Println(totale)
}
```

**PER INDICARE CHE UN NUMERO è FLOATING POINT USARE IL PUNTO DOPO IL NUMERO (esempio: `100.0`)**

- date le altezze in centimetri (numeri interi) di due persone, calcolare la media (decimale)

### convertire i numeri interi in float64
```go
package main
import "fmt"

func main(){
	var h1,h2 int
	fmt.Scan(&h1,&h2)
	var media float64
	// media = (h1+h2)/2 NON SI PUò FARE BISOGNA CONVERTIRE I NUMERI
	media = float64((h1+h2)/2)
	// OPPURE
	media = float64(h1+h2)/2.0
}
```



# COME FARE LA RADICE QUADRATA

```go
package main

import (
	"math"
	"fmt"
)

func main(){
	var f,a float64
	fmt.Scan(&f)
	s = math.Sqrt(f)
	fmt.Println(s)
	x = int(s)
	fmt.Println(x)
	y = int(5 + 0.5)
	fmt.Println(y)
}
```

**int(s)** cambia in numero intero una variabile


## ESERCIZIO A CASA:

convertire la media da 30esimi in 110mi

```go
package main

import "fmt"

const COSTANTE_110esimi = 110
const COSTANTE_30esimi = 30

func main() {
    var media, media_calcolata float64
    fmt.Print("inserisci qui la media da trasformare: ")
    fmt.Scan(&media)
    
    media_calcolata = media * COSTANTE_110esimi / COSTANTE_30esimi
    //29:30=x:110
    fmt.Println("la media calcolata su", media, "/ 30 è", media_calcolata, "/ 110")
}
```

## ALTRI OPERATORI:

esistono altri operatori oltre ai comuni (`+ - * / %*`)

- variabile ++ (incrementa di uno una variabile)
- variabile --  (decrementa di uno una variabile)
- variabile += -= *= /=


## blank identifier

```go
package main
import "fmt"

func main(){
	var x,y float64
	x = 3.5 *4
	y = 3.6 * 5
	_ = x

	fmt.Println(y)
}
```

`_` è un blank identifier serve per usare la variabile, (è come un cestino elimina il contenuto della var)

