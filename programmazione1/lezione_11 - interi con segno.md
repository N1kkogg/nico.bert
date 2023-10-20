
`int8 int16 int32 int64 `

#### rappresentazione in complemento a 2

01111111 --> 127
01111110 --> 126
00000000 --> 0

11111111 --> -1
10000000 --> -128

```go
var x, y int8
x = 100
y = 100
fmt.Println(x+y+120)

//overflow
// ret 64
```


### floating point

numeri reali --> `float32, float64`
numeri complessi --> `complex64, complex128`

1.35e-7 -->1.35 * 10^-7l

**MAI USARE == CON FLOATING POINT**

`x==y` NO

| x-y | 

`math.Abs(x - y) < 1e-7 `

### tipo rune

- standard US-ASCII
no lettere accentate, non tutte le lettere. fino a 127 caratter

- ISO-88591 - Latin1
120 --> US-ASCII
128 --> tutte le lettere accentate ecc

- unicode
milioni di caratteri