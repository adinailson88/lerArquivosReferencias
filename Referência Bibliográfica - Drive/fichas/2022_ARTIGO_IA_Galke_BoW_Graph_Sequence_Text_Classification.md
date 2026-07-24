# Bag-of-Words vs. Graph vs. Sequence in Text Classification: Questioning the Necessity of Text-Graphs and the Surprising Strength of a Wide MLP

## Referência

GALKE, Lukas; SCHERP, Ansgar. Bag-of-Words vs. Graph vs. Sequence in Text Classification: Questioning the Necessity of Text-Graphs and the Surprising Strength of a Wide MLP. In: *Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics*, 2022. p. 4038–4051.

- **Arquivo no acervo:** `2022_ARTIGO_IA_Galke_BoW_Graph_Sequence_Text_Classification.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1Nwpby-lbV1Op9oLGNQCmdJtj5Yl_Ov3G/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; ACL 2022, p. 4038–4051

## Síntese detalhada

O artigo compara 16 métodos de classificação textual organizados em três famílias: bag-of-words, modelos baseados em grafos e modelos sequenciais. Em cinco conjuntos de dados, uma MLP larga alimentada por bag-of-words supera TextGCN e HeteGCN e se aproxima de HyperGAT; BERT e DistilBERT obtêm os melhores resultados gerais. A análise também mostra que a MLP é menor e mais rápida em textos longos.

## Método e escopo

Revisão orientada por experimentos e reprodução de sete modelos em cinco benchmarks, combinando resultados próprios e números publicados. O foco é classificação indutiva, custo computacional, tamanho do modelo e desempenho preditivo.

## Resultados e contribuição

A principal contribuição é demonstrar que complexidade arquitetural não garante vantagem sobre baselines bem ajustados. A WideMLP é proposta como baseline forte e controlável, enquanto Transformers entregam maior desempenho ao custo de mais parâmetros e atenção quadrática no comprimento da sequência.

## Contribuições reutilizáveis

- Justifica manter TF-IDF/BoW e modelos lineares ou MLP como baselines obrigatórios.
- Oferece critérios conjuntos de desempenho, tamanho, treinamento e inferência.
- Ajuda a interpretar ganhos de BERT sem atribuí-los automaticamente à arquitetura mais complexa.

## Limitações e cuidados

- Os benchmarks são gerais e não representam diretamente chamados de manutenção em português.
- Parte das comparações usa resultados da literatura, sujeitos a diferenças de protocolo.
- Eficiência depende do hardware e da implementação.

## Aderência ao projeto

- **Classificação:** Muito alta — seleção de modelos e baselines para classificação textual
- **Palavras-chave:** classificação textual; bag-of-words; MLP; BERT; DistilBERT; redes neurais em grafos; eficiência
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Cite para sustentar a necessidade de baselines fortes e a avaliação conjunta de desempenho e custo. Não use os rankings dos benchmarks como previsão direta para o corpus institucional.
