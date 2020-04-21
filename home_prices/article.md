# Como vai evoluir o preço das casas no pós-pandemia

Parece um problema distante mas nos últimos 2 anos uma das questões mais
presente no dia-a-dia de muitos jovens portugueses é de como vão evoluir o preço
das casas. Apesar de as taxas de juro para crédito a habitação estarem em
mínimos históricos o preço das casas tem estado a aumentar constantemente.

![Comparação do preço das casas com a taxa de juro para crédito a
habitação](https://github.com/manuelfcreis/research/blob/master/home_prices/figures/juro.png?raw=true)

Uma das consequências da pandemia que está agora a atacar o mundo é que, muito
provavelmente, o preço das casas vai descer. Neste artigo quero tentar fazer uma
previsão simples do que poderá ser a trajetória de evolução.

O caminho até à previsão é explicado em baixo. Mas deixo já aqui o resumo. 

![Previsão evolução preço das
casas](https://github.com/manuelfcreis/research/blob/master/home_prices/figures/previsão.png?raw=true)

A minha previsão é que as casas caiam cerca de 14.43%. Para chegar a este número
assumi que algumas variávels chaves vão cair em 2020, a tabela em baixo resume
as mudanças.

| Variavel                       | Tipo        | 2019   | 2020    |
|:------------------------------:|-------------|:------:|:-------:|
| Preço das casas                | crescimento | 9.20%  | -14.43% |
| Construção                     | crescimento | 12.33% | -24.00% |
| Noites de Turistas             | crescimento | 5.50%  | -20.00% |
| Registos alojamento local      | crescimento | 13.56% | -20.00% |
| Taxa de juro crédito habitação | valor       | 1.41%  | 1.83%   |

Estas estimativas de variações vêm de valores históricos e da previsão por parte
do governo de que por cada com o país fechada perdemos 6% do PIB. Se
considerarmos um fecho de 2 a 3 meses e ajustarmos as variáveis acima tendo isso
em conta chegamos a valores parecidos. 

Em termos mais práticos signfica que, em média, uma casa que valia 300 000 € vai
passar a valer, no fim de 2020, cerca de 260 000 €.

Esta previsão tem muitas falhas e não passa de um exercício intelectual. Espero
que não façam decisões de investimento com base em números criados desta forma
*bruta*. O que era importante para mim neste exercício era fazer uma estimativa
por alto para tentar medir o que pode acontecer.

Tudo isto é dependente de como evolui a pandemia e
numa reabertura da economia no fim de Maio. A incerteza é tanta que não vale
muito a pena fazer previsões, é só mesmo para quem está aborrecido em casa como
eu.

## Dados

O preço das casas tem súbido em Portugal devido a muitos factores. Sendo que o
imobiliário é um ativo como tantos outros sabemos que isto se deve as forças do
mercado no país. Mas quais são essas forças?

* O alojamento local cresceu para mais do dobro entre 2016 e 2019 aumento muito a
procura por casas em zonas mais turisticas da cidade. 

![Preço das casas e alojamento
local](https://github.com/manuelfcreis/research/blob/master/home_prices/figures/casas_alojamento_local.png?raw=true)

* Turismo aumentou consistentemente durante os últimos anos
![Turismo e preço das casas](https://github.com/manuelfcreis/research/blob/master/home_prices/figures/turismo.png?raw=true)

* O número de vistos gold também teve um aumento significativo, mas o número em
  absoluto é relativamente baixo - no máximo 1 500 vistos gold por ano.

* As taxas de juro baixaram consideravelmente nos últimos anos como demostra o
  primeiro gráfico do artigo.
  
* A construção voltou a aumentar no país. Não é certo qual o destino desta
  construção. Caso tenha sido para fazer novos edificios semelhantes aos
  existentes teria um efeito negativo no preço das casas. No entanto é provavel
  que tenha principalmente ou para o setor de alojamento local ou para
  propriedades de luxo, que irá fazer o preço subir.
  
Por fim, existem alguns factores que poderiam ter efeito mas que não mostraram
grande evolução neste periodo.

* O número de pessoas em Portugal, e em especial nas cidades, não aumentou
  consideravelmente. Este poderia ser um factor importante num aumento da
  procura de imobiliário mas não aconteceu.
* O rendimento dos portugueses não aumentou consideravelmente. Caso
  tivesse existido um aumento nos rendimentos seria possível que as rendas e o
  preço das casas acompanhasse. Na realidade o que aumentou foi o peso do
  imobiliário nos orçamentos familiares. 
  
## Previsão

Para fazer esta previsão utilizei métodos bastantes simples. O código está
inteiramente disponível no
[Github](https://github.com/manuelfcreis/research/tree/master/home_prices).

Utilizei um ARMA(1, 0), com alguns dos factores acima mencionados, sempre em
crescimento percentual. Retirei os golden visas da análise porque não existiam dados para todo o periodo e acabavam por
não melhorar a análise.

![Previsão evolução preço das
casas](https://github.com/manuelfcreis/research/blob/master/home_prices/figures/previsão.png?raw=true)

