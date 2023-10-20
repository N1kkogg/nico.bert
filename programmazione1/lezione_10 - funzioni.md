come si definisce una funzione:
```go
func test(argomento tipo, arg tipo) tipo_return
```

**descrivere sempre la funzione con dei commenti**

```go
/*
dato un intero x la funzione ritorna boolean,
se il numero è primo
*/
func isPrime(x int) bool {
	var d int
	for d=2;d<x;d++ {
		if x%d == 0 {
			break
		}
	}
	if d < x {
		return false
	} else {
		return true
	}
}
```

```go
func isPrime(x int) bool {
	var d int
	for d=2;d<x;d++ {
		if x%d == 0 {
			break
		}
	}
	return d == x
}
```

```go
func isPrime(x int) bool {
	var d int
	for d=2;d<x;d++ {
		if x%d == 0 {
			return false
		}
	}
	return true
}
```

```go
/* dato n ritorna tutti quanti numeri primi ci sono 
fino ad esso */
func countPrime(n int) int {
	var d,c int
	for d = 2; d <= n; d++ {
		if isPrime(d){
			c++
		}
	}
	return c
}
```

```go
func asintotico(n int) float64 {
	return float64(n) / math.Log(float64(n))
}
```

**esempio di main su queste funzioni**
```go
func main() {
	var n int 
	n = 2
	for {
		x1 := float64(countPrime(n))
		x2 := asintotico(n)
		fmt.Println(n, x1/x2)
		n++
	}
}
```


# rappresentazione dell'informazione



### tipi di base:
- interi
- floating point 
- altri

#### interi
- senza segno --> `uint, uint8, uint16, uint32, uint64`
- con segno --> `int, int8, int16, int32, int64`
#### floating point
- reali --> `float32, float64` 
- complessi --> `complex64, complex128`

#### altri
- bool 
- byte
- rune
- string
- error
- uintptr