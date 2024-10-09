# Modelo Lógico

Funcionário (<ins>CPF</ins> , nome, salgados_vendidos, info_email, info_telefone)

Gerente (<ins>CPF</ins>, valor_total)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;CPF → Funcionario (CPF)

Vendedor (<ins>CPF</ins>)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;CPF → Funcionario (CPF)

HorarioVendedor (<ins>CPF, horario</ins>)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;CPF → Funcionario (CPF)

Cobre (<ins>Faltante, Cobridor</ins>, data)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Faltante → Funcionario(CPF)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Cobridor → Funcionario(CPF)

Cliente (<ins>email</ins>, nome, pontos)

Salgado (<ins>nome, sabor</ins>, estoque, preço)
	
Pedido (<ins>ID</ins>, data, tipo_pagamento)

ReservaOnline (<ins>IDPedido</ins>, turno, ativo, EmailCliente!)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IDPedido → Pedido(ID)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EmailCliente → Cliente(Email)

VendaFisica(<ins>IDPedido</ins>, e_proprio)
	
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IDPedido → Pedido(ID)

PedidoSalgado(<ins>IDPedido, TipoSalgado, SaborSalgado</ins>, quantidade_salgados)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IDPedido → Pedido(ID)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TipoSalgado, SaborSalgado → Salgado(tipo, sabor)

Vende (<ins>IDPedido</ins>, [CPFFuncionario]!, turno)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IDPedido → Pedido(ID)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;CPFFuncionario → Funcionario (CPF)

SaborSalgado (<ins>TipoSalgado, sabor)
	
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TipoSalgado → Salgado(tipo)

Promoção (<ins>ID</ins>, valor, [IDVenda]!)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IDVenda -> Venda(IDPedido)
