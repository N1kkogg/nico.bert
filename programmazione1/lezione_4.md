
```go
package main
import "fmt"
func main(){
	var n, i int
	fmt.Print("Quante volte, padre?")
	fmt.Scan(&n)
	for i=0;i<n+;i++ {
		fmt.Println("ciao")
	}
}
```

```bash
$ go build hello.go
```

```bash
$ ./hello
```

```
$ go build hello.go

$ ./hello

$ go help

$ go Doc fmt.Println

$ go fmt hello.go

```


esempi di token:

`package` 
`main`
`func`
`"fmt"`
`(`
`)`
`{`

i token sono separati da whitespace

---
#### Aspetti sintattici:

**Livello:**
- lessicale
- sintattico
- semantico
- pragmatico

--- 
**Token:**

whitespace = ` ` e `\t` e `\n`

**Normalmente i token sono separati da whitespace TRANNE se uno dei due token non è alfanumerico (in questo caso whitespace si può omettere)**


**tipi di token**

- keyword --> `package`, `import`, `func`, `var`, `for`...
- identificatori --> caratteri alfanumerici (*case sensitive*) `main`, `piPpo`, `p3` `p_l` `int`
- separatori --> `,` `.` `;` `:` `(` `)` `[` `]` `{` `}`...
- operatori --> `+` `++` `-` `--` `=` `>` `<`...
- letterali --> costanti stringa 

quando voglio indicare che sono dentro ad un blocco più piccolo indento di più

aggiungere sempre commenti 


```go
package main
import "fmt"
func main(){
	var n, i int // variabili
	fmt.Print("Quante volte, padre?")
	fmt.Scan(&n)
	for i=0;i<n+;i++ {
		fmt.Println("ciao")
	}
}
/*
programma per dire ciao tot volte come definito 
dall'utente
*/
```


## PROGRAMMA GO MINIMALE

program.go

*il boilerplate sono tutte quelle cose che sono obbligatorie per far funzionare un programma*

```go
package main
import "fmt"
func main(){
	
}
```

#### direttiva di importazione:

```go
import "fmt"
```


sintassi fattorizzata
```go
import (
"fmt"
"pippo"
)
```



---

#### altri appunti

 > fmt appartiene alla libreria standard di go

> guardare la package https://pkg.go.dev/

> not invented here syndrome 

> check online for libraries
