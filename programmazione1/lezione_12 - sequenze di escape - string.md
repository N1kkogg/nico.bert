
**Sequenze di escape**

`\`
backslash

`\t` --> tab
`\n` --> newline
`\'` --> mettere in una stringa una '
`\\` --> escaped backslash

**UNICODE**
`\uXXXX`
`\UXXXXXXXX`

## UTF-8

- rappresentazione a lunghezza variabile

string --> utf-8

1) ogni caratter occupa da 1 a 4 byte
2) il primo byte --> 0|..... per i caratteri ascii (monobyte) oppure 1110|.... per i caratteri di k>1 byte
3) i byte successivi al pimo iniziano con 10|.... ù


# string

`var s string`

`len(s)` --> lunghezza in byte s

`s[i]` 

variabile tipo `rune` --> int32 per rappresentare i caratteri