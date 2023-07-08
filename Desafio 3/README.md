## Instruções de Entrega do Desafio

1. Verifique os cabeçalhos e tipos de dados

2. Modifique os valores monetários para o tipo double preciso

3. Verifique a existência dos nulos e analise a remoção

4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente

5. Verifique se há algum departamento sem gerente

6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas

7. Verifique o número de horas dos projetos

8. Separar colunas complexas

9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção

10. Neste processo elimine as colunas desnecessárias.

11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.

12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores

13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.

14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.

15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente

16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela

______________________________________________________________________________________________________________________________________________

## Respondendo a pergunta do item número 14

- **Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.**

No caso supracitado, podemos utilizar apenas a mescla de tabelas ao invés de atribuir porque estamos buscando combinar informações de diferentes tabelas com base em uma relação de chaves. O mesclar irá combinar as linhas com base nas chaves correspondentes, enquanto por outro lado o atribuir é utilizado quando queremos adicionar  única coluna a uma tabela existente com base em um valor correspondente em outra tabela (e não mesclar tudo).

______________________________________________________________________________________________________________________________________________

## Ações Realizadas:

**BD**
- Baixar BD base fornecida pelo desafio
- Corrigir nomes e queries

**Todas as Tabelas**
- Remover colunas desnecessárias.
- Converter a coluna chave de número para texto.
- Alterar nomes para melhor entendimento.
- Substitur os valores da coluna "Sexo" (nas tabelas que a possuem) de M -> "Male" e F -> "Female".

**Tabela "company department"**

- Todos os departamentos possuem um gerente associado, datas de início da gestão e criação do departamento.
- Mezclar tabela com a tabela de localização depois de limpar ela. Selecionar primeiro esta e depois a outra. Usar Outer Left Join usando a chave número do departamento.
- Selecionar as colunas relevantes, expandir, apagar colunas desnecessárias.

**Tabela "company employee"**

- Combinar as colunas de primeiro nome, inicial do nome do meio e sobrenome em uma única coluna "Full_Name".
- Na coluna "Super_ssn" contém um valor nulo, indicando a ausência de um gerente.
- Mezclar tabela com a tabela de departamento depois de limpar ambas. Selecionar primeiro esta e depois a outra. Usar Outer Left Join usando a chave número do departamento.
- Selecionar as colunas relevantes, expandir, apagar colunas desnecessárias.

**Tabela "company works_on"**

- Removi as colunas: "company.employee" e "company.project";
- Converti a coluna "Pno" de número para texto, pois trata-se de uma chave.

- Revisar relações, colunas e dados.

## Relatório

Após o tratamento dos dados no Power Query, criar um relatório simples no Power BI para representar graficamente as informações.
