# DS_HouseRocket
  Este Projeto foi desenvolvido durante os meus estudos para o Curso Python: Do Zero ao DS, junto à Comunidade DS. A ideia do trabalho é desenvolver uma solução de 
negócio (encontrar e sugerir os melhores negócios de compra e venda de imóveis) para uma Imobiliária Fictícia (House_Rocket), que utiliza uma plataforma online para 
organizar as suas transações.

1. QUESTÃO DE NEGÓCIO:
Quais imóveis que a House Rocket deveria comprar e por qual preço? 
Uma vez que o imóvel foi comprado, qual o melhor momento para vendê-lo e por qual preço?

2. CONTEXTO:
  
  A House Rocket é uma plataforma digital que trabalha com a compra e venda de imóveis. 
  O objetivo do projeto é encontrar as melhores oportunidades de negócio e assim maximizar a receita.
  A estratégia principal é encontrar as casas com ótimas localizações, preços baixos e margem para venda com preço mais alto, seja pela reforma ou pela oportunidade de 
negócio, gerando assim um lucro maior.
  As casas possuem muitos atributos que as tornam mais ou menos atrativas aos compradores e vendedores e a localização e o período do ano também podem influenciar os 
preços.
  O conjunto de dados que representam o contexto está disponível na plataforma do Kaggle, pelo link https://www.kaggle.com/harlfoxem/housesalesprediction. 
  Esse conjunto de dados contém casas vendidas entre Maio de 2014 e Maio de 2015.

3. HIPÓTESES:
 * H01: Imóveis com vista para a água são 30% mais caros, na média.
 * H02: Imóveis com data de construção menos que 1955, são 50% mais baratos, na média.
 * H03: A área total do terreno dos imóveis sem porão, são 40% maiores que os imóveis com porão.
 * H04: O crescimento do preço de imóveis YoY (year over year) é de 10%.
 * H05: O crescimento do preço dos imóveis MoM (month over month) é de 15%.
 * H06: Imóveis com maior número de quartos são, em média, 10% mais caros.
 * H07: Imóveis que nunca foram reformados são, em média, 20% mais baratos.
 * H08: Propriedades mais antigas que nunca foram reformadas são 40% mais baratas.
 * H09: Imóveis que foram reformados recentemente são, em média, 10% mais caros.
 * H10: Imóveis estado ruim e que ficam à beira-mar são, em média, 10% mais caros.

4. PREMISSAS ADOTADAS NA RESOLUÇÃO DO PROJETO:
* Atributo yr_renovated: Valores de 0 - imóveis que não foram reformados, valores de 1 - imóveis reformados.
* As reformas recentes foram consideradas as que foram feitas no ano 2000 ou após essa data.
* O atributo 'price' é o preço de compra pela empresa House Rocket.
* Os valores de ID duplicados foram removidos e considerados apenas a compra mais recente.
* A localização e o estado do imóvel são fundamentais para a decisão de comprá-lo ou não.
* A análise de preço é sempre em comparação com a região.
* A época é a variável decisiva para a venda dos imóveis.
* O imóvel com 33 quartos foi considerado outlier.
* A coluna waterfront, valor = 0, significa que o imóvel não está localizado com vista para a água e valor =1, significa que o imóvel possui vista para a água 
(mar, lago...).

5. PLANEJAMENTO DA SOLUÇÃO:

a) Produto final: Tabela de recomendação de compra e venda; Tabela com variação de preço regional x sazonalidade; Dashboard interativo.

b) Ferramentas: Linguagem Python, Jupyter Notebook, PyCharm

c) Processo: 
- Coletar os dados do site kaggle, limpeza e organização dos dados e atributos;
- Agrupar os dados por região(zipcode) e encontrar a mediana dos preços dos imóveis;
- Sugerir a compra de imóveis da mesma região, em boas condições e abaixo da mediana de preço; 
- Agrupar imóveis por região (zipcode) e sazonalidade;
- Dentro de cada região e sazonalidade, calcular a mediana de preço;
- Condições de venda:

a) Se o preço da compra for maior que a mediana da região + sazonalidade: 
o preço de venda será igual ao preço da compra + 10%.

b) Se o preço da compra for menor que a mediana da região + sazonalidade: 
o preço de venda será igual ao valor da compra + 30%.

c) Imóveis da mesma região, em boas condições e abaixo do preço mediano.

6. PRINCIPAIS INSIGHTS
* Os imóveis com vista para a água são menos disponibilizados, sendo difíceis de encontrar e, mesmo em condições ruins, são muito mais caros.
* Os meses de maior crescimento no ano analisado foram abril, maio e junho.
* Os imóveis que nunca foram reformados são, em média, 40% mais baratos.
* Os imóveis no outono são, em média, 0.4% mais caros que no inverno.
* Bons negócios podem ser realizados através da compra e venda de imóveis mais baratos que a média, em estado regular ou bom.
* Observando a influência da sazonalidade na realização de compra e venda de imóveis, se o preço de compra, for maior que a média da região, 
o preço de venda deve ser igual ao preço de compra mais 10%. E, se o preço de compra, for menor que a média da região, o preço de venda deve ser o preço de compra 
mais 30%.

7. RETORNO FINANCEIRO
Considerando as estratégias de compra e venda de todos os imóveis sugeridos:
* Custo: $ 11,610,168,601.00	
* Venda: $ 13,726,919,454.10
* Lucro: $ 2,116,750,853.10

8. CONCLUSÃO
O objetivo do projeto era gerar insights para viabilizar a compra e venda de imóveis, identificando as melhores opções de negócios, visando o maior lucro. 
Após a análise dos dados, observou-se a identificação dos imóveis com o melhor preço para compra e que estavam em melhores condições, possibilitando a oportunidade 
de maior rentabilidade nas transações de venda.
O projeto cumpriu seu objetivo, trazendo relatórios capazes de identificar as melhores oportunidades de negócios e um mapa interativo com a localização, média de preço e condições 
dos imóveis.
