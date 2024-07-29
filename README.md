# Projeto Comedoria
Projeto para a cadeira de Banco de Dados e Engenharia de Software
Projeto para a cadeira de Banco de Dados e Engenharia de Software 
## Equipe: 

 Celeste Azul Gomes de Gouveia Pereira - caggp@cin.ufpe.br

 Maria Antonia Monteiro da Silva - mams5@cin.ufpe.br

 Beatriz Helena da Silva Melo - bhsm2@cin.ufpe.br

 Dayane Camile Bezerra de Lima - dcbl@cin.ufpe.br

 Felipe de Vasconcelos Melo - fvm@cin.ufpe.br

 Arthur Luis de Farias Alves - alfa@cin.ufpe.br

 Leonardo Bezerra de Oliveira - lbo@cin.ufpe.br

## Descrição do projeto:
Um sistema de gerenciamento de salgados para auxiliar as vendas feitas pela equipe de Marcelinho Salgados.
Diante do processo de venda desses salgados, surgiu a necessidade da criação de um sistema de reservas, para que os alunos possam indicar o interesse na compra de salgados específicos, sistema esse que auxiliaria também no controle de vendas, cadastro de clientes e funcionários, obtenção e análise de dados.

## Entidades e seus respectivos requisitos

# Cliente:
Cliente pode completar cadastro informando CPF, NOME e CONTATO;
CPF de Cliente único no banco de dados;
Campo CONTATO do Cliente deve conter e-mail e/ou telefone;
Tabela CLIENTE permite cadastro, remoção e visualização de clientes; 
Cliente pode visualizar Tabela SALGADOS para ver disponibilidades;
Cliente pode visualizar Tabela PEDIDO pessoal com histórico de reservas;
Cliente não pode visualizar outros Clientes ou outras tabelas, exceto Tabela SALGADOS e PEDIDO.

# Funcionário:
Funcionário pode completar cadastro informando CPF e NOME;
CPF de Funcionário único no banco de dados;
Funcionário GERENTE possui campo “valor total”, representando lucro;
Funcionário VENDEDOR possui campo “salgados vendidos” que gera o valor do seu salário baseado em comissão de vendas;
Funcionário VENDEDOR e tabela COMISSÃO se comunicam para gerar salário e atualizar salgados vendidos;
Funcionário VENDEDOR e tabela HORÁRIO se comunicam para gerar dias e turnos dos vendedores;
Funcionário pode remover e visualizar Clientes;
Funcionário pode cadastrar, atualizar, remover e visualizar Salgados;
Funcionário GERENTE pode remover funcionários da tabela, mas Funcionário VENDEDOR não.

# Salgado: 
Salgados são incluídos informando TIPO, PREÇO, SABOR, STATUS e ESTOQUE;
Salgados são identificados pelo campo TIPO; 
Salgados fora do estoque, recebem campo ESTOQUE como NULL;
Campo STATUS na tabela será derivado do campo ESTOQUE, onde com estoque campo será AVAILABLE e sem estoque NULL;
Tabela SALGADO permite cadastro, atualização, remoção e visualização de salgados;
Tabela SALGADO interage com tabela PEDIDO atualizando estoque;
Ao ser feito um pedido, o ESTOQUE do salgado é diminuído conforme a solicitação.

# Pedido:
Tabela PEDIDO permite registro, cancelamento e retirada de pedidos realizados;
Tabela PEDIDO e CLIENTE possuem ligação por registro de pedido por CPF;
Se o pedido for cancelado, campo ESTOQUE da Tabela SALGADO, referente aos salgados reservados, será atualizada.
Horário:
Funcionário VENDEDOR e tabela HORÁRIO se comunicam para gerar dias e turnos dos vendedores;

# Comissão:
Será gerada a partir de venda e deve ter um Funcionário responsável; 
Tabela PEDIDO irá informar quantidade de salgados vendidos e será possível gerar a comissão;
O funcionário responsável receberá o valor da comissão.
