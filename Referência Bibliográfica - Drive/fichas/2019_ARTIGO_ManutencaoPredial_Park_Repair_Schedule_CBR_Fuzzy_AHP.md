# Forecasting Repair Schedule for Building Components Based on Case-Based Reasoning and Fuzzy-AHP

## Referência

PARK, Sojin; KWON, Nahyun; AHN, Yonghan. Forecasting repair schedule for building components based on case-based reasoning and fuzzy-AHP. *Sustainability*, v. 11, n. 24, art. 7181, 2019. DOI: 10.3390/su11247181.

- **Arquivo no acervo:** `2019_ARTIGO_ManutencaoPredial_Park_Repair_Schedule_CBR_Fuzzy_AHP.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1KBbfUCMYF8ZPdhpC12kMVmhbyp3xDPd0/view?usp=drivesdk)
- **Tipo:** artigo; modelagem preditiva com raciocínio baseado em casos, fuzzy-AHP e k-vizinhos mais próximos.
- **Conferência:** texto integral de 17 páginas consultado.

## Síntese detalhada

O artigo estima o intervalo entre a conclusão de um edifício residencial e o primeiro reparo de seus componentes. A motivação é substituir ciclos genéricos de manutenção por previsões baseadas em casos históricos e atributos do edifício, inclusive quando ainda há pouca informação sobre o novo empreendimento.

Os autores reuniram 712 registros da Korea Land and Housing Corporation relativos a 22 componentes. Após remover valores ausentes ou inadequados, conservaram 257 casos. O modelo utiliza nove entradas: taxa de ocupação, coeficiente de aproveitamento, número de edifícios, pavimentos e unidades, área administrada, ano de conclusão, custo de manutenção por área e quantidade de manutenções. O tempo até o primeiro reparo é a variável de saída.

Dez atributos foram definidos após revisão e entrevistas com profissionais de custos, construção, meio ambiente e manutenção. Os pesos foram obtidos por fuzzy-AHP: 42 de 70 questionários retornaram e 30 passaram pelo critério de consistência. Quantidade de manutenções (0,1895), custo por área (0,1567) e número de unidades (0,0910) foram as variáveis mais influentes.

A similaridade foi calculada por distância euclidiana ponderada. Vinte casos foram separados aleatoriamente para teste e comparados com 3, 5, 7 e 10 vizinhos. As similaridades médias foram 98,05%, 97,86%, 97,73% e 97,59%; os MAPEs médios, 8,07%, 9,21%, 9,64% e 9,51%. Apesar do bom resultado médio, alguns casos tiveram erro superior a 20%, mostrando sensibilidade à composição da base e aos resultados dos vizinhos recuperados.

## Método e dados reutilizáveis

- **Pipeline:** limpeza, normalização, seleção e ponderação de atributos, recuperação de casos, previsão e validação.
- **Algoritmos:** CBR, fuzzy-AHP, distância euclidiana ponderada, k-NN e leave-one-out cross-validation.
- **Alvo:** anos até o primeiro reparo.
- **Preditores:** cinco características físicas e quatro atributos de manutenção.
- **Validação:** 20 casos; comparação de k = 3, 5, 7 e 10 por similaridade e MAPE.
- **Extensão:** distribuição beta-PERT e simulação de Monte Carlo são usadas para representar incerteza em exemplos selecionados.

## Resultados aproveitáveis

1. Um chamado histórico pode ser representado como caso e recuperado por similaridade, abordagem diretamente transferível à previsão de manutenção.
2. Pesos multicritério permitem combinar variáveis físicas, custos e histórico sem presumir importância igual.
3. A qualidade e a cobertura da base são determinantes; similaridade alta não garante erro baixo.
4. As variáveis de manutenção receberam peso agregado maior que as características físicas, reforçando o valor de registros operacionais consistentes.
5. O modelo prevê o primeiro reparo, não reincidência, custo total ou risco de falha.

## Citações verificadas

- “database was established by collecting 257 cases” (p. 1).
- “the number of maintenances (0.1895)” (p. 9).
- “overall average error rate was 9.11%” (p. 12).

## Limitações

- Base de apartamentos sul-coreanos; a transferência para campi universitários exige recalibração.
- Exclusão de registros incompletos reduziu 712 observações a 257 e pode introduzir viés de seleção.
- Apenas 20 casos foram usados no teste apresentado.
- O artigo não compara o CBR com regressão, árvores, ensembles ou redes neurais.
- O resultado depende da qualidade dos atributos, dos pesos fuzzy-AHP e da disponibilidade de casos semelhantes.

## Aderência aos repositórios

- **Máxima:** `malha-previsao-chamados`, `malha-previsao-custos`, `malha-estatisticas-associadas`, `malha-ia`.
- **Alta:** `malha-previsao-filtros`, `classificacao-chamados`, `malha-ia-regras-llm`, `pls-ufsb-dashboard`.
- **Complementar:** `malha-ods-esg`, `revisao-bibliografica`, `NOVA-revisao-bibliografica`.

## Como citar com segurança

Use a referência publicada e o DOI. Ao transportar os números para outro domínio, descreva explicitamente que se referem a apartamentos da Coreia do Sul e não apresente o MAPE como desempenho esperado para dados brasileiros sem validação externa.
