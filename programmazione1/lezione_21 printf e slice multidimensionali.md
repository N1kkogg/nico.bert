`fmt.Printf(stringa di fromato, args,...)`

#### verbi 
preceduti da %

il  numero di verbi ugale al numero di argomenti
```go
fmt.Printf("lol %s", )
```

- %d --> intero
- %f --> float
- %s --> string

avverbi

%4d --> 4 è un ampiezza (padding a sinistra con spazi)
%7.2f --> ampiezza 7 caratteri e esattamente 2 dopo la virgola
%02d --> padding con "0"

sprintf ritorna una stringa formattata
```go
func data2string(d Data) string {
	 return fmt.Sprintf("%02d/%02d/%04d", d.g, d.m, d.a)
}
```

esercizio semplice

scrivete una funzione che data una slice di persone e un cognome, restituisce quante persone hanno quel cognome 

## slice multidimensionali

funzione che data una slice quadrata di interi stabilisce se è un quadrato magico

