# Text Categorization with Support Vector Machines: Learning with Many Relevant Features

## Referência

JOACHIMS, Thorsten. Text Categorization with Support Vector Machines: Learning with Many Relevant Features. In: *Machine Learning: ECML-98*. Berlin: Springer, 1998.

- **Arquivo no acervo:** `1998_ARTIGO_IA_Joachims_Text_Categorization_SVM.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1vPRVi3Uc61eL6MRE6P5IeYn0PXSKzvUx/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; ECML 1998

## Síntese detalhada

O trabalho investiga SVM em classificação de textos de alta dimensionalidade e mostra que margens máximas são adequadas a representações esparsas com muitos atributos relevantes. Em experimentos com categorias Reuters, SVM apresentou resultados competitivos ou superiores aos métodos comparados e exigiu pouca seleção manual de atributos.

## Método e escopo

Estudo experimental com documentos representados por termos, treinamento supervisionado e comparação com algoritmos tradicionais da época. A análise relaciona propriedades do espaço textual — alta dimensionalidade, vetores esparsos e muitos atributos informativos — ao comportamento das SVMs.

## Resultados e contribuição

A principal contribuição é estabelecer SVM como baseline forte para categorização textual. A vantagem decorre do controle de capacidade pela margem, e não de redução agressiva da dimensionalidade.

## Contribuições reutilizáveis

- Fundamenta LinearSVC/SVM como baseline para chamados.
- Ajuda a justificar TF-IDF esparso em problemas com muitas palavras relevantes.
- Serve como referência histórica para comparação com modelos profundos.

## Limitações e cuidados

- Experimentos antigos e corpus em inglês.
- Não aborda calibração probabilística nem deriva temporal.
- Resultados dependem do pré-processamento e da taxonomia.

## Aderência ao projeto

- **Classificação:** Muito alta — fundamento de SVM para classificação textual
- **Palavras-chave:** SVM; classificação textual; alta dimensionalidade; Reuters; aprendizado supervisionado
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use como fundamento metodológico das SVMs em texto. A superioridade deve ser testada no corpus atual, com métricas por classe e validação temporal.
