# azure_company
Repositorio para armazenar do projeto AzureSQL
Criando o banco de dados

Estou utilizando MySQL Workbench
Essa consulta faz uma junção da tabela employee (e1) com ela mesma (e2) usando a coluna Super_ssn de e1 e a coluna Ssn de e2. Isso retorna os nomes dos funcionários junto com os nomes de seus supervisores.

SELECT e1.Fname AS Employee_First_Name, e1.Lname AS Employee_Last_Name, 
       e2.Fname AS Supervisor_First_Name, e2.Lname AS Supervisor_Last_Name
FROM employee e1
LEFT JOIN employee e2 ON e1.Super_ssn = e2.Ssn
WHERE e1.Super_ssn IS NOT NULL;

Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente.
O colaborador sem gerente é o James da Sede/Matriz, não tem superior o restante são os próprios gerentes.


Mesclar Consultas
Mesclar consultas permite unir duas tabelas com base em colunas correspondentes, semelhante a um JOIN em SQL. Isso é útil quando você deseja adicionar colunas de uma tabela a outra, criando uma tabela mais completa. Por exemplo, se você tem uma tabela de vendas e outra de produtos, pode mesclar as duas usando a coluna de ID do produto.

Combinar Consultas
Combinar consultas, por outro lado, pode se referir a duas operações principais:

Mesclar Consultas: Como descrito acima, une tabelas horizontalmente.
Acrescentar Consultas: Adiciona linhas de uma tabela a outra, semelhante a um UNION em SQL. Isso é útil quando você tem dados semelhantes em várias tabelas e deseja consolidá-los em uma única tabela


