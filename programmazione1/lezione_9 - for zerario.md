Lezione 9

Ciclo zerario
```go
    for {
        <blocco>
    }
```
è un ciclo infinito

lettura sequenza di input

1) lunghezza nota a priori
```go
    var n,h,s int
    fmt.Scan(&n)
    
    for i:=0; i<n;i++ {
        fmt.Scan(&h)
        s+=h
    }
    media := float64(s)/float64(n)
    fmt.Println(media)
```
2) lettura con tappo (cit. Boldi)
```go
    var n,s,h int
    fmt.Scan(&h)
    for h > 0 {
        n++
        s+=h
        fmt.Scan(&h)
    }
    media := float64(s)/float64(n)
    fmt.Println(media)
```

`Break:
istruzione per il controllo del flusso che serve per interrompere un ciclo (in caso di cicli innestati, interrompe quello più interno)

Es.
```go
    for … {
        <blocco if>
        break
    }
```
Continue:
fa ripartire un ciclo da capo


Identificare se un numero è primo
```go
package main
import "fmt"

func main() {
        var n int
        var trovDiv bool
        fmt.Scan(&n)
        for d:= 2; d<n; d++ {
                if n%d == 0 {
                        trovDiv= true
                        break
                }
        }
        if trovDiv {
                fmt.Println("Non è primo")
        } else  {
                fmt.Println("è primo")
        }
}
```
oppure più efficiente e giusto:

```go
package main
import "fmt"

func main() {
        var n, d int
        fmt.Scan(&n)
        for d = 2; d<n; d++ {
                if n%d == 0 {
                        break
                }
        }
        if d < n {
                fmt.Println("Non è primo")
        } else  {
                fmt.Println("è primo")
        }
}
```


```go
var n, stampati int
fmt.Scan(&n)
for d:=2; stampati < n; d++{
	for c = 2; c < d; c++{
		if d % c == 0{
			break
		}
	}
	if c == d {
		fmt.Println(d)
		stampati++
	}
}
```

