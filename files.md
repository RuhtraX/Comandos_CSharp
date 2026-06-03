## Arquivos

#### Importar
```
using System;
using System.IO;
```

### Exluir arquivo

```
try
{
  File.Delete(caminho);
}
catch (Exception e)  
{
  Console.WriteLine("Erro ao excluir arquivo: {0}", e.ToString());
}
```

### Capturar arquivos na pasta

```
private static void GetFilesinFolder(String urlPasta, String busca)
{
  try
  {
    string[] dirs = Directory.GetFiles(urlPasta, busca);
    Console.WriteLine("Existem {0} arquivos começando com {1}:", dirs.Length, busca);
    foreach (string dir in dirs)
    {
      Console.WriteLine(dir);
    }
  }
  catch (Exception e)
  {
    Console.WriteLine("Erro: {0}", e.ToString());
  }
}
```

### Renomear pasta ou arquivo

```
private static void MoveFileFolder()
{
  string origem = @"C:\Users\Public\public\test.txt";
  string destino = @"C:\Users\Public\private\test.txt";
  // Para mover o arquivo ao destino:
  System.IO.File.Move(origem, destino);
  // Para mover uma pasta inteira:
  System.IO.Directory.Move(@"C:\Users\Public\public\test\", @"C:\Users\Public\private");
}
```

### Ler conteúdo de um arquivo de texto

#### Importar
```
using System;
using System.IO;
using System.Text;
```

#### Exemplo
```
public static void lerArquivo(String caminho)
{
  string texto = File.ReadAllText(filePath, Encoding.Default);
  Console.WriteLine(texto);
}
```

### Capturar nome do arquivo

```
private static void GetFileName()
{
  String caminhoArquivo = @"C:\arquivo.xlsx";
  FileInfo fileInfo = new FileInfo(caminhoArquivo);
  Console.WriteLine("Nome do arquivo: {0}, fileInfo.Name);
  return fileInfo.Name;
}
```

### Escrever texto em arquivo
```
using (StreamWriter writer = new StreamWriter("C:\\dados\\arquivo.txt", true))
{
  writer.WriteLine("Lorem Ipsum");
}
```

### Extrair conteúdo de arquivo compactado (.zip)

#### Importar
`using System.IO.Compression;`

#### Exemplo
```
string caminhoZip = @".\arquivo.zip";
string destino = @".\extract";
ZipFile.ExtractToDirectory(caminhoZip, destino);
```
