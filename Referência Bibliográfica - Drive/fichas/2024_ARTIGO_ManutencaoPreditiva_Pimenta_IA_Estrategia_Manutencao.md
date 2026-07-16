# Aplicação de soluções de inteligência artificial para análise e melhoria da estratégia de manutenção

## Referência

PIMENTA, Douglas et al. **Aplicação de soluções de inteligência artificial para análise e melhoria da estratégia de manutenção**. [S. l.: s. n.], [2024]. 11 p.

- **Arquivo no acervo:** `2024_ARTIGO_ManutencaoPreditiva_Pimenta_IA_Estrategia_Manutencao.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/16ZfSfkgVOjtYGmnPietY076VW-G7IwQ-/view?usp=drivesdk)
- **Tipo:** artigo técnico/relato de implantação industrial na Vale.
- **Conferência bibliográfica:** veículo, evento, editora, DOI e ano não constam no PDF; completar antes de submissão.

## Síntese detalhada

O texto descreve a solução CEOS, criada para avaliar e melhorar cadastros e estratégias de manutenção da Vale em grande escala. A base abrange mais de 547 mil planos, 565 mil listas de tarefa e 310 mil ordens mensais; a ferramenta atende mais de 2.000 usuários de Engenharia e Planejamento e Controle da Manutenção.

A arquitetura extrai dados do SAP via SAP/HANA, analisa-os no ecossistema Microsoft Azure e entrega painéis no Power BI. O processo é dividido em captura, avaliação, caracterização e comunicação. O primeiro MVP avaliou 17 parâmetros do cadastro das listas de tarefa; fases seguintes comparam listas e ordens, verificam mão de obra, materiais, custo, ciclo de consumo e qualidade da execução.

O trabalho diferencia avaliação objetiva — regras explícitas, preenchimento e consistência entre campos — de avaliação subjetiva, na qual aprendizado de máquina busca similaridades e recorrências entre planejamento e execução considerando localidade, ativo, sazonalidade e ambiente. Os painéis são atualizados semanalmente e oferecem sugestões de correção baseadas no histórico.

Como resultados, os autores relatam redução de 30 para 1 minuto na identificação de problemas por lista, menor retrabalho, melhor visibilidade e apoio à decisão. O IQPL consolida a qualidade dos planos. Contudo, valores e imagens não correspondem aos números reais da empresa; não há protocolo de medição, amostra de usuários, distribuição do índice, comparação estatística ou impacto demonstrado sobre falhas dos ativos.

## Pipeline reutilizável

- **Fontes:** plano, lista de tarefa, ordem, mão de obra, material, custo e execução.
- **Qualidade:** completude, consistência, conformidade, repetibilidade e aderência ao padrão.
- **Regras:** validação de campo e dependências entre atributos.
- **ML:** similaridade entre planejamento e execução e detecção de recorrência.
- **Entrega:** ranking, volumetria × qualidade, sugestão de ajuste e workflow.
- **Governança:** padrão normativo, IQPL, atualização semanal e gestão da mudança.

## Citações verificadas

- “mais de 547 mil planos de manutenção” (p. 1).
- “mais de 2.000 usuários diretos” (p. 1).
- “Redução de 30 para 1 minuto” (p. 8).

## Limitações

- Relato corporativo sem desenho experimental, baseline formal ou métricas dos modelos.
- Dados, figuras e valores são didáticos/mascarados, limitando reprodução.
- Não especifica algoritmos, hiperparâmetros, treinamento ou validação do ML.
- O ganho de tempo não é acompanhado de amostra, variabilidade ou auditoria independente.
- Referência editorial incompleta no PDF.

## Aderência aos repositórios

- **Máxima:** `malha-ia-regras-llm`, `classificacao-chamados`, `malha-previsao-filtros`, `malha-ia`.
- **Muito alta:** `malha-previsao-chamados`, `malha-previsao-custos`, `malha-estatisticas-associadas`, `glpi-google-sheets-sync`.
- **Governança:** `pls-ufsb-dashboard`, `malha-ods-esg`.
- **Revisão:** `revisao-bibliografica`, `NOVA-revisao-bibliografica`, `lerArquivosReferencias`.

## Como citar com segurança

Use como caso de arquitetura, escala e governança de qualidade de dados. Não apresente eficácia do ML ou impacto sobre confiabilidade como validados; complete os dados editoriais e preserve a ressalva sobre valores didáticos.
