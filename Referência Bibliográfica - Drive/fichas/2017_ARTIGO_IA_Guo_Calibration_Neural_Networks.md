# On Calibration of Modern Neural Networks

## Referência

GUO, Chuan et al. On Calibration of Modern Neural Networks. In: *Proceedings of the 34th International Conference on Machine Learning*. PMLR, v. 70, 2017.

- **Arquivo no acervo:** `2017_ARTIGO_IA_Guo_Calibration_Neural_Networks.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1Mh9o_3gZ4R0yvRp6Hy96n1XrUHTgdB1F/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; ICML/PMLR 70, 2017

## Síntese detalhada

O estudo mostra que redes neurais modernas podem ser acuradas e, ao mesmo tempo, mal calibradas, produzindo confiança superior à probabilidade real de acerto. Avalia efeitos de profundidade, largura, weight decay e batch normalization e compara técnicas de pós-processamento. O temperature scaling, com um único parâmetro ajustado em validação, apresentou desempenho de calibração consistentemente forte.

## Método e escopo

Experimentos com arquiteturas de visão e classificação documental, diagramas de confiabilidade e métricas de calibração. Os métodos de pós-processamento são treinados em conjunto de validação separado, preservando a predição de classe.

## Resultados e contribuição

A contribuição central é separar discriminação de calibração. Um modelo pode manter a mesma acurácia após temperature scaling, mas fornecer probabilidades mais compatíveis com sua frequência de acerto.

## Contribuições reutilizáveis

- Fundamenta limiares de confiança para automação de chamados.
- Justifica medir ECE e usar diagramas de confiabilidade além de F1 e acurácia.
- Oferece método simples de calibração pós-hoc.

## Limitações e cuidados

- Calibração pode degradar sob mudança de domínio e deriva temporal.
- O método exige conjunto de validação representativo e separado.
- Os resultados originais não são específicos de português ou manutenção.

## Aderência ao projeto

- **Classificação:** Muito alta — confiabilidade das probabilidades e limiares de automação
- **Palavras-chave:** calibração; redes neurais; temperature scaling; Platt scaling; confiança; ECE
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Cite para justificar avaliação e correção de calibração. Não trate uma probabilidade produzida pelo modelo como confiança operacional válida sem validação temporal no corpus-alvo.
