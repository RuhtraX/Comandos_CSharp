## Banco de Dados

### SQL SERVER

#### Importar
`using System.Data.SqlClient; // Instalar via NuGet System.Data.SqlClient`

#### Exemplo conexão e consulta

```
SqlConnection conexao = new SqlConnection(connString);
conexao.Open();
SqlCommand cmd = new SqlCommand(query, conexao);
SqlDataReader reader = cmd.ExecuteReader();
while (reader.Read())
{
	MessageBox.Show(String.Format("{0};{1};{2};{3}", reader[0], reader[1], reader[2], reader[3]));  
}
conexao.Close();
```

### MYSQL

#### Importar
`using MySql.Data.MySqlClient; // Instalar via NuGet MySQL.Data`

#### Exemplo conexão e consulta
```
MySqlConnection conexao = new MySqlConnection(connString); // Cria conexão com o BD na variável conexao  
conexao.Open(); // Libera a conexão
MySqlCommand cmd = new MySqlCommand(query, conexao); // Executa a query na conexão
MySqlDataReader reader = cmd.ExecuteReader(); // Salva os dados em uma variável
while (reader.Read()) // Cria uma recorrencia para os dados encontrados(Semelhante ao "FOR EACH")
{
	MessageBox.Show(String.Format("{0};{1};{2};{3}", reader[0], reader[1], reader[2], reader[3])); // Mostra o resultado
}
conexao.Close(); // Fecha conexão
```

### ORACLE

#### Importar
`using Oracle.ManagedDataAccess.Client; //Instalar via NuGet Oracle.ManagedDataAccess`

#### Exemplo conexão e consulta
```
OracleConnection conexao = new OracleConnection(connString);
conexao.Open();
OracleCommand cmd = new OracleCommand(query, conexao);
OracleDataReader reader = cmd.ExecuteReader();
while (reader.Read())
{
	MessageBox.Show(String.Format("{0};{1};{2};{3}", reader[0], reader[1], reader[2], reader[3]));
}
conexao.Close();
```
