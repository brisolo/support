# Frete dos Correios diferente do valor do contrato no WooCommerce

**O problema:** o frete que o WooCommerce mostra no carrinho não bate com o valor que o simulador dos Correios mostra para o seu contrato.

**Por que acontece:** quase sempre a diferença está nos dados enviados: peso, dimensões, valor declarado ou CEP. Um produto sem peso ou com dimensão errada muda o preço, e a caixa real costuma ser maior que a soma dos produtos (peso cúbico).

**Como conferir, passo a passo:**
1. Em Configurações > EntregaFlow, role até "Conferir com os Correios".
2. Informe o CEP de destino, o peso em gramas, comprimento, largura, altura e o valor.
3. Clique em Conferir. A tabela mostra exatamente o que foi enviado aos Correios (já com a embalagem configurada), o peso cobrado e o preço devolvido para SEDEX e PAC.
4. Digite os mesmos valores no simulador do seu contrato. Se o simulador mostrar o mesmo preço, a diferença que você viu no carrinho vem do cadastro dos produtos (peso ou dimensões) ou da embalagem: ajuste o peso da embalagem e os centímetros extras em Configurações > EntregaFlow. Se mostrar outro preço com os mesmos dados, abra um chamado em https://github.com/brisolo/support/issues com a tabela (sem o código de acesso).

**Valor declarado:** se você posta com valor declarado, ative "Cotar com valor declarado" nas configurações; sem isso a cotação sai sem a taxa do valor declarado. O valor declarado enviado é o total do carrinho. Os Correios têm um valor máximo por serviço (menor no PAC); se recusarem o valor, aquele serviço é cotado sem valor declarado e a recusa fica registrada em WooCommerce > Status > Logs.

**Onde o EntregaFlow ajuda:** ele usa as credenciais do seu próprio contrato e mostra os valores enviados. Ele não garante que o valor final cobrado pelos Correios seja igual ao cotado.
