# Análise e identificação de possíveis candidaturas laranjas

Um levantamento das candidaturas de possíveis laranjas na última eleição municipal no país, utilizando Python e a biblioteca de manipulação de dados Pandas.

No decorrer deste trabalho, iremos trabalhar com os dataset's do TSE referentes aos resultados das eleições municipais de 2020.

O art. 10, § 3º, da Lei das Eleições (Lei 9.504 de 30 de Setembro de 1997), determina que 30% (trinta por cento) das candidaturas efetivamente lançadas por um partido político seja destinada ao gênero oposto ao da maioria. Como a maioria dos candidatos são, geralmente, do sexo masculino, esta regra acaba valendo como uma cota mínima de 30% para candidaturas femininas.

O objetivo do nosso trabalho é mapear possíveis candidaturas de fachada, tendo como critério a ausência de votos em candidatos deferidos para disputar o pleito.

## Objetivo

Mapear e identificar possíveis candidaturas de fachada, com base na ausência de votos recebidos, e agrupá-las das seguintes formas:

- Partido;
- Sexo dos candidatos;
- Região/Estado;
- Etnia declarada;
- Grau de escolaridade.

## Metodologia

Para os fins do estudo, definimos as seguintes regras para reconhecer uma candidatura como possível laranja:

- Total de votos recebidos igual a zero;
- Candidatura apta a estar na urna e deferida pela Justiça Eleitoral;
- Disputa do pleito realizada no ano de 2020, disputando o cargo de vereador.

A última condição foi firmada pela improbabilidade de se firmar uma candidatura majoritária ao executivo que não fosse reconhecida e válida.

Os detalhes do estudo, como código utilizado e detalhes dos algoritmos, estão disponíveis <a href="https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/Mapeamento%20de%20poss%C3%ADveis%20candidatos%20laranjas.ipynb">aqui.</a>

Os dados utilizados como fonte são os disponíveis no <a href="https://www.tse.jus.br/hotsites/pesquisas-eleitorais/index.html">Repositório de dados eleitorais do TSE</a>.

Foram utilizadas duas bases do repositório acima, referentes à eleição de 2020:

- <a href="https://cdn.tse.jus.br/estatistica/sead/odsele/votacao_candidato_munzona/votacao_candidato_munzona_2020.zip">Votação nominal por município e zona</a>
- <a href="https://cdn.tse.jus.br/estatistica/sead/odsele/consulta_cand/consulta_cand_2020.zip">Dados dos candidatos</a>

A primeira base nos permite determinar a votação nominal de cada candidato, assim como o estado de sua candidatura. Já a seguinte foi utilizada para extrair dados como sexo, etnia e escolaridade dos supostos concorrentes.

## Resultados

Foram identificadas 4628 candidaturas na situação de zero votos recebidos, mesmo sendo deferidas e disponíveis nas urnas. 
A motivação principal do trabalho foi identificar a proporção entre os sexos neste grupo, uma vez que neste ano há um incentivo de cumprir com a norma citada anteriormente.

Os resultados gerais se encontram abaixo.

![Partido](https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/results/Partido.jpg?raw=true)

![Etnia](https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/results/Etnia1.jpg?raw=true)

![Estadp](https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/results/UF.jpg?raw=true)

![Grau de escolaridade](https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/results/Grau.JPG?raw=true)

Para facilitar a exibição da distribuição destas candidaturas ao redor do país, criamos o mapa abaixo para ilustrar tal situação.

![Mapa](https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/results/Mapa.jpg?raw=true)

Por fim, podemos visualizar a diferença de representação das candidaturas femininas neste grupo.

Vemos aqui que as mulheres representam este grupo desproporcionalmente em relação ao número de homens.
No cenário total possuímos:

- 370.552 candidatos homens;
- 187.082 candidatas mulheres.

Gráficamente, a divisão dos grupos é esta:

![Gênero](https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/results/generoPizzaTotal.jpg?raw=true)

A exata proporção oposta ocorre quando o grupo analisado é o de membros sem nenhum voto:

- 1.549 candidatos homens;
- 3.079 candidatas mulheres.

![Gênero](https://github.com/JDanrley/Mapeamento-Candidatos-Laranjas/blob/main/results/generoPizza.jpg?raw=true)


