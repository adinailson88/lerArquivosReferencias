# An Introduction to Information Retrieval

## Referência

MANNING, Christopher D.; RAGHAVAN, Prabhakar; SCHÜTZE, Hinrich. *An Introduction to Information Retrieval*. Cambridge: Cambridge University Press, edição on-line de 2009.

- **Arquivo no acervo:** `2009_LIVRO_IA_Manning_Information_Retrieval.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1DsZiuPAqIuYBsG2OMHZZLkTVgwDH25JA/view?usp=drivesdk)
- **Tipo:** livro técnico; recuperação da informação, classificação textual e aprendizado de máquina.
- **Conferência desta ficha:** texto integral legível no PDF arquivado; estrutura, capítulos e conceitos conferidos na edição on-line de 1º de abril de 2009.

## Síntese detalhada

O livro apresenta os fundamentos teóricos e computacionais da recuperação da informação, desde a representação básica de coleções textuais até classificação, agrupamento e busca na Web. A obra organiza o campo em 21 capítulos e combina explicações conceituais, formalização matemática, algoritmos, exemplos e exercícios. Para o acervo, sua principal utilidade é fornecer a base metodológica para transformar descrições textuais de chamados, ordens de serviço e registros de manutenção em representações adequadas à busca, classificação e análise automatizada.

Os capítulos iniciais descrevem o índice invertido, estrutura que relaciona cada termo aos documentos em que ocorre. A construção desse índice depende de decisões de delineamento documental, codificação, tokenização, remoção de palavras muito frequentes, normalização, lematização ou stemming. O livro mostra que essas decisões não são meramente operacionais, pois alteram o vocabulário, a comparabilidade entre documentos e o equilíbrio entre precisão e cobertura da recuperação.

A obra também sistematiza mecanismos de consulta tolerante, incluindo curingas, índices de k-gramas, distância de edição e correção ortográfica. Em chamados prediais, esses recursos são particularmente relevantes porque os registros apresentam abreviações, erros de digitação, variações regionais, nomes de equipamentos e formas distintas de descrever a mesma falha. A normalização pode melhorar a recuperação, mas precisa preservar termos técnicos discriminantes.

Nos capítulos de ranqueamento, o livro apresenta frequência de termos, frequência inversa de documentos, ponderação TF-IDF, representação vetorial e similaridade do cosseno. Documentos e consultas são representados no mesmo espaço de termos, permitindo ordenar registros por proximidade textual. A obra também aborda campos e zonas, possibilitando atribuir pesos diferentes a título, descrição, categoria, localização ou solução do chamado, além de estratégias para cálculo eficiente dos documentos mais relevantes.

A avaliação de sistemas de recuperação é tratada a partir de coleções de teste, julgamentos de relevância e métricas como precisão, revocação, medida F e métricas para resultados ordenados. O texto ressalta que qualidade algorítmica e utilidade para o usuário não são equivalentes. Para aplicações de manutenção, isso implica avaliar não apenas acurácia global, mas também a recuperação de classes críticas, o custo de encaminhamentos incorretos e a capacidade de localizar registros semelhantes úteis à decisão.

Os capítulos 13 a 15 tratam diretamente da classificação textual supervisionada. São apresentados Naive Bayes multinomial e Bernoulli, seleção de atributos por informação mútua e qui-quadrado, classificadores baseados em vetores, Rocchio, k-vizinhos mais próximos e máquinas de vetores de suporte. A metodologia inclui separação entre treinamento e teste, avaliação por classe e discussão do compromisso entre viés e variância. Esses métodos constituem baselines adequados para comparar modelos mais recentes de PLN.

Os capítulos 16 a 18 abordam agrupamento plano e hierárquico, k-means, expectativa-maximização, rotulação de grupos, decomposição matricial e indexação semântica latente. No contexto do projeto, essas técnicas podem revelar temas emergentes, subdivisões de categorias, padrões de falha e grupos de chamados ainda não contemplados na taxonomia institucional.

## Estrutura e métodos abordados

- **Representação textual:** tokenização, normalização, stemming, lematização, vocabulário e índices posicionais.
- **Recuperação:** modelo booleano, índices invertidos, consultas por frase, correção ortográfica e expansão de consulta.
- **Ranqueamento:** TF-IDF, espaço vetorial, similaridade do cosseno, modelos probabilísticos, BM25 e modelos de linguagem.
- **Classificação:** Naive Bayes, Rocchio, k-NN, SVM, seleção de atributos e avaliação por classe.
- **Agrupamento:** k-means, expectativa-maximização, métodos hierárquicos e rotulação de clusters.
- **Avaliação:** precisão, revocação, medida F, avaliação de resultados ordenados, relevância e utilidade do usuário.

## Resultados aproveitáveis nos projetos

1. O texto oferece uma cadeia metodológica completa para classificação de chamados: delimitação do documento, limpeza, representação, treinamento, validação e análise de erros.
2. TF-IDF com classificadores lineares permanece um baseline necessário para avaliar se modelos mais complexos produzem ganho real.
3. A avaliação deve ser estratificada por categoria, pois a acurácia global pode ocultar desempenho insuficiente em classes raras ou críticas.
4. Campos do GLPI podem ser tratados como zonas com pesos diferentes, separando descrição, categoria, localização, solicitante e solução.
5. Correção ortográfica e k-gramas são úteis para lidar com abreviações e erros frequentes sem eliminar vocabulário técnico.
6. Agrupamento e indexação semântica podem apoiar revisão da taxonomia e descoberta de padrões antes da classificação supervisionada.

## Limitações e cuidados

- A obra antecede Transformers, embeddings contextuais e grandes modelos de linguagem; deve ser usada como fundamento e baseline, não como panorama do estado atual.
- A edição arquivada é uma versão on-line datada de 2009 e apresenta avisos editoriais de rascunho.
- Exemplos e coleções de teste são predominantemente em inglês; aplicações em português exigem validação de tokenização, normalização e morfologia.
- Métricas clássicas precisam ser complementadas por custo do erro, tempo operacional, calibração e desempenho por classe no uso institucional.
- A redução agressiva do vocabulário pode remover siglas, códigos, locais e nomes de equipamentos essenciais à manutenção.

## Aderência aos projetos

- **Classificação de chamados e PLN:** muito alta.
- **Malha IA e comparação de modelos:** muito alta como referência para baselines, avaliação e análise de erros.
- **Manutenção e governança:** alta na organização, recuperação e reutilização do histórico de ordens de serviço.
- **Previsão de custos:** indireta, por apoiar a estruturação das variáveis textuais que podem alimentar modelos preditivos.
- **ODS/ESG:** indireta, aplicável à classificação automática de documentos e evidências relacionadas aos ODS.

## Como citar em pesquisas do acervo

Use a obra para fundamentar pré-processamento textual, TF-IDF, espaço vetorial, classificação supervisionada, agrupamento e métricas de recuperação da informação. Para métodos contemporâneos, complemente-a com referências específicas de Transformers, BERT e modelos de linguagem.
