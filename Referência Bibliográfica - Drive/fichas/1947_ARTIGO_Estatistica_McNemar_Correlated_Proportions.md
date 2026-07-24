# Note on the Sampling Error of the Difference Between Correlated Proportions or Percentages

## Referência

MCNEMAR, Quinn. Note on the sampling error of the difference between correlated proportions or percentages. *Psychometrika*, v. 12, n. 2, p. 153–157, 1947.

- **Arquivo no acervo:** `1947_ARTIGO_Estatistica_McNemar_Correlated_Proportions.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1nK1DjlyTaNTd_pipQ9gUM82t-pDseG6t/view)
- **Pasta temática:** `03_Predicao_Custos_e_Estatistica`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; Psychometrika, v. 12, n. 2, 1947

## Síntese detalhada

O artigo deriva fórmulas para testar a diferença entre duas proporções correlacionadas, como respostas antes/depois ou resultados de dois métodos aplicados aos mesmos casos. A formulação conduz ao qui-quadrado com um grau de liberdade baseado nos pares discordantes de uma tabela 2×2.

## Método e escopo

Desenvolvimento estatístico analítico para amostras pareadas. Em comparação de classificadores, a tabela é formada pelos casos em que ambos acertam, ambos erram e apenas um dos modelos acerta.

## Resultados e contribuição

O teste avalia se a assimetria entre os dois tipos de discordância é compatível com acaso. Sua pertinência decorre do pareamento: as previsões dos modelos são feitas sobre as mesmas observações e não constituem amostras independentes.

## Contribuições reutilizáveis

- Comparar dois classificadores no mesmo conjunto de teste.
- Evitar teste de proporções independentes quando as predições são pareadas.
- Complementar métricas agregadas com inferência sobre discordâncias.

## Limitações e cuidados

- A forma assintótica pode ser inadequada com poucos pares discordantes.
- O teste não mede magnitude prática nem desempenho por classe.
- Múltiplas comparações exigem controle adicional.

## Aderência ao projeto

- **Classificação:** Muito alta — teste estatístico para predições pareadas
- **Palavras-chave:** teste de McNemar; proporções correlacionadas; dados pareados; qui-quadrado; comparação de classificadores
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use para comparação pareada de dois modelos sobre os mesmos itens, registrando a tabela de discordâncias. Em amostras pequenas, verifique a versão exata e complemente com tamanho de efeito e intervalos.
