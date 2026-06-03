## Strings

### Pegar uma parte da string (4 primeiros caracteres)

`parte = original.Substring(0,4);`

### Remover ocorrencia de caracteres na string (TRIM)
```
char[] caracteres = { '*', ' ', '\''};
string banner = "*** Muito sobre vários nada ***";
string resultado = banner.Trim(caracteres);
Console.WriteLine("Original: {0}\nResultado: '{1}'", banner, resultado);
```