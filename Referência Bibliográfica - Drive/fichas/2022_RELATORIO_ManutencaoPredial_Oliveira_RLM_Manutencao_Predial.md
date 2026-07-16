# Previsão do custo de manutenção predial em Universidades Públicas Federais por modelagem com regressão linear — RLM

## Referência

OLIVEIRA, Adinailson Guimarães de. **Previsão do custo de manutenção predial em Universidades Públicas Federais por modelagem com regressão linear — RLM**. 2022. 81 f. Dissertação (Mestrado Profissional em Engenharia Industrial) — Universidade Federal da Bahia, Salvador, 2022. Orientador: Robson da Silva Magalhães.

- **Arquivo no acervo:** `2022_RELATORIO_ManutencaoPredial_Oliveira_RLM_Manutencao_Predial.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1th6MpjS-rvks1XZF8K7XhzEJgo76g9qY/view?usp=drivesdk)
- **Tipo:** dissertação; modelagem quantitativa por regressão linear múltipla.
- **Conferência:** texto integral consultado; 81 folhas no registro e 82 páginas no PDF.

## Síntese detalhada

A dissertação desenvolve uma ferramenta objetiva para prever o custo anual de manutenção predial das universidades federais brasileiras. A finalidade prática é apoiar planejamento orçamentário, PPA e LOA, substituindo ou complementando previsões baseadas apenas no valor executado no ano anterior.

O universo corresponde às 63 universidades federais em funcionamento em 2018. As informações foram extraídas do SIAFI/Tesouro Gerencial, Portal da Transparência e sinopses do ensino superior. A série cobre 2009–2020 e reúne 730 observações; dados mais antigos foram usados no ajuste e os anos recentes em teste temporal.

O desenho inicial combina oito variáveis institucionais observadas em quatro defasagens, totalizando 32 preditores. O procedimento backward, combinado com VIF, significância e Cp de Mallows, reduz o modelo a quatro entradas sem grande perda de ajuste. O texto identifica receita/despesa discricionária do ano anterior, custo de manutenção do ano anterior, obras em andamento com duas defasagens e uma quarta variável defasada em quatro anos.

No treinamento, o modelo final apresentou R² de 89,25% e R² ajustado de 89,14%. O teste F foi 760,03, com p-valor inferior a 0,001; 95,14% dos resíduos padronizados ficaram entre dois desvios-padrão. A análise gráfica foi utilizada para linearidade, normalidade, homoscedasticidade e ausência de autocorrelação.

Na avaliação por ano, o conjunto de teste 2019–2021 apresentou correlação de 86,4% e R² de 74,6%. Considerando 2013–2021, R foi 90,4% e R² 81,8%. O baseline baseado somente no custo do ano anterior alcançou R de 89,7% e R² de 80,5%, indicando ganho global pequeno, embora o modelo ampliado ofereça fundamentação institucional e teste estatístico.

## Variáveis e pipeline reutilizáveis

- **Alvo:** custo anual de manutenção predial por IFES.
- **Fontes:** SIAFI/Tesouro Gerencial, transparência e estatísticas do ensino superior.
- **Painel:** IFES por ano, com quantidade de universidades variável no início da série.
- **Defasagens:** até quatro anos, alinhadas ao ciclo do PPA.
- **Seleção:** backward, VIF, p-valor e Cp de Mallows.
- **Diagnóstico:** ANOVA, resíduos, R, R², R² ajustado e teste temporal.
- **Benchmark:** previsão pelo custo do ano anterior.

## Ponto de conferência obrigatório

Há uma inconsistência interna na apresentação da quarta variável do modelo final. O texto, a Figura 11 e a Tabela 7 indicam custo de manutenção em `t−4`, enquanto a Equação 4.9 imprime `CACt−4`, associado a custo da área construída. Antes de implementar a fórmula, é necessário conferir a base/código original ou confirmar com o autor qual variável foi efetivamente usada. A equação não deve ser copiada automaticamente sem essa verificação.

## Resultados aproveitáveis

1. É a referência central do próprio ecossistema para previsão de custos de manutenção em IFES.
2. A estrutura de painel temporal pode ser estendida com inflação, área, idade, backlog, contratos e categorias de chamados.
3. O baseline forte demonstra que novos modelos precisam ser comparados com persistência temporal.
4. A separação temporal é mais apropriada que divisão aleatória para evitar vazamento entre anos.
5. Métricas de erro absoluto e relativo devem ser acrescentadas, pois R² não informa magnitude monetária do erro.
6. O modelo é interpretável e adequado como baseline para árvores, boosting, modelos hierárquicos e séries temporais.

## Citações verificadas

- “A série de dados coletados compreende 12 anos” (p. 50).
- “redução de 32 variáveis de entradas [...] para 4” (p. 60).
- “coeficiente de determinação (R2) de 81,8%” (p. 70).

## Limitações

- Dados financeiros podem refletir orçamento, contingenciamento e classificação contábil, não apenas necessidade técnica.
- Não há MAE, RMSE, MAPE, intervalos preditivos ou validação por universidade deixada de fora.
- A comparação com o baseline mostra melhora global reduzida em R e R².
- Outliers foram mantidos; isso preserva casos reais, mas pode influenciar fortemente RLM.
- Há a inconsistência de notação da quarta variável mencionada acima.
- Para valores atuais, é necessário atualizar a série e tratar inflação e mudanças contábeis.

## Aderência aos repositórios

- **Máxima e autoral:** `malha-previsao-custos`, `malha-estatisticas-associadas`, `malha-ia`, `pls-ufsb-dashboard`.
- **Muito alta:** `malha-previsao-chamados`, `malha-previsao-filtros`, `malha-ia-regras-llm`.
- **Governança:** `malha-ods-esg`, `classificacao-chamados`, `glpi-google-sheets-sync`.
- **Essencial:** `revisao-bibliografica`, `NOVA-revisao-bibliografica`, `lerArquivosReferencias`.

## Como citar com segurança

Cite como dissertação da UFBA. Para reproduzir o modelo, confira a quarta variável na base ou código original, atualize os valores monetários e reporte também métricas de erro em reais e percentuais.
