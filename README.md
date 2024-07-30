
<div align="center">
  <img src="https://portal.cin.ufpe.br/wp-content/uploads/2020/07/Horizontal-Vermelho-Logotipo-CIn-UFPE.png" alt="logo_cin" width="400" height="auto" style="border-radius:20px;" />
  <h2>
    Banco de Dados - CIN UFPE
  </h2>
  <h1>
    Projeto — Comedoria 2024.1
  </h1> 
</div> 


## 🎯 Objetivo: 

Um sistema de gerenciamento de salgados para auxiliar as vendas feitas pela equipe de Marcelinho Salgados e reservas feitas por clientes.


## Introdução

Diante do processo de venda desses salgados, surgiu a necessidade da criação de um sistema de reservas, para que os alunos possam indicar o interesse na compra de salgados específicos, sistema esse que auxiliaria também no controle de vendas, cadastro de clientes e funcionários, obtenção e análise de dados.


## 🧠 Equipe: 

 Arthur Luis de Farias Alves - alfa@cin.ufpe.br

 Beatriz Helena da Silva Melo - bhsm2@cin.ufpe.br

 Celeste Azul Gomes de Gouveia Pereira - caggp@cin.ufpe.br

 Dayane Camile Bezerra de Lima - dcbl@cin.ufpe.br

 Felipe de Vasconcelos Melo - fvm@cin.ufpe.br

 Leonardo Bezerra de Oliveira - lbo@cin.ufpe.br

 Maria Antonia Monteiro da Silva - mams5@cin.ufpe.br
 

## 🔗 Links:

Notion do projeto: https://www.notion.so/ffe3b257ecd64d4e976b589e21f3f66d?v=513785d499704759b375abb23bf55c91&pvs=4


## 📝 Requisitos da modelagem
Como explicado anteriormente, a modelagem do banco foi construída a partir do contexto do Empreendimento Marcelinho Salgados;
O foco principal do projeto são as reservas e as vendas que ocorrem no empreendimento.

Os requisitos da modelagem foram atendidos da seguinte forma:

- Atributos:
  - Composto, multivalorado
  
    - Horario, Sabor

- Relacionamentos:

  - Relacionamento 1:1, 1:N, N:M
    - Cliente-CartãoFidelidade, Funcionário-Venda, Reserva-Salgados

  - Relacionamento parcial-total, parcial-parcial

    - Funcionario-Pedido,Cliente-Salgado

  - Relacionamento Unário ou Auto Relacionamento, N-ário

    - Funcionário-Funcionário, Cliente-Reserva-Salgado

  - Relacionamento Identificador ou Entidade Fraca
     
    - Cliente-CartãoFidelidade

 - Outros:

    - Herança (qualquer tipo)

      - Pedido-Venda-Reserva , Funcionario-Gerente-Vendedor
