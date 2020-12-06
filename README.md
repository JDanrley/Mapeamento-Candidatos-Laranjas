# Análise de possíveis candidaturas laranjas

Um levantamento das candidaturas de possíveis laranjas na última eleição municipal no país, utilizando Python e a biblioteca de manipulação de dados Pandas.

## Objetivo

Mapear e identificar possíveis  candidaturas de fachada, com base na ausência de votos recebidos, e agrupá-las das seguintes formas:

- Partido;
- Sexo dos candidatos;
- Região/Estado;
- Etnia declarada;
- Grau de escolaridade.

## Metodologia

Para os fins do estudo, definimos as seguintes regras para reconhecer uma candidatura como possível laranja:

- Totais de votos recebidos igual a zero;
- Candidatura apta a estar na urna e deferida pela Justiça Eleitoral;
- Disputa do pleito, no ano de 2020, ao cargo de vereador.

A última condição foi firmada pela improbabilidade de se adicionar uma candidatura majoritária ao executivo que não fosse reconhecida e válida.


