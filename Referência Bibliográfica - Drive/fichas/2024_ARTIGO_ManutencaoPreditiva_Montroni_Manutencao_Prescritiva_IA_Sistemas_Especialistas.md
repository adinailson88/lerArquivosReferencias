# Manutenção prescritiva: uso da inteligência artificial em sistemas especialistas

## Referência

MONTRONI, Carolina et al. **Manutenção prescritiva: uso da inteligência artificial em sistemas especialistas**. [S. l.: s. n.], [2024]. 11 p.

- **Arquivo no acervo:** `2024_ARTIGO_ManutencaoPreditiva_Montroni_Manutencao_Prescritiva_IA_Sistemas_Especialistas.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/16_ARpNT5IVTkeC-0NxeTu_swt6V7I6f4/view?usp=drivesdk)
- **Tipo:** artigo técnico/relato de implantação industrial.
- **Contexto:** Centro de Monitoramento de Ativos da Vale; Mine Asset Health e Assistente Cognitivo.
- **Conferência bibliográfica:** o PDF integral foi consultado, mas não apresenta veículo, evento, local, editora, DOI ou ano na página de rosto. O ano entre colchetes deriva do nome do arquivo e da data de criação do PDF; completar a referência antes de publicação formal.

## Síntese detalhada

O trabalho descreve duas soluções de IA integradas ao CMA Web da Vale para avançar da manutenção preditiva à prescritiva. O Centro de Monitoramento de Ativos centraliza inspeções preditivas, mecânicas e elétricas, permite análise e prognóstico e oferece informações para planejar intervenções. O CMA Global atua em riscos e capacidade no médio/longo prazo; o CMA Local concentra confiabilidade e decisões de curto prazo.

O Mine Asset Health (MAH) atende equipamentos de mina. A camada preditiva combina análise de óleo, alarmes de fabricante e tendências de telemetria para detectar anomalias; uma árvore de falhas transforma alertas em causas possíveis e recomendações. O modelo usa uma adaptação não supervisionada de KNN centrada em medianas e algoritmos disponíveis na biblioteca PyOD. Os alertas são priorizados para apoiar inspetores e a abertura ou confirmação de ordens de manutenção.

O MAH opera em minas do Pará e de Minas Gerais e cobre mais de 350 ativos, incluindo caminhões fora de estrada, perfuratrizes, tratores, escavadeiras e carregadeiras. O texto relata preservação de motores, transmissões e comandos finais, porém não apresenta quantidade de alertas, verdade-terreno, precisão, falso positivo, custo evitado ou comparação controlada.

O Assistente Cognitivo apoia usinas de pelotização. Uma API no Azure consulta o histórico do ativo e retorna as três prescrições passadas mais semelhantes, além de sugerir prazo. Redes neurais siamesas extraem representações e calculam similaridade entre alarmes atuais e registros históricos. A interface coleta feedback do inspetor para melhoria contínua.

Implantado em janeiro de 2023, o Assistente cobre mais de 6.500 componentes de transportadores de correia, moinhos e ventiladores em Vitória/Tubarão, São Luís e Vargem Grande. O artigo afirma que as sugestões são assertivas e úteis na maioria dos casos, mas não oferece métricas formais. A agenda inclui vibração, combustível, arrefecimento, modelos preditivos a partir de falhas/intervenções e IA generativa para padronizar prescrições, com validação técnica antes de incorporação ao histórico.

## Pipeline e campos reutilizáveis

- **Entradas MAH:** óleo, alarme OEM, telemetria, vibração, combustível e arrefecimento.
- **Detecção:** KNN não supervisionado/outlier detection e ranking por criticidade.
- **Prescrição:** árvore de falhas com causa provável e ação recomendada.
- **Assistente:** alarme consolidado, histórico por ativo, embedding siamês, top 3 similares e prazo.
- **Integração:** CMA Web, API Azure, ordem de manutenção e feedback humano.
- **Governança:** validação técnica antes de usar texto generativo na base histórica.

## Resultados aproveitáveis

1. O caso liga anomalia, explicação, prescrição, prazo, ordem e feedback em um único fluxo.
2. Comparação entre pares da mesma frota reduz dependência de rótulos, mas exige grupos realmente comparáveis.
3. Recuperar casos similares pode fundamentar recomendações em histórico auditável.
4. A padronização textual é problema de PLN com impacto direto na qualidade da base e das prescrições.
5. O feedback do especialista deve registrar aceitação, edição, rejeição e resultado da intervenção.
6. A validação humana antes de consolidar texto gerado é uma regra adequada para `malha-ia-regras-llm`.

## Citações verificadas

- “mais de 350 ativos de mineração” (p. 6).
- “as três prescrições passadas mais similares” (p. 8).
- “mais de 6.500 componentes” (p. 9).

## Limitações

- Relato corporativo sem conjunto de teste, baseline, métricas formais ou análise estatística.
- Não informa volume de dados, distribuição de falhas, parâmetros do KNN/rede siamesa ou processo de rotulagem.
- Benefícios de custo e confiabilidade são descritos, mas não quantificados.
- A afirmação de maior assertividade não pode ser avaliada de forma independente.
- Dados editoriais do documento estão incompletos; a referência deve ser confirmada antes de submissão.

## Aderência aos repositórios

- **Máxima:** `classificacao-chamados`, `malha-ia-regras-llm`, `malha-previsao-chamados`, `malha-ia`.
- **Muito alta:** `malha-previsao-filtros`, `malha-estatisticas-associadas`, `malha-previsao-custos`, `glpi-google-sheets-sync`.
- **Operação sustentável:** `malha-ods-esg`, `pls-ufsb-dashboard`.
- **Revisão:** `revisao-bibliografica`, `NOVA-revisao-bibliografica`, `lerArquivosReferencias`.

## Como citar com segurança

Use como estudo de arquitetura e implantação real, não como comprovação quantitativa de desempenho. Antes de submissão, complete o veículo e o evento da publicação e não atribua redução de custo ou acurácia que o artigo não mede.
