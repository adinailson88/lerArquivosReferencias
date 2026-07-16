# BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding

## Referência

DEVLIN, Jacob; CHANG, Ming-Wei; LEE, Kenton; TOUTANOVA, Kristina. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. In: *Proceedings of NAACL-HLT 2019*. Minneapolis: Association for Computational Linguistics, 2019. p. 4171-4186.

- **Arquivo no acervo:** `2019_ARTIGO_IA_Devlin_BERT_Pretraining_Transformers.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1C6BJKE0KFuic9hyqf3JeX4w8FTUe9lnR/view?usp=drivesdk)
- **Tipo:** artigo de representação de linguagem, pré-treinamento e transferência para tarefas de PLN.
- **Conferência desta ficha:** PDF integral legível; objetivos, arquitetura, pré-treinamento, ajuste fino e resultados conferidos no texto.

## Síntese detalhada

O artigo apresenta o BERT, modelo de representação de linguagem baseado no encoder do Transformer e pré-treinado de forma profundamente bidirecional. A contribuição central é permitir que cada token seja representado considerando simultaneamente o contexto à esquerda e à direita em todas as camadas. Essa característica diferencia o BERT dos modelos autorregressivos então predominantes, que restringiam a atenção a uma única direção.

O fluxo metodológico possui duas etapas. No pré-treinamento, o modelo aprende representações gerais a partir de grandes coleções não rotuladas. No ajuste fino, os mesmos parâmetros são inicializados com o modelo pré-treinado e atualizados usando os dados rotulados de cada tarefa. A arquitetura de entrada e o encoder permanecem praticamente iguais entre tarefas; normalmente é acrescentada apenas uma camada de saída específica.

O BERT usa embeddings WordPiece com vocabulário de 30 mil unidades. Cada entrada combina embeddings de token, segmento e posição. O token especial [CLS] representa a sequência completa em tarefas de classificação; [SEP] separa segmentos. Essa configuração permite tratar uma descrição isolada ou um par de textos, como descrição e solução de um chamado.

O pré-treinamento original combina duas tarefas. Na modelagem de linguagem mascarada, 15% dos tokens são selecionados para predição: 80% são substituídos por [MASK], 10% por um token aleatório e 10% permanecem inalterados. O objetivo é recuperar o token original usando o contexto bidirecional. Na predição da próxima sentença, metade dos pares contém a sentença subsequente real e metade uma sentença aleatória, buscando aprender relações entre segmentos.

O artigo avalia duas configurações principais. BERT Base possui 12 camadas, dimensão oculta 768, 12 cabeças de atenção e aproximadamente 110 milhões de parâmetros. BERT Large possui 24 camadas, dimensão 1.024, 16 cabeças e aproximadamente 340 milhões de parâmetros. A dimensão interna das redes feed-forward corresponde a quatro vezes a dimensão oculta.

O pré-treinamento utilizou BooksCorpus e Wikipédia em inglês. O ajuste fino foi aplicado a 11 tarefas, incluindo classificação de sentenças, inferência textual, similaridade, resposta a perguntas e reconhecimento de entidades. No GLUE, a representação agregada do token [CLS] alimenta uma camada de classificação treinada conjuntamente com todo o encoder.

Os resultados reportados estabeleceram novo estado da arte nas 11 tarefas avaliadas. O BERT alcançou média 80,5 no GLUE, acurácia 86,7% no MultiNLI, F1 93,2 no SQuAD v1.1 e F1 83,1 no SQuAD v2.0. Os estudos de ablação mostraram que bidirecionalidade, modelagem mascarada e tamanho do modelo contribuíram para os ganhos.

## Método e evidências

- **Arquitetura:** encoder Transformer bidirecional.
- **Pré-treinamento:** masked language modeling e next sentence prediction.
- **Entrada:** embeddings de token, segmento e posição; tokens especiais [CLS] e [SEP].
- **Modelos:** Base com 110 milhões e Large com 340 milhões de parâmetros.
- **Corpora:** BooksCorpus e Wikipédia em inglês.
- **Avaliação:** 11 tarefas de PLN, incluindo GLUE, MultiNLI e SQuAD.
- **Transferência:** ajuste fino de todos os parâmetros com pequena camada específica por tarefa.

## Resultados aproveitáveis nos projetos

1. O uso do token [CLS] fornece uma representação contextual da descrição completa para classificação de chamados.
2. O ajuste fino permite reutilizar conhecimento linguístico aprendido em grandes corpora com uma base institucional rotulada menor.
3. Pares de segmentos podem representar descrição e solução, chamado e categoria ou solicitação e resposta técnica.
4. Modelos BERT adaptados ao português devem ser comparados com TF-IDF e classificadores lineares para demonstrar ganho efetivo.
5. O pré-treinamento não elimina a necessidade de taxonomia consistente, auditoria dos rótulos e validação temporal.
6. O custo computacional e a latência justificam avaliar versões compactas, congelamento de camadas e embeddings pré-calculados.

## Limitações e cuidados

- O modelo original foi pré-treinado em inglês; aplicação em português exige modelo adequado ao idioma e ao domínio.
- Os benchmarks avaliados não representam chamados de manutenção nem linguagem administrativa brasileira.
- O tamanho dos modelos aumenta custo de treinamento, inferência, armazenamento e reprodutibilidade.
- O artigo não trata diretamente desbalanceamento severo, deriva dos dados, calibração ou governança operacional.
- A tarefa de próxima sentença foi posteriormente reavaliada em outras arquiteturas; não deve ser tratada como requisito universal.
- Resultados em benchmarks gerais não garantem melhoria nas categorias e subcategorias do GLPI.

## Aderência aos projetos

- **Classificação de chamados e PLN:** muito alta.
- **Malha IA:** muito alta para modelos contextuais, transferência e comparação com baselines.
- **Governança de dados:** alta quando associado a auditoria de rótulos, monitoramento e explicabilidade.
- **Manutenção preditiva:** indireta, pela estruturação de informação textual para integração a modelos de risco.
- **ODS/ESG:** alta para classificação semântica de documentos quando houver conjunto rotulado adequado.

## Como citar em pesquisas do acervo

Use o artigo para fundamentar representações contextuais bidirecionais, masked language modeling, ajuste fino e uso do token [CLS] em classificação. Não atribua ao BERT original desempenho em português ou em manutenção predial sem validação empírica específica.
