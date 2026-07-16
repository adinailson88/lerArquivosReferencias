# Empirical quantification and prediction of building component lifespans with graph neural networks

## Referência

WU, Pei-Yu; MUNDT-PETERSEN, S. O. Empirical quantification and prediction of building component lifespans with graph neural networks. **IOP Conference Series: Earth and Environmental Science**, v. 1554, 012036, 2025. DOI: 10.1088/1755-1315/1554/1/012036.

- **Arquivo no acervo:** `2025_ARTIGO_ManutencaoPreditiva_Wu_GNN_Lifespan_Building_Components.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1N95fm-wj6gbRsQwOHwq0Y3S0gp9Xh21k/view?usp=drivesdk)
- **Tipo:** artigo em anais da Sustainable Built Environment Conference 2025 Zurich; modelagem empírica com GNN.

## Síntese detalhada

O artigo estima a idade até a identificação de danos em componentes prediais suecos e testa redes neurais em grafos para regressão. A origem é um conjunto de 2.100 registros de danos por umidade, provenientes de 428 investigações/inventários realizados por inspetores acreditados entre 2014 e 2021 no centro e sul da Suécia. A amostra inclui escolas (44%), multifamiliares (24%), unifamiliares (19%) e outros não residenciais (14%).

São descritos dez tipos de dano e doze grupos de componentes. Para garantir volume, os componentes foram reunidos em seis classes: paredes (N=763), pisos/vigas (465), ambiente/interior (271), coberturas (204), portas/janelas (82) e fundação/estrutura (57). Observações menores que cinco ou maiores que 95 anos foram excluídas. Materiais, dano, clima, tipologia, propriedade e detalhes construtivos formam nós e relações em um grafo acíclico dirigido definido com conhecimento de especialistas.

GCN, GraphSAGE e GAT foram implementadas em PyTorch Geometric com 12 atributos, embeddings categóricos, uma ou duas camadas, Adam, ReLU e saída normalizada para até 100 anos. A divisão declarada é 70% treino, 15% validação e 15% teste. A GCN obteve R² 0,83, GraphSAGE 0,73 e GAT 0,35. Componentes residenciais danificados apresentaram em geral cerca de 25–30 anos, enquanto materiais e tipos de dano explicaram variações importantes.

O alvo não é a vida útil completa: é o intervalo entre construção e identificação do dano. A base contém apenas 2% de edifícios não danificados, produzindo forte viés de seleção. Danos podem existir antes de serem observados. Além disso, o texto alterna 2.100 registros, 1.842 observações nas seis classes e “1.500 nós/edifícios” sem reconciliar claramente as exclusões.

## Pipeline reutilizável

- **Alvo:** idade na detecção do dano, distinguida de vida útil real/remanescente.
- **Entradas:** componente, material, dano, clima, tipologia, propriedade e detalhe construtivo.
- **Grafo:** relações causais/associativas definidas por especialistas.
- **Modelos:** GCN, GraphSAGE e GAT; comparação com mesmos hiperparâmetros principais.
- **Métricas a acrescentar:** MAE/RMSE em anos, teste independente, calibração e intervalos preditivos.
- **Validação recomendada:** separação por edifício e por tempo, evitando registros do mesmo prédio em conjuntos diferentes.

## Citações verificadas

- “2,100 complex moisture damage records from 428” investigações (p. 4).
- “70% training, 15% validation, and 15% testing” (p. 6).
- “GCN achieves the highest R² score (0.83)” (p. 7).

## Limitações e alerta de modelagem

- Forte viés para componentes já danificados; apenas 2% sem dano.
- Idade na inspeção/detecção não equivale a vida útil ou tempo até falha.
- Contagens 2.100/1.842/1.500 não são plenamente reconciliadas.
- Não fica claro se a divisão impede vazamento entre registros do mesmo edifício ou no grafo transdutivo.
- R² é apresentado sem MAE/RMSE e sem resultado separado claramente para o conjunto de teste.
- O DAG combina relações causais, associativas e atributivas definidas por especialistas, sem análise de sensibilidade.

## Aderência aos repositórios

- **Máxima:** `malha-ia`, `malha-previsao-chamados`, `malha-estatisticas-associadas`, `malha-previsao-custos`.
- **Muito alta:** `malha-previsao-filtros`, `malha-ia-regras-llm`, `classificacao-chamados`.
- **Ciclo de vida:** `malha-ods-esg`, `pls-ufsb-dashboard`.
- **Revisão:** `revisao-bibliografica`, `NOVA-revisao-bibliografica`, `lerArquivosReferencias`.

## Como citar com segurança

Cite R² e idades como resultados da base sueca de componentes danificados. Não os interprete como vida útil universal; antes de reproduzir, esclareça unidade de divisão, contagens finais, conjunto de teste e prevenção de vazamento.
