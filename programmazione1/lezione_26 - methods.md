dato p1 point quanto è distante da p2? p1.DIst()
```go
package pointlol
import (
"math"
)

func (p1 Point) Dist(p2 Point) float64 {
	dx := p1.x - p2.x
	dy := p1.y - p2.y
	return math.Sqrt(dx * dx + dy *dy)
}

```

uso pacchetto esterno --> go init main 
go mod tidy
```go
package main

import(
	"github.com/test/pointlol"
)

func main() {
	 var p1, p2 mpoint.Point
	 p1 = mpoint.NewPoint(3,2)
	 p2 = mpoint.NewPoint(5,5)
	 dist := p1.Dist(p2)
	 fmt.Println(" la distanza fra ", p1, "e", p2, "e", dist)
	 pm := p1.Median(p2)
	 fmt.Println("il loro punto medio è, pm")
}



```