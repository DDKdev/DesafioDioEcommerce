Este documento esclarece o contexto de cada entidade e seus relacionamentos, criados para atender a demanda do Desafio:

"Refine o modelo apresentado acrescentando os seguintes pontos:

1- Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;

2- Pagamento – Pode ter cadastrado mais de uma forma de pagamento;

3- Entrega – Possui status e código de rastreio;"

###############################################################
Para resolução do item 1, generalizei a entidade cliente tornando-a Superclasse para a criação de subclasses PessoaFisica e PessoaJuridica. Cada uma delas passa a ter um relacionamento único com a entidade PEDIDO.

Para a resolução do item 2 - PAGAMENTO foi criada um atributo FORMA_DE_PAGAMENTO para que na escolha do tipo de pagamento durante a compra, seja persistido os dados necessários para a efetivação da compra. Por exemplo, escolheu a opção Cartão, então deve-se persistir os dados da entidade Cartão.

Para a resolução do item 3 - ENTREGA, criamos uma entidade TRANSPORTADORA com os dados de quem efetuará a ENTREGA. A entidade ENTREGA é responsável por informar o rastreio.
