# Modelo Relacional criado a partir de narrativa
## Esquema conceitual para desafio do Bootcamp da DIO

## Objetivo:
Criar o esquema conceitual para o contexto de oficina com base na narrativa fornecida

## Narrativa:
* Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica
* Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas
* Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
* A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
* O valor de cada peça também irá compor a OS. O cliente autoriza a execução dos serviços
* A mesma equipe avalia e executa os serviços
* Os mecânicos possuem código, nome, endereço e especialidade
* Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

## Estrutura
O projeto conta com as entidades: Cliente, Veiculo, Equipe, Mecanico e Ordem_servico.
Conta também com uma tabela com a relação de peças e serviços oferecidos, que servirá de base para as relações: servicos_prestado e pecas_adquiridas.
Há também a relação de posse entre o veículo e cliente; e por fim a relação de avaliaçã e execução do serviço.


## Cliente
Cliente é identificado com um CPF ou CNPJ, e também conta com campos para nome completo, endereço, email, e telefone.

## Posse (Possui)
Relacionamento que une o cliente e seu respectivo veículo com dados de identificação de ambos.

## Veículo
Entidade com identificação através de licença, e descrição com atributos de modelo, ano, cor, descrição, placa, quantidade de eixos, tipo de veículo.

## Equipe
Entidade que agrupa vários mecânicos para execução de serviços, contando com código próprio e informações de seus respectivos integrantes.

## Mecânico
Entidade que conta com código, nome, especialidade e endereço.

## Avalia e executa
Relacionamento composto por informações da equipe  que avaliará e executará o serviço e do veículo a ser trabalhado.

## Peças e peças adquiridas
A primeira é a entidade que contém uma tabela com o nome e preço de peças disponíveis, já a seguna é referente às adquiridas para a execução dos serviços da Ordem.

## Serviços e serviços prestados
O primeiro é uma entidade que contém uma tabela com a relação da mão de obra e seus preços. Já a segunda se trata dos trabalhos prestados para a execução da Ordem.

## Ordem de serviço
A ordem recebe informações do cliente, veículo, equipe que está trabalhando,  peças adquiridas e serviços prestados. Por sua vez, tem o valor total dos trabalhos realizados, data de emissão e de entrega, status do andamento dos trabalhos e o tipo de atendimento, além de possibilitar uma descrição mais detalhada ou a adição de observações.

