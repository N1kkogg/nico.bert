```go
package main
import (
	"fmt"
	"bufio
	"os"
	"strconv"
)

bufio := bufio.NewScanner(os.Stdin)
scanner.Split(bufio.ScanWords)

for scanner.Scan(){
	riga := scanner.Text()
	fmt.Println("la stringa è <" + riga + "> e la lunghezza è di " + strconv.Itoa(len(text))) + " bytes")
}
```

`go doc bufio`

`strconv.Itoa` (INTEGER TO STRING)
`strcont.Atoi` (STRING TO INTEGER)