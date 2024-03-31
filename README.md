# dio_data_analytics_desafio2
Desafio de projeto Dio Data Analytics conectar Azure MySQL flexible server com o Power Bi Desktop


##Query levantar gerentes:

select Fname , 'Franklin' as gerente from employee e where Super_ssn = 333445555
union
select Fname , 'Jennifer' as gerente from employee e where Super_ssn = 987654321
union
select Fname , 'James' as gerente from employee e where Super_ssn = 888665555;

##Resultado

John	Franklin
Joyce	Franklin
Ramesh	Franklin
Ahmad	Jennifer
Alicia	Jennifer
Franklin	James
Jennifer	James
