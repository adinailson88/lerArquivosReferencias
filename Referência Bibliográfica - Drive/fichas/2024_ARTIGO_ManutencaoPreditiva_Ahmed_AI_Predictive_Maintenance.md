# AI-Driven Predictive Maintenance for Energy Infrastructure

## Referência

AHMED, Ibrahim Adeiza; ASAMOAH, Paul Boadu. AI-Driven Predictive Maintenance for Energy Infrastructure. **International Journal of Research and Scientific Innovation**, v. 11, n. 9, p. 507–528, set. 2024. DOI: 10.51244/IJRSI.2024.1109048.

- **Arquivo no acervo:** `2024_ARTIGO_ManutencaoPreditiva_Ahmed_AI_Predictive_Maintenance.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1qYMu-WwVGw83Um1ygy06Mbt0f7xT8x71/view?usp=drivesdk)
- **Tipo:** artigo; apresentação de modelos e estudos de caso em infraestrutura energética.
- **Conferência:** texto integral consultado, com 22 páginas no PDF.
- **Status de uso:** **usar com cautela; baixa reprodutibilidade dos resultados numéricos**.

## Síntese detalhada

O artigo discute manutenção preditiva orientada por IA em infraestrutura de energia e apresenta Random Forest, SVM, CNN e RNN como alternativas para analisar histórico de manutenção e sinais de sensores. O texto associa essas abordagens à antecipação de falhas, redução de paradas e melhor alocação de recursos em energia eólica, solar e térmica.

São reportadas acurácias de 92% para Random Forest, 89% para SVM, 94% para CNN e 95% para RNN. Também aparecem precisão e revocação de 93% e 91% para CNN, F1 de 93% para RNN e MAE entre 0,03 e 0,07. Nos estudos de caso, o texto afirma redução de 20% no custo e aumento de 15% na disponibilidade em energia eólica; aumento de 10% na produção e redução de 25% no custo em solar; e redução de 30% no tempo de inatividade e aumento de 20% na eficiência em usina térmica.

Entretanto, o artigo não informa tamanho ou origem dos conjuntos de dados, quantidade de equipamentos e falhas, divisão treino/teste, definição das variáveis e do alvo, hiperparâmetros, procedimento de validação, intervalos de incerteza ou matrizes de confusão. Também não identifica de maneira suficiente as organizações e amostras dos casos. Parte dos percentuais é seguida por referências gerais da literatura, sem separação clara entre resultado empírico dos autores e síntese de trabalhos anteriores.

Por isso, a principal utilidade da referência é conceitual: levantar famílias de modelos, tipos de dados, métricas e riscos de implantação. Os números não devem ser usados como benchmark, prova de superioridade ou estimativa de retorno sem confirmação independente.

## Estrutura reutilizável

- **Fontes possíveis:** vibração, temperatura, pressão, corrente, ruído, histórico de falhas e ordens.
- **Modelos candidatos:** Random Forest e SVM como baselines; CNN/RNN para sinais e sequências.
- **Métricas necessárias:** precisão, revocação, F1, MAE, antecedência do alerta, falso alarme, downtime e custo evitado.
- **Casos de uso:** turbinas eólicas, painéis solares e geração térmica.
- **Requisitos de governança:** qualidade, disponibilidade, segurança e integração de dados.

## Resultados aproveitáveis

1. A comparação entre modelos deve usar a mesma divisão temporal e métricas sensíveis ao desbalanceamento.
2. Dados de sensores precisam ser ligados a ativo, tempo, falha confirmada, intervenção e custo.
3. Benefício operacional deve ser avaliado separadamente da métrica preditiva.
4. Qualidade e disponibilidade dos dados são dependências centrais da manutenção preditiva.
5. Estudos futuros devem medir desempenho no longo prazo e deriva de sensores e equipamentos.

## Citações verificadas

- “The random forest model achieved an accuracy of 92%” (p. 523).
- “reliance on the quality and availability of data” (p. 526).
- “Long-Term Performance [...] was not extensively examined” (p. 526).

## Alerta de qualidade metodológica

As métricas não são reprodutíveis a partir do artigo. Faltam amostra, fonte, distribuição de classes, protocolo experimental, configurações, código e resultados desagregados. Trate as porcentagens como afirmações do texto, não como evidência validada. Antes de citá-las, procure a base primária ou outra publicação com protocolo verificável.

## Aderência aos repositórios

- **Conceitual, com cautela:** `malha-ia`, `malha-previsao-chamados`, `malha-previsao-custos`, `classificacao-chamados`.
- **Regras e avaliação:** `malha-ia-regras-llm`, `malha-previsao-filtros`, `malha-estatisticas-associadas`.
- **Energia e sustentabilidade:** `malha-ods-esg`, `pls-ufsb-dashboard`.
- **Revisão crítica:** `revisao-bibliografica`, `NOVA-revisao-bibliografica`, `lerArquivosReferencias`.

## Como citar com segurança

Cite para contextualizar aplicações, modelos e desafios de dados. Não use as métricas do artigo como benchmark nem como estimativa de ganhos econômicos sem localizar evidência primária independente.
