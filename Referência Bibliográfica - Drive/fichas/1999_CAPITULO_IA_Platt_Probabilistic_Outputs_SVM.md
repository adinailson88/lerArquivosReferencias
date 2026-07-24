# Probabilistic Outputs for Support Vector Machines and Comparisons to Regularized Likelihood Methods

## Referência

PLATT, John C. Probabilistic Outputs for Support Vector Machines and Comparisons to Regularized Likelihood Methods. In: SMOLA, A. J. et al. (eds.). *Advances in Large Margin Classifiers*. 1999.

- **Arquivo no acervo:** `1999_CAPITULO_IA_Platt_Probabilistic_Outputs_SVM.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1ZSsBRXb3BxuYRPAtzsMJ7rn37p7ygPeT/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** CAPITULO
- **Conferência:** Leitura integral; capítulo em Advances in Large Margin Classifiers

## Síntese detalhada

O capítulo propõe ajustar uma função sigmoide às saídas não calibradas de uma SVM para convertê-las em probabilidades posteriores. O procedimento treina primeiro a SVM e depois estima os parâmetros da sigmoide em dados separados, preservando a esparsidade do classificador.

## Método e escopo

Desenvolvimento metodológico e comparação experimental entre SVM seguida de sigmoide e métodos de kernel treinados por máxima verossimilhança regularizada em três conjuntos de dados.

## Resultados e contribuição

A técnica produz probabilidades de qualidade comparável às alternativas avaliadas e tornou-se conhecida como Platt scaling. Ela diferencia a margem de decisão da probabilidade de acerto e permite decisões baseadas em custo ou limiares.

## Contribuições reutilizáveis

- Calibrar probabilidades de SVM para triagem automática.
- Definir limiares de encaminhamento e revisão humana.
- Comparar com temperature scaling e calibração isotônica.

## Limitações e cuidados

- Exige dados de calibração independentes.
- A forma sigmoide pode não representar todos os padrões de má calibração.
- Pode degradar sob mudança de domínio.

## Aderência ao projeto

- **Classificação:** Muito alta — calibração probabilística de SVM
- **Palavras-chave:** SVM; calibração; Platt scaling; probabilidade posterior; função sigmoide
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use para descrever o Platt scaling. Calibre apenas com dados não usados no ajuste do classificador e verifique confiabilidade em teste temporal.
