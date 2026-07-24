# Term-Weighting Approaches in Automatic Text Retrieval

## Referência

SALTON, Gerard; BUCKLEY, Christopher. Term-weighting approaches in automatic text retrieval. *Information Processing & Management*, v. 24, n. 5, p. 513–523, 1988.

- **Arquivo no acervo:** `1988_ARTIGO_IA_Salton_Buckley_Term_Weighting_Text_Retrieval.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/16HdkHSc3wsUgUWhCcah05kYjmGFQsr5o/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; Information Processing & Management 24(5)

## Síntese detalhada

O artigo sistematiza esquemas de ponderação de termos em recuperação automática de textos e compara oito métodos em coleções experimentais. Discute frequência do termo, frequência inversa nos documentos, normalização pelo comprimento e ponderação de consultas. As combinações completas e normalizadas apresentaram desempenho forte e servem como baseline para representações mais complexas.

## Método e escopo

Comparação experimental de modelos de indexação de termos em várias coleções de recuperação de informação, usando precisão média e ranking. O texto formaliza vetores de documentos e consultas e a similaridade cosseno.

## Resultados e contribuição

A eficácia depende da combinação entre importância local, discriminação global e normalização. O TF-IDF sem normalização não é universalmente o melhor; características das consultas e coleções alteram o ranking dos esquemas.

## Contribuições reutilizáveis

- Fundamenta TF-IDF, vetores esparsos e similaridade cosseno.
- Justifica baselines para classificação e busca de chamados semelhantes.
- Alerta para documentar normalização e variante de ponderação.

## Limitações e cuidados

- Foco original em recuperação de informação, não classificação supervisionada.
- Coleções e métricas são históricas.
- Resultados dependem de tokenização, consultas e corpus.

## Aderência ao projeto

- **Classificação:** Muito alta — fundamento de TF-IDF e representação textual
- **Palavras-chave:** TF-IDF; recuperação de informação; ponderação de termos; modelo vetorial; similaridade cosseno
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Cite para a base conceitual da ponderação de termos. Informe a variante de TF-IDF, normalização e parâmetros realmente usados no pipeline.
