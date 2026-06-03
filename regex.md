## REGEX

### REPLACE

#### Importar
```
using System;
```

#### Exemplo
```
String s = "aaa";
Console.WriteLine("The initial string: '{0}'", s);
s = s.Replace("a", "b").Replace("b", "c").Replace("c", "d");
Console.WriteLine("The final string: '{0}'", s);
```

### MATCH

#### Importar
```
using System;
using System.Text.RegularExpressions;
```

#### Exemplo
```
string pattern = @"\ba\w*\b";  
string input = "An extraordinary day dawns with each new day.";  
Match m = Regex.Match(input, pattern, RegexOptions.IgnoreCase);  
if (m.Success) Console.WriteLine("Encontrado '{0}' na posição {1}.", m.Value, m.Index);
```
