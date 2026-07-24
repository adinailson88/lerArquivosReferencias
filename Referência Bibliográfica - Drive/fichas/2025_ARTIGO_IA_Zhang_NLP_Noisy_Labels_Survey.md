# A Survey on Learning with Noisy Labels in Natural Language Processing: How to Train Models with Label Noise

## Referência

ZHANG, Han et al. A survey on learning with noisy labels in Natural Language Processing: How to train models with label noise. *Engineering Applications of Artificial Intelligence*, v. 146, art. 110157, 2025. DOI: 10.1016/j.engappai.2025.110157.

- **Arquivo no acervo:** `2025_ARTIGO_IA_Zhang_NLP_Noisy_Labels_Survey.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1jLLAN7auxT9k_dXub_FGK3nDUTcVcuaA/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; DOI 10.1016/j.engappai.2025.110157

## Síntese detalhada

A revisão analisa aprendizagem com rótulos ruidosos em PLN e organiza os métodos em cinco famílias conforme a fase de treinamento: vetores de atributos, matriz de transição, confiança das predições, melhoria da função de perda e ponderação de dados. Também reúne bases, códigos e critérios de comparação.

## Método e escopo

Survey metodológico com classificação das técnicas e avaliação sistemática em seis dimensões. Discute fontes de ruído, relação entre extração de atributos, saída predita e otimização, além de desafios como out-of-distribution.

## Resultados e contribuição

O tratamento de ruído busca reduzir o dano dos rótulos incorretos e aproveitar informação confiável. As técnicas variam em hipóteses, custo, necessidade de dados limpos e compatibilidade com diferentes tarefas; não há método universal.

## Contribuições reutilizáveis

- Mapa de técnicas para rótulos históricos inconsistentes.
- Base para comparar filtragem, reponderação e perdas robustas.
- Suporte ao desenho de auditorias e conjuntos de validação limpos.

## Limitações e cuidados

- Survey secundário; desempenho deve ser conferido nos estudos primários.
- O campo e os códigos evoluem rapidamente.
- Aplicação institucional exige caracterizar o tipo real de ruído.

## Aderência ao projeto

- **Classificação:** Muito alta — tratamento de ruído de rótulos em classificação textual
- **Palavras-chave:** PLN; rótulos ruidosos; robustez; matriz de transição; confiança; função de perda; ponderação
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use para taxonomia e seleção inicial de estratégias. Antes de aplicar um método, estime taxa, padrão e origem do ruído no corpus e valide em um conjunto adjudicado.
