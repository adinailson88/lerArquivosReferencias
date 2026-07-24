# Technical Language Processing for Prognostics and Health Management: Applying Text Similarity and Topic Modeling to Maintenance Work Orders

## Referência

SUNDARAM, Sarvesh; ZEID, Abe. Technical language processing for Prognostics and Health Management: applying text similarity and topic modeling to maintenance work orders. *Journal of Intelligent Manufacturing*, v. 36, p. 1637–1657, 2025. DOI: 10.1007/s10845-024-02323-4.

- **Arquivo no acervo:** `2025_ARTIGO_IA_Sundaram_Technical_Language_Processing_Maintenance_Orders.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1Fyg68snI0SGWGOFCwlk0UAqWNCdXy00x/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; DOI 10.1007/s10845-024-02323-4

## Síntese detalhada

O estudo propõe Technical Language Processing para lidar com abreviações, jargão e textos pouco estruturados de ordens de manutenção. Em registros de aeronaves, compara similaridade sintática com TF-IDF e semântica com BERT para recomendar ações corretivas e aplica LDA para identificar tópicos e relacioná-los a códigos padronizados JASC/ATA.

## Método e escopo

Abordagem não supervisionada com especialista no ciclo, escolhida porque os registros não possuíam rótulos adequados para classificação e uma mesma falha podia admitir ações diferentes. São calculadas similaridades cosseno e extraídos três tópicos dominantes.

## Resultados e contribuição

TF-IDF e BERT produziram recomendações complementares; em alguns casos a correspondência lexical foi mais apropriada, em outros a semântica. A modelagem de tópicos indicou predominância de problemas ligados ao motor e sistemas próximos.

## Contribuições reutilizáveis

- Estrutura para busca de chamados semelhantes e recomendação de soluções.
- Justifica combinar sinais lexicais e semânticos.
- Mostra uso de códigos técnicos e human-in-the-loop.

## Limitações e cuidados

- Domínio de aviação e vocabulário altamente especializado.
- Validação principalmente por coerência e similaridade, sem teste operacional controlado.
- Ano on-line 2024 e volume final 2025 devem ser distinguidos.

## Aderência ao projeto

- **Classificação:** Muito alta — PLN técnico aplicado a ordens de manutenção
- **Palavras-chave:** linguagem técnica; ordens de manutenção; PHM; TF-IDF; BERT; LDA; aviação
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use como referência metodológica para PLN técnico e recomendação por similaridade. A validade das ações requer especialista e avaliação operacional no domínio local.
