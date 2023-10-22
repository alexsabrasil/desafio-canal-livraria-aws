# Desafio AWS - Mentoria de Carreira 3.0 do Canal da Cloud | 2023.2

## SITUAÇÃO PROBLEMA

O cliente Livraria Cloud Books deseja expandir seu catálogo de livros e
audiobooks na web e deseja utilizar os serviços de nuvem da AWS.
Segundo o diretor da empresa, o João das Neves, hoje estão hospedando a
aplicação (WordPress) e o banco de dados (MySQL) em um servidor OnPremise
com 8 CPU e 16 GB de RAM, mas normalmente utiliza na faixa de 30% dos
recursos, tendo picos imprevisíveis que chegam a 100%, às vezes até ficando fora
do ar, o que fez a empresa perder cerca de 20% de clientes neste último ano. A
aplicação possui 100 GB de disco, sendo que 85 GB são de PDFs, imagens e
áudios.
A empresa estruturou muitos novos livros e audiobooks, que serão
anunciados ao longo do primeiro semestre de 2024, tendo uma previsão de
aumento de acessos da ordem de 50% no final do ano, em relação ao início do
semestre.
O diretor está preocupado com esse crescimento frente aos desafios que
tiveram com seu servidor OnPremise esse ano. Portanto, ele entrou em contato com
a Amazon Web Services, o maior provedor de computação em nuvem do mundo,
para entender como a Livraria Cloud Books pode se beneficiar da nuvem.
A AWS nos encaminhou o cliente para que possamos projetar a jornada de
adoção para a nuvem da empresa e oferecermos uma solução para o João das
Neves.
Espaço para criação das estruturas e construção dos serviços da aws.

## Time 5:

- Mentor: Diogo
- Apoiadora: Paula
  
Time five: 

- Alexsandra
- Jonatas
- Marcos
- Wayne

## Programação Canal da Cloud 3.0 

- Aulas ao vivo - online (uma ou duas aulas na semana)
- Reuniões (Time Five): Aos sábados ou Segunda-feira, podendo ser alterado conforme a necessidade do time.
  
## Tarefas atribuídas

- Definição de itens de Arquitetura na AWS - Responsável: <nome>
- Redes (VPC, Subnets pública/privada, AZs, Regiões) - Responsável: <nome>
- Recursos (EC2, S3, etc) - Responsável: (Alexsandra)
- Plano de Migração: Responsável: (Jonatas)
- Diagrama da arquitetura - Responsável: <nome>
- Solução de monitoria - Responsável: <nome>
- Estimativa de custos - Responsável: <nome>
- Definição de planos - Responsável: <nome>
- Calculadora de custos - Responsável: <nome>
- Backups - Responsável: <nome>
- Planos de backup (rotina, recursos, etc) - Responsável: <nome>
- Apresentação - Responsável: <nome>
- Cronograma - Responsável: <nome> 

## Minha Tarefa: Recursos

- EC2: Utilizar instâncias EC2 para hospedar o WordPress e aplicar Auto Scaling para lidar com picos de tráfego.
- S3: Migrar os dados de PDFs, imagens e áudios para o Amazon S3 para armazenamento escalável e durável.

#### Serviços Complementares:

- Para análise de custo, conforme a necessidade do cliente.

## Representação textual simplificada da arquitetura e do cronograma

- Arquitetura na AWS:

+------------------+          +-------------------+           +---------------------+
|     VPC          |         |    Instâncias EC2     |         |     Banco de Dados     |
|                        |         |     +----------------+          |     +------------------+        |
|  +------+       |          |     |      +----------------+      |      +-------+     |
|  | Subnet |     |         |    |      |     S3 (Armazenamento)    |     |     Balanceadores de carga      |
|  |  Pública  |      |        |     |    |              |            |     |              |     |
|  |  Subnet |     |        |    |      |              |           |     |              |     |
|  +------+      |         |    +-------------------+         |     +--------------+     |
|                        |         |                    |          |     |  Auto Scaling      |
+------------------+         +-------------------+          +---------------------+

