# Innovative Approach to Preventive Maintenance of Production Equipment Based on a Modified TPM Methodology for Industry 4.0

## Referência

HARDT, Filip; KOTYRBA, Martin; VOLNA, Eva; JARUSEK, Robert. Innovative approach to preventive maintenance of production equipment based on a modified TPM methodology for Industry 4.0. *Applied Sciences*, v. 11, n. 15, art. 6953, 2021. DOI: 10.3390/app11156953.

- **Arquivo no acervo:** `2021_ARTIGO_TPM_Hardt_TPM_Industry_4_0.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1E0NxQ6VTYACrHwrPDl8a25_39umJt1W9/view?usp=drivesdk)
- **Tipo:** artigo; desenvolvimento e implantação de metodologia em ambiente industrial.
- **Conferência:** texto integral de 17 páginas consultado.

## Síntese detalhada

O artigo modifica a Total Productive Maintenance para integrar planejamento, execução, registro e avaliação de manutenção preventiva em ambiente de Indústria 4.0. A solução foi implementada na fábrica da ITT em Ostrava, República Tcheca, dedicada à produção de pastilhas de freio.

A proposta organiza a manutenção em blocos, frequências, achados e responsabilidades. Operadores registram verificações e anomalias em painéis; os registros recebem identificador único e permanecem rastreáveis. Gestores planejam intervenções a partir da base de achados, alocam equipe e acompanham execução. O sistema Mpoint funciona como CMMIS/data warehouse e conecta dados de usuários, equipamentos e manutenção.

Na época do estudo, o sistema estava implantado em toda a planta e tinha mais de 200 usuários. O desempenho preventivo era calculado como proporção entre verificações executadas e previstas, classificada em faixas: acima de 75%, entre 50% e 75% e abaixo de 50%. Após a implantação houve aumento inicial de anomalias registradas — interpretado como melhora de captura, não piora real — e depois redução de pendências com a execução do bloco de manutenção autônoma.

O artigo apresenta indicadores mensais, por exemplo desempenho de 42%, 37%, 88%, 64% e 75% entre julho e novembro de 2020. A evidência apoia a viabilidade do processo informatizado, mas não isola causalmente a intervenção nem apresenta comparação estatística controlada.

## Arquitetura de informação reutilizável

- Equipamento e componente com identificador único.
- Plano, frequência e checklist de manutenção preventiva.
- Achado/anomalia, origem, gravidade, data e responsável.
- Conversão do achado em ação, alocação de equipe e encerramento.
- Histórico rastreável em data warehouse.
- KPI de execução preventiva e painéis por área/equipamento.
- Retroalimentação para planejamento e priorização.

## Resultados aproveitáveis

1. O aumento de chamados após implantação pode indicar melhor detecção e adesão, não deterioração do ativo.
2. KPIs devem diferenciar demanda identificada, pendência e serviço executado.
3. Identificadores únicos e histórico de alterações são requisitos para auditoria e aprendizado de máquina.
4. A combinação de checklist, sensores, registros humanos e data warehouse aproxima manutenção preventiva e preditiva.
5. A adoção depende de treinamento, mudança cultural e participação dos operadores.

## Citações verificadas

- “more than 200 users work with it” (p. 14).
- “an enormous increase in abnormalities was seen” (p. 14).
- “the number of abnormalities has decreased significantly” (p. 16).

## Limitações

- Ambiente industrial de produção, não manutenção predial pública.
- Resultados apresentados de forma descritiva, sem grupo de controle ou teste de significância.
- Mudanças simultâneas no processo e no sistema dificultam atribuição causal.
- A classificação por faixas de execução é operacional e não mede diretamente confiabilidade, custo ou qualidade do reparo.

## Aderência aos repositórios

- **Máxima:** `malha-ia`, `malha-previsao-chamados`, `malha-estatisticas-associadas`, `glpi-google-sheets-sync`.
- **Alta:** `classificacao-chamados`, `malha-previsao-filtros`, `malha-previsao-custos`, `malha-ia-regras-llm`, `pls-ufsb-dashboard`.
- **Complementar:** `malha-ods-esg`, `revisao-bibliografica`, `NOVA-revisao-bibliografica`.

## Como citar com segurança

Use o estudo como referência de processo digital e adoção de TPM, deixando explícito que a aplicação foi industrial. Não generalize os percentuais mensais como ganho causal ou desempenho esperado em manutenção predial.
