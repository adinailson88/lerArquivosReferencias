# Natural Language Processing Model for Managing Maintenance Requests in Buildings

## Referência

BOUABDALLAOUI, Yassine et al. Natural Language Processing Model for Managing Maintenance Requests in Buildings. *Buildings*, v. 10, n. 9, art. 160, 2020. DOI: 10.3390/buildings10090160.

- **Arquivo no acervo:** `2020_ARTIGO_IA_Bouabdallaoui_NLP_Maintenance_Requests_Buildings.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1lqdAguuG92bOERm5_PSlCdBsLMIE36dv/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; DOI 10.3390/buildings10090160

## Síntese detalhada

O estudo propõe classificar automaticamente solicitações de manutenção predial registradas em texto livre. Utiliza dez anos de registros de uma unidade de saúde, com menos de 30 mil ordens, e compara CNN, CNN com múltiplos filtros, LSTM e uma combinação CNN–LSTM. A CNN com múltiplos filtros alcançou a melhor acurácia média, 78%; as classes de iluminação e instalações hidrossanitárias superaram 90%, enquanto categorias semanticamente próximas apresentaram desempenho inferior a 60%.

## Método e escopo

Estudo aplicado com pré-processamento de descrições, representação vetorial e comparação de quatro arquiteturas neurais multiclasse. A avaliação usa acurácia e matriz de confusão; o próprio artigo reconhece que a métrica pode ocultar diferenças entre classes, embora caracterize o conjunto como não desbalanceado.

## Resultados e contribuição

A sequência das palavras agregou menos que a presença de termos discriminantes, razão apresentada para o baixo ganho dos modelos com LSTM. O artigo evidencia que descrições curtas e ruidosas de manutenção podem ser tratadas por PLN, mas também mostra erros por sobreposição semântica e rotulagem inconsistente.

## Contribuições reutilizáveis

- Referência diretamente aplicável à classificação de chamados e ordens de serviço.
- Base para comparar modelos simples e redes profundas sob a mesma divisão de dados.
- Exemplo de análise por classe, indispensável quando a acurácia global mascara categorias frágeis.

## Limitações e cuidados

- Caso único em unidade de saúde e taxonomia institucional própria.
- Amostra inferior a 30 mil registros e possíveis rótulos inconsistentes.
- Não apresenta validação externa nem comparação com baselines lineares fortes, como TF-IDF com SVM.

## Aderência ao projeto

- **Classificação:** Muito alta — classificação automática de chamados de manutenção
- **Palavras-chave:** manutenção predial; facility management; PLN; classificação textual; CNN; LSTM; ordens de serviço
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Use como evidência empírica de viabilidade do PLN em solicitações de manutenção e para discutir erros por classe. Não transfira a acurácia de 78% para outra instituição sem reproduzir a taxonomia, a divisão dos dados e o protocolo experimental.
