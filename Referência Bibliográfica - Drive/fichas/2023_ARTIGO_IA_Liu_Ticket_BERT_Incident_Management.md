# Ticket-BERT: Labeling Incident Management Tickets with Language Models

## Referência

LIU, Zhexiong; BENGE, Cris; JIANG, Siduo. Ticket-BERT: Labeling Incident Management Tickets with Language Models. arXiv:2307.00108, 2023.

- **Arquivo no acervo:** `2023_ARTIGO_IA_Liu_Ticket_BERT_Incident_Management.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1QKHHadItDuoQmnAmTCcMIz7VsYgRsZla/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; arXiv:2307.00108

## Síntese detalhada

O trabalho cria três conjuntos derivados de 76 mil tickets do Microsoft Azure — humanos, gerados por máquinas e mistos — com dez rótulos finos. O Ticket-BERT supera Naive Bayes, regressão logística e serviços de classificação avaliados, com F1 próximo ou superior a 98% nos cenários apresentados, e é integrado a um ciclo de aprendizado ativo no sistema de gestão de incidentes da Microsoft.

## Método e escopo

Fine-tuning de modelo de linguagem com diferentes composições de texto do ticket e comparação com baselines BoW/TF-IDF. O desenho considera atualizações durante o ciclo de vida do incidente e mecanismo de reaprendizado com poucas novas anotações.

## Resultados e contribuição

O estudo demonstra alto desempenho em um domínio empresarial bem delimitado e destaca deriva de rótulos, atualizações frequentes e diferenças entre texto humano e automático. O próprio artigo informa que o modelo não se generaliza a todos os tickets do sistema IcM.

## Contribuições reutilizáveis

- Referência para BERT especializado em tickets e aprendizado ativo.
- Estrutura para separar fontes humanas, automáticas e mistas.
- Alerta para deriva temporal e inclusão de novos rótulos.

## Limitações e cuidados

- Dados proprietários e domínio específico de hardware Azure.
- Desempenho muito alto pode refletir taxonomia e padrões internos.
- Generalização para chamados prediais em português não foi testada.

## Aderência ao projeto

- **Classificação:** Muito alta — classificação e atualização contínua de tickets
- **Palavras-chave:** BERT; tickets; gestão de incidentes; classificação; active learning; Microsoft Azure
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Cite para justificar modelos de linguagem adaptados ao domínio e atualização contínua. Não use o F1 publicado como expectativa para a UFSB sem réplica em teste temporal externo.
