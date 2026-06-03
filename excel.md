## Excel

### Ler Excel

#### Importar
`using Excel = Microsoft.Office.Interop.Excel; // Instalar via NuGet Microsoft.Office.Interop.Excel`

#### Exemplo leitura Excel
```
public static void LerExcel(string caminho)
{
  try
  {
    Excel.Application oExcel = new Excel.Application();
    Excel.Workbook WB = oExcel.Workbooks.Open(caminho);
    string tituloExcel = WB.Name;
    int qtdPlanilhas = WB.Worksheets.Count;
    // Utilizar a 5ª planilha
    Excel.Worksheet wks = (Excel.Worksheet)WB.Worksheets[4];
    string nomePlanilha = wks.Name;
    var valorCelula = ((Excel.Range)wks.Cells[rCount, 1]).Value;
    Console.WriteLine("Valor da célula: {0}", valorCelula);
    WB.Close();
  }
  catch (Exception ex)
  {
  Console.WriteLine("Erro: {0}", ex);
  }
}
```
