# BancoDeDados-LojaDeRoupas
Projeto completo de banco de dados para uma loja de roupas criado em SqlServer.

# Descrição
O projeto conta com Modelo Entidade Relacionamento (MER), Projeto Lógico e Físico do banco de dados.

O sistema de controle da loja foi construído para atender as necessidades de automação das atividades de uma loja de roupas femininas.
A loja possui clientes, funcionários (pessoas físicas) e fornecedores (pessoa jurídica). Como forma de estímulo, os vendedores possuem uma porcentagem de comissão fixa mensal sobre a conclusão das vendas, esse valor pode ser alterado conforme metas são atingidas porém esse valor nunca excede 20%. A porcentagem de comissão e o salário base são utilizados para calcular o salário bruto. Para se executar o processo de venda, o funcionário responsável deve entrar com login e senha na área do sistema que é voltada a isso, sendo que o login só é válido dentro do período entre data de contratação e data de desligamento. Os clientes possuem apenas código cliente usado para ver a quantidade de compras que aquele cliente realizou. Os fornecedores podem estar ativos ou não (status) e possuem um prazo de entrega em dias. 
As roupas são divididas em categorias (social, finas, etc), sendo que uma roupa contém apenas uma categoria. O atributo qtd_estoque é controlado por uma trigger e frequentemente atualizado dependendo das compras e vendas.
O Funcionário atende Cliente que gera uma Venda com data e se é troca ou não. Essa Venda é composta por Roupas, cada roupa é vendida em uma certa quantidade e um valor especificado em cada roupas, no entanto esse valor pode variar aplicando-se descontos.
Como a loja trabalha com descontos dependendo da forma de pagamento, é necessário deixar registrado as formas de pagamento disponíveis com seus respectivos descontos. Além disso, uma venda pode possuir mais de uma forma de pagamento, sendo que o valor do desconto aplicado é proporcional ao valor a ser pago por aquela forma de pagamento.
Por fim, o funcionário realiza pedidos aos fornecedores, gerando um pedido de compra de roupas com data de pedido e data de entrega para que seja possível calcular o tempo que o pedido demorou para ser entregue e se está dentro do prazo definido no fornecedor. Além disso, os funcionários com nível de acesso mais alto são responsáveis pelo cadastro de despesas como contas a pagar (água, luz) e pagamento dos funcionários, devendo ser registrados a data de pagamento e vencimento assim como o valor.
Funcionalidades:
- cadastrar clientes, funcionários, fornecedores, roupas, categorias, formas de pagamento e despesas;
- realizar venda para um cliente listando as roupas compradas e suas respectivas quantidades e preço de venda, calculando os totais e subtotais;
- consultar vendas por clientes e por vendedor;
- consultar vendas por roupas;
- realizar pedido para um fornecedor listando as roupas encomendas, suas respectivas quantidades e preço de custo no momento em que foi comprado, calculando totais e subtotais;
- consulta de pedidos por fornecedor e cliente;
- consultar pedidos por fornecedores;
- consultar quais fornecedores entregam no prazo;
- consultar formas de pagamento mais utilizadas;
- consultar despesas que ainda precisam ser pagas;
- consultar saldo de caixa;
- consultar quantidade gasto/ganho em um dia;
