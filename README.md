DESAFIO SERA IMPLEMENTAR UM SERVIÇO QUE DETERMINE QUAIS MODALIDADES DE EMPRESTIMO UMA PESSOA TEM ACESSO.

AS MODALIDADES SERAO ANALISADAS SAO:

- EMPRESTIMO PESSOAL: TAXA DE JUROS DE 4%
- EMPRESTIMO CONSIGNADO TAXA DE 2%
- EMPRESTIMO COM GARANTIA DE 3%

AS MODALIDADES DE EMPRESTIMO DISPONIVEIS PARA UMA PESSOA SAO BASEADAS EM ALGUMAS VARIAVEIS ESPECÍFICAS SÃO ELAS:

-IDADE
- SALÁRIO
- LOCALIZAÇÃO

  SEU SERVIÇO RECEBE UMA CHAMADA PARA DETERMINAR QUAIS MODALIDADES DE EMPRESTIMO UMA PESSOA TEM ACESSO

  POST  {{host}}/customer-loans

{
   "age": 40,
   "cpf": "123.345.567-78",
   "name":"reginaldo rossi",
   "income": 800.00,
   "location": "RJ"
}

seu serviço deve retornar uma resposta contento o nome do cliente e uma lista de emprestimo aos quais ele tem acesso, com os respectivos tipos e taxas de juros

{
	"customer": "reginaldo rossi",
	"loans":
 [
	{
		"type": "personal",
		"interest_rate":4
	},
	{
	  "type": "guaranteed",
	  "interest_rate":3
	},
	{
		"type": "consignment",
		"interest_rate":2
	},
]
}
	
REQUISITOS

- CONCEDER EMPRESTIMO PESSOAL SE O SALARIO DO CLIENTE FOR IGUAL OU INFERIOR A R$ 3000
- CONCEDER EMPRESTIMO PESSOAL SE O SALARIO ESTIVER ENTRE 3000 E 5000, SE O CLIENTE TIVER MENOS DE 30 ANOS E RESISDIR EM SP
- CONCEDER EMPRESTIMO CONSIGNADO SE O SALARIO FOR IGUAL OU SUPERIOR A 5000
- CONCEDER EMPRESTIMO COM GARANTIA SE O SALARIO FOR IGUAL OU INFERIOR A 3000
- CONCEDER EMPRESTIMO COM GARANTIA SE O SALARIO ESTIVER ENTRE 3000 A 5000 SE O CLIENTE TIVER MENOS DE 30 ANOS E MORAR EM SP


========================================RESOLUÇÃO=======================================================================
criei uma aplicação com spring boot  com os recursos:
- controller
- service
- dto

para fazer os testes das chamadas dos endpoints usei uma extensao no vscode chamada thunder  client

nessa extensao vc cria um collection e nele é feito so testes do HTTP assim como é feito no INSOMMIA E NO POSTMAN.




