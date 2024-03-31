# dio_data_analytics_desafio2
Desafio de projeto Dio Data Analytics conectar Azure MySQL flexible server com o Power Bi Desktop


##Query levantar gerentes:




----------



1. Criação de uma instância na Azure para MySQL - OK

2. Criar o Banco de dados com base disponível no github  - OK

3. Integração do Power BI com MySQL no Azure - OK

4. Verificar problemas na base a fim de realizar a transformação dos dados - OK

Diretrizes para transformação dos dados

1. Verifique os cabeçalhos e tipos de dados - OK

2. Modifique os valores monetários para o tipo double preciso - OK

3. Verifique a existência dos nulos e analise a remoção - OK 

4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente - James é o gerente geral

5. Verifique se há algum departamento sem gerente - OK, todos tem gerente

6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas - ok

7. Verifique o número de horas dos projetos  - OK

8. Separar colunas complexas - OK

9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção

10. Neste processo elimine as colunas desnecessárias. - ok

11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo. - ok -----------------------------------------------------[select Fname , 'Franklin' as gerente from employee e where Super_ssn = 333445555
union
select Fname , 'Jennifer' as gerente from employee e where Super_ssn = 987654321
union
select Fname , 'James' as gerente from employee e where Super_ssn = 888665555;


-------------------------------------------------------------------
12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores - OK

13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro. - OK

14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir. R: mesclar é preferido devido à sua flexibilidade, capacidade de atualização automática e capacidade de lidar com dados complexos.

15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente - OK  ##Resultado

Franklin = 3 (John; Joyce; Ramesh);;
Jennifer = 2 (Ahmad; Alicia);;
James = 2 (Franklin; Jennifer)]

16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cad - OK
