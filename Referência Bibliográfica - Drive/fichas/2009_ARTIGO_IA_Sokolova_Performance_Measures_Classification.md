# A Systematic Analysis of Performance Measures for Classification Tasks

## Referência

SOKOLOVA, Marina; LAPALME, Guy. A systematic analysis of performance measures for classification tasks. *Information Processing & Management*, v. 45, p. 427–437, 2009. DOI: 10.1016/j.ipm.2009.03.002.

- **Arquivo no acervo:** `2009_ARTIGO_IA_Sokolova_Performance_Measures_Classification.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1Rx7FudvuMsp_OZym_p16y-XNwqOuoezL/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; DOI 10.1016/j.ipm.2009.03.002

## Síntese detalhada

O artigo analisa sistematicamente 24 medidas de desempenho para classificação binária, multiclasse, multirrótulo e hierárquica. Relaciona alterações na matriz de confusão a propriedades de invariância das métricas e constrói uma taxonomia para orientar a escolha de medidas segundo distribuição de classes e qualidade dos rótulos.

## Método e escopo

Análise formal das medidas e estudos de caso de classificação textual. O foco não é escolher uma métrica universal, mas identificar o que cada medida preserva ou altera diante de mudanças na distribuição de rótulos.

## Resultados e contribuição

A avaliação pode mudar conforme a métrica mesmo com o mesmo classificador. Classificação de comunicação humana e classificação documental podem exigir medidas diferentes; representatividade e confiabilidade dos rótulos devem orientar a seleção.

## Contribuições reutilizáveis

- Justifica macro-F1, micro-F1 e métricas por classe.
- Apoia avaliação sob desbalanceamento e mudanças de distribuição.
- Evita depender apenas de acurácia global.

## Limitações e cuidados

- Não cobre todas as métricas e práticas modernas.
- A taxonomia não substitui análise operacional de custo de erro.
- Escolha final depende do objetivo e da prevalência das classes.

## Aderência ao projeto

- **Classificação:** Muito alta — seleção e interpretação de métricas
- **Palavras-chave:** métricas; classificação; matriz de confusão; invariância; multiclasse; multilabel
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use para justificar um conjunto de métricas alinhado ao problema. Declare averaging, classes incluídas e matriz de confusão; não apresente uma única métrica como retrato completo.
