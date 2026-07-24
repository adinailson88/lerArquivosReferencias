# A Noise Audit of Human-Labeled Benchmarks for Machine Commonsense Reasoning

## Referência

KEJRIWAL, Mayank et al. A noise audit of human-labeled benchmarks for machine commonsense reasoning. *Scientific Reports*, v. 14, art. 8609, 2024. DOI: 10.1038/s41598-024-58937-4.

- **Arquivo no acervo:** `2024_ARTIGO_IA_Kejriwal_Noise_Audit_Human_Labeled_Benchmarks.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1ZzXWDdlJDqHVvCmCJZPUhwsImvn0iVeB/view)
- **Pasta temática:** `02_IA_e_CienciaDeDados`
- **Tipo:** ARTIGO
- **Conferência:** Leitura integral; DOI 10.1038/s41598-024-58937-4

## Síntese detalhada

O artigo audita ruído em benchmarks de raciocínio de senso comum sob uma configuração de rotulagem menor e mais controlada e outra de crowdsourcing em maior escala. Identifica ruído de nível, padrão e sistema mesmo no cenário de maior qualidade. A variação dos anotadores altera estimativas de desempenho humano em quase 10 pontos percentuais em alguns casos e de sistemas como ChatGPT em mais de 4 pontos.

## Método e escopo

Auditoria baseada no enquadramento de ruído de Kahneman, matrizes anotador–item, diferentes definições de ground truth e intervalos de confiança. O estudo avalia tanto a discordância quanto seu impacto na comparação entre sistemas.

## Resultados e contribuição

A contribuição é mostrar que um rótulo único não deve ser presumido como verdade indiscutível em tarefas com julgamento humano. Diferenças modestas entre modelos podem ser compatíveis com a variabilidade da anotação.

## Contribuições reutilizáveis

- Fundamenta dupla rotulagem, adjudicação e amostras de auditoria.
- Justifica registrar discordância e incerteza de rótulo.
- Ajuda a interpretar diferenças pequenas entre classificadores.

## Limitações e cuidados

- Domínio de raciocínio de senso comum, não manutenção.
- A decomposição de ruído depende do desenho de anotação.
- Não fornece diretamente um procedimento de correção para rótulos institucionais.

## Aderência ao projeto

- **Classificação:** Muito alta — auditoria de qualidade dos rótulos
- **Palavras-chave:** ruído de rótulos; auditoria; benchmarks; anotação humana; ground truth; ChatGPT
- **Aplicação principal:** suporte aos repositórios `classificacao-chamados`, `malha-ia`, `NOVA-revisao-bibliografica` e ao desenvolvimento da tese, conforme a pertinência temática.

## Como citar com segurança

Cite para discutir incerteza da anotação e limites do ground truth único. Não transfira os percentuais de ruído para o corpus de chamados sem auditoria própria.
