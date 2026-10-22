# Ler o código do serviço dos Correios no pedido (ERP e etiquetas)

**O problema:** sistemas de ERP e de etiquetas precisam saber se o pedido foi enviado por PAC ou SEDEX, mas o método de entrega aparece sempre com o mesmo identificador.

**A solução:** o EntregaFlow grava o código do serviço dos Correios escolhido na meta do pedido `_entregaflow_product_code` (por exemplo 03220 para SEDEX e 03298 para PAC, ou os códigos do seu contrato). O resumo do pacote cotado fica no item de entrega do pedido, na meta `_entregaflow_breakdown`.

**Passo a passo:** na integração, leia a meta do pedido com esse nome. Se estiver vazia, o pedido não usou um método de entrega do EntregaFlow. Funciona com o checkout clássico e com o checkout em blocos, e com o armazenamento de pedidos HPOS.

**Limites:** o EntregaFlow não gera etiquetas nem rastreio nesta versão.
