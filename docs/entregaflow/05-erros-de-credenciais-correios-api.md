# Erros de credenciais da API dos Correios no WooCommerce

**O problema:** o frete não aparece e o administrador vê um aviso do EntregaFlow.

**"Os Correios recusaram as credenciais":**
1. Confira o usuário do Meu Correios, o código de acesso à API (CWS) e o cartão de postagem em Configurações > EntregaFlow.
2. Ao salvar novas credenciais, o token guardado é descartado e um novo é pedido.
3. Deixe o campo do código de acesso em branco para manter o já salvo.

**"Os Correios recusaram a cotação" (erro 403):** as credenciais foram aceitas, mas o cartão de postagem não tem a API de Preço (serviço 38202) habilitada, ou o código do serviço não está no seu contrato. Peça aos Correios para vincular o serviço 38202 ao cartão e confira os códigos de SEDEX e PAC nas configurações.

**Mais detalhes:** a mensagem dos Correios aparece entre parênteses no aviso, e cada erro fica registrado em WooCommerce > Status > Logs, origem "entregaflow". O aviso some quando uma cotação volta a funcionar.

**Observação:** clientes da loja nunca veem essas mensagens; só quem pode gerenciar a loja.
