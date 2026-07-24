# Framewise Phoneme Classification with Bidirectional LSTM and Other Neural Network Architectures

## Referência

GRAVES, Alex; SCHMIDHUBER, Jürgen. Framewise phoneme classification with bidirectional LSTM and other neural network architectures. *Neural Networks*, v. 18, p. 602–610, 2005. DOI: 10.1016/j.neunet.2005.06.042.

- **Arquivo no acervo:** `2005_ARTIGO_IA_Graves_Bidirectional_LSTM_Phoneme_Classification.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1E7cZ-K2CoQ3UD9aksZJuEqGsquNJGtBT/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; DOI 10.1016/j.neunet.2005.06.042

## Síntese detalhada

O artigo apresenta redes LSTM bidirecionais e uma versão de gradiente completo do algoritmo de treinamento. Na classificação quadro a quadro de fonemas da base TIMIT, redes bidirecionais superaram as unidirecionais, e LSTM treinou mais rapidamente e com maior acurácia que RNNs convencionais e MLPs com janelas temporais.

## Método e escopo

Comparação experimental de arquiteturas MLP, RNN e LSTM, em versões uni e bidirecionais, para uma tarefa sequencial de reconhecimento de fala. O desenho explora informação passada e futura em cada posição da sequência.

## Resultados e contribuição

O estudo demonstra o valor de contexto bidirecional e memória de longo prazo em sequências. Sua contribuição é arquitetural; não é um estudo de classificação de documentos nem de manutenção.

## Contribuições reutilizáveis

- Fundamenta historicamente o uso de LSTM e BLSTM.
- Ajuda a explicar quando a ordem e o contexto da sequência podem ser relevantes.
- Serve para diferenciar tarefas sequenciais de tarefas dominadas por termos isolados.

## Limitações e cuidados

- Domínio de fala e classificação por quadro, distante de textos curtos de chamados.
- Resultados não demonstram superioridade de LSTM em qualquer problema textual.
- Arquiteturas e capacidade computacional refletem o estado da arte de 2005.

## Aderência ao projeto

- **Classificação:** Alta — fundamento arquitetural de BLSTM
- **Palavras-chave:** LSTM bidirecional; redes recorrentes; classificação de fonemas; sequências; TIMIT
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use como referência fundacional de BLSTM. Para justificar sua adoção em chamados, complemente com evidência no domínio e comparação empírica com modelos não sequenciais.
