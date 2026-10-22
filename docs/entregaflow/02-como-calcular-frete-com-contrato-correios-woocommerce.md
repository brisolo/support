# Como calcular frete com contrato dos Correios no WooCommerce

**O problema:** você tem contrato com os Correios e quer que o WooCommerce cote SEDEX e PAC com o preço do seu contrato.

**Passo a passo:**
1. Tenha em mãos o usuário do Meu Correios, o código de acesso à API (CWS), o número do cartão de postagem e o número do contrato com a sua DR (Diretoria Regional). O cartão precisa ter a API de Preço (serviço 38202) habilitada.
2. Instale e ative o EntregaFlow.
3. Em Configurações > EntregaFlow, preencha usuário, código de acesso, cartão de postagem, número do contrato, DR e o CEP de origem. Sem contrato e DR preenchidos, o plugin não envia o contrato na cotação.
4. Confira os códigos dos serviços: o padrão é 03220 (SEDEX) e 03298 (PAC); se o seu contrato usa outros (por exemplo 04162 e 04669), informe-os. Marque SEDEX e/ou PAC.
5. Se você posta com valor declarado, ative "Cotar com valor declarado". Informe o peso da embalagem e os centímetros extras por lado da sua caixa.
6. Em WooCommerce > Configurações > Entrega, adicione o método EntregaFlow à zona do Brasil.
7. Confira se cada produto tem peso e dimensões cadastrados.
8. Use "Conferir com os Correios" com um pacote e compare com o simulador do seu contrato.

**Onde o EntregaFlow ajuda:** as credenciais ficam no banco de dados do seu site e são enviadas somente a api.correios.com.br. Não há chave compartilhada.
