# SEDEX e PAC com vários produtos no carrinho

**O problema:** o carrinho tem mais de um produto e o frete não corresponde ao que os Correios cobrariam pelo pacote.

**Como o EntregaFlow calcula:** o carrinho é cotado como um único pacote. Os pesos e os valores declarados são somados; comprimento e largura são os maiores entre os produtos; a altura é o volume total dividido por comprimento × largura. Depois entram o peso da embalagem (somado uma vez) e os centímetros extras (somados a cada lado); por fim, cada lado é arredondado para cima e nunca fica abaixo de 16 × 11 × 2 cm, o menor pacote que o plugin cota. Uma única consulta por serviço é enviada aos Correios.

**Por que configurar a embalagem:** a caixa calculada é a menor possível. Se os Correios cobrarem peso cúbico, a sua caixa real (maior) custa mais. Informe o peso da embalagem e os centímetros extras em Configurações > EntregaFlow para chegar perto da caixa que você usa.

**Passo a passo para conferir:**
1. Use "Conferir com os Correios" em Configurações > EntregaFlow com o peso total e as dimensões da caixa que você realmente usaria.
2. Compare o preço e o peso cobrado com o simulador do seu contrato.

**Limites:** os Correios aceitam até 30 kg, 100 cm em qualquer lado e 200 cm somando os três; acima disso o plugin informa o motivo ao gerente da loja em vez de mostrar um preço errado.
