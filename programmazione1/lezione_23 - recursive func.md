```go
func isPalin(s string) bool {
	if len(s) <=1{
		return true
	} else {
		return s[0] == s[len(s)-1] && isPalin(s[1:len(s)-1])
	}
}
```
è come fare
```go
func isPalin(s string) bool {
	if len(s) <=1{
		return true
	} else {
		if s[0]!=s[len(s)-1]{
			return true
		}
		return isPalin(s[1:len(s)-1])
	}
}
```

esercizio

```go
type Esame struct {
	name string
	propedeuticita []string
}
```

### http server golang


```go
package main

import (
	"fmt"
	"net/http"
)

func pippoPage(w http.ResponseWriter, r *http.Request) {
	w.Write([]byte("<title>Pippo</title>\n<h1>ciao sono pippo!</h1>"))
}

func main() {
	http.HandleFunc("/pippo", pippoPage)
	fmt.Println("Listening on http://localhost:3000/")
	http.ListenAndServe(":3000", nil)
}
```