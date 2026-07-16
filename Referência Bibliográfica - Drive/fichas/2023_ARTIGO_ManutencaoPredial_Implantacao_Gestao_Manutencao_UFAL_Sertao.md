# Implantação da gestão de manutenção predial na UFAL — Campus Sertão

## Referência

SILVA, Marcus Paulo Bezerra; SILVA, Diniz Alves de Sant’Ana; NASCIMENTO, Tatiane Conceição do; VIEIRA, Victor Menezes. Implantação da gestão de manutenção predial na UFAL — Campus Sertão. *Revista Gestão e Planejamento*, Salvador, v. 24, p. 76-99, jan./dez. 2023. DOI: 10.53706/gep.v.23.6669.

- **Arquivo no acervo:** `2023_ARTIGO_ManutencaoPredial_Implantacao_Gestao_Manutencao_UFAL_Sertao.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1gHQGtRGwcp3NPwU9NGI_MVG2YdPEynpg/view?usp=drivesdk)
- **Tipo:** artigo; estudo de caso quantitativo e implantação piloto de CMMS.
- **Período empírico:** cadastros e ordens de serviço de 2018; artigo aceito em 2022 e publicado em 2023.

## Síntese detalhada

O estudo aplica o software SADEGE, PDCA e 5W2H à gestão de equipamentos do Campus Sertão da UFAL. O objetivo é estruturar cadastro, ordens, planejamento, mão de obra, materiais e indicadores para migrar de uma operação predominantemente corretiva para preventiva.

Foram cadastrados 107 equipamentos eletroeletrônicos e eletrodomésticos de maior uso em 14 categorias, distribuídos por anfiteatro, escritórios, centro acadêmico, centro técnico, laboratório e restaurante universitário. Itens sem consumo de energia ou de consumo muito baixo foram excluídos. A identificação recebeu padrão de tags por categoria para evitar duplicidade e permitir associação com fabricante, modelo, número de série e patrimônio.

O sistema registrou turnos, equipe, materiais, ferramentas, planos anual/mensal/semanal, ordens, horas trabalhadas, defeitos, disponibilidade, MTBF, MTTR e horas de máquina parada. Entre quatro atividades preventivas exemplificadas, três estavam vencidas. Em 100 equipamentos analisados, 82 apresentaram disponibilidade acima da meta institucional de 70%; vários permaneceram parados por mais de 60 dias.

Em uma amostra de 42 equipamentos com manutenção corretiva, 66,67% apresentaram disponibilidade inerente superior a 50%. Falha de instalação e peça defeituosa foram ocorrências frequentes; peça defeituosa gerou o maior tempo parado. Os autores propõem planos de limpeza, regulagem e inspeção e continuidade do ciclo PDCA.

## Estrutura de dados reutilizável

- Cadastro do ativo: tag, categoria, patrimônio, fabricante, modelo, série e localização.
- Eventos: defeito, abertura, início, término, parada e encerramento.
- Recursos: técnico, turno, hora normal/extra, material e ferramenta.
- Indicadores: MTBF, MTTR, disponibilidade, HMP, backlog e cumprimento do plano.
- Planejamento: tarefa, frequência, status, prioridade e 5W2H.

## Resultados aproveitáveis

1. É um caso brasileiro diretamente transferível para modelagem de dados de chamados em campus universitário.
2. Tag consistente é pré-condição para unir chamado, patrimônio, custo, falha e reincidência.
3. Horas paradas e defeitos devem ser analisados conjuntamente; frequência isolada não mede impacto.
4. Atividades vencidas permitem KPI de aderência ao plano preventivo.
5. A abertura digital expõe backlog antes invisível, exigindo cuidado ao comparar períodos pré e pós-implantação.

## Citações verificadas

- “foram encontrados 107 equipamentos” (p. 84).
- “82 [...] apresentaram um percentual de disponibilidade acima de setenta por cento” (p. 92).
- “42 [...] equipamentos que passaram por manutenção corretiva” (p. 93).

## Limitações

- Caso único e conjunto restrito a equipamentos elétricos/de apoio, não toda a edificação.
- Não há grupo de controle, baseline formal ou teste de significância.
- Parte dos resultados é demonstração funcional do software, não efeito comprovado da implantação.
- As metas de 70% e 50% precisam de justificativa técnica por classe de ativo.
- O artigo afirma redução de custos, mas não apresenta série monetária que permita quantificá-la.

## Aderência aos repositórios

- **Máxima:** `glpi-google-sheets-sync`, `classificacao-chamados`, `malha-previsao-chamados`, `malha-estatisticas-associadas`, `pls-ufsb-dashboard`.
- **Muito alta:** `malha-ia`, `malha-previsao-custos`, `malha-previsao-filtros`, `malha-ia-regras-llm`.
- **Complementar:** `malha-ods-esg`, `revisao-bibliografica`, `NOVA-revisao-bibliografica`.

## Como citar com segurança

Use os números como descrição do piloto de 2018. Não trate disponibilidade ou redução de paradas como efeito causal do SADEGE sem comparação longitudinal controlada.
