# Attention Is All You Need

## Referência

VASWANI, Ashish et al. Attention Is All You Need. In: *Advances in Neural Information Processing Systems 30*. Long Beach: NIPS, 2017.

- **Arquivo no acervo:** `2017_ARTIGO_IA_Vaswani_Attention_Transformer.pdf`
- **Texto completo:** [Google Drive](https://drive.google.com/file/d/1RojBXyLt9ffVtgUW_B_Exh3QKRGWK5xQ/view?usp=drivesdk)
- **Tipo:** artigo de arquitetura de redes neurais; modelagem de sequências e tradução automática.
- **Conferência desta ficha:** PDF integral legível; arquitetura, dados de treinamento, hiperparâmetros, resultados e conclusão conferidos no texto.

## Síntese detalhada

O artigo introduz o Transformer, arquitetura de transdução de sequências baseada exclusivamente em mecanismos de atenção. O modelo elimina recorrência e convoluções do núcleo encoder-decoder e usa autoatenção para relacionar diretamente posições distintas da sequência. A proposta busca reduzir a dependência de operações sequenciais, ampliar o paralelismo do treinamento e encurtar o caminho computacional entre dependências distantes.

A arquitetura mantém a organização encoder-decoder. O encoder-base possui seis camadas idênticas, cada uma formada por autoatenção multi-head e uma rede feed-forward aplicada posição a posição. O decoder também possui seis camadas e acrescenta atenção sobre as saídas do encoder, além de mascaramento na autoatenção para impedir acesso a tokens futuros. Conexões residuais e normalização de camada envolvem cada subcamada.

Na atenção por produto escalar escalonado, consultas e chaves são combinadas por produto interno, divididas pela raiz quadrada da dimensão das chaves e convertidas em pesos por softmax. O fator de escala reduz efeitos de produtos internos muito elevados. Na configuração-base, a atenção multi-head utiliza oito cabeças paralelas, com dimensão 64 para chaves e valores, em um espaço de representação de dimensão 512. As saídas das cabeças são concatenadas e projetadas novamente.

O modelo-base utiliza dimensão de representação igual a 512 e camada feed-forward interna de dimensão 2.048. Como não há recorrência nem convolução, a ordem dos tokens é incorporada por codificações posicionais senoidais somadas aos embeddings. O artigo também testou embeddings posicionais aprendidos e encontrou resultado praticamente equivalente na tarefa avaliada.

A comparação teórica mostra que a autoatenção conecta todas as posições com número constante de operações sequenciais, enquanto redes recorrentes exigem uma cadeia proporcional ao comprimento da sequência. Para sequências de comprimento menor que a dimensão de representação, a autoatenção também pode ter menor custo por camada. A desvantagem é o custo quadrático em relação ao comprimento da sequência, aspecto relevante para documentos extensos.

Os experimentos utilizaram o WMT 2014 inglês-alemão, com aproximadamente 4,5 milhões de pares de sentenças e vocabulário compartilhado de cerca de 37 mil tokens por byte-pair encoding. Para inglês-francês, foram usados 36 milhões de pares e vocabulário de 32 mil unidades word-piece. O treinamento ocorreu em uma máquina com oito GPUs NVIDIA P100.

O modelo-base foi treinado por 100 mil passos, aproximadamente 12 horas, com cerca de 0,4 segundo por passo. O modelo grande foi treinado por 300 mil passos, aproximadamente 3,5 dias. O otimizador foi Adam, com β1 igual a 0,9, β2 igual a 0,98, aquecimento por 4 mil passos e posterior decaimento proporcional ao inverso da raiz do passo. Foram empregados dropout, label smoothing e compartilhamento de pesos entre embeddings e transformação anterior ao softmax.

Na tradução inglês-alemão, o Transformer grande alcançou 28,4 BLEU e superou em mais de dois pontos os melhores resultados anteriores reportados, inclusive ensembles. Na tarefa inglês-francês, alcançou 41,0 BLEU como modelo único, com custo de treinamento inferior ao de alternativas comparadas. O estudo de ablação mostrou perda de qualidade com uma única cabeça, benefício de modelos maiores e importância do dropout para evitar sobreajuste.

## Método e evidências

- **Arquitetura:** encoder-decoder com seis camadas em cada lado.
- **Mecanismos centrais:** autoatenção, atenção encoder-decoder, atenção multi-head, redes feed-forward posicionais e codificação posicional.
- **Configuração-base:** dimensão 512, camada interna 2.048, oito cabeças e aproximadamente 65 milhões de parâmetros.
- **Configuração-grande:** dimensão 1.024, camada interna 4.096, 16 cabeças e aproximadamente 213 milhões de parâmetros.
- **Dados:** WMT 2014 inglês-alemão e inglês-francês.
- **Métrica principal:** BLEU.
- **Avaliação adicional:** custo aproximado de treinamento e estudos de variação arquitetural.

## Resultados aproveitáveis nos projetos

1. O Transformer fundamenta modelos contextuais empregados na classificação de descrições de chamados e ordens de serviço.
2. A autoatenção permite modelar relações entre termos distantes, como equipamento, defeito, localização e ação executada dentro da mesma descrição.
3. A atenção multi-head possibilita que diferentes subespaços representem simultaneamente aspectos semânticos, sintáticos e operacionais.
4. Codificação posicional é necessária quando a arquitetura não possui recorrência; essa escolha influencia o tratamento da ordem textual.
5. A comparação com baselines deve considerar qualidade, custo de treinamento, latência e tamanho do modelo, não apenas a métrica principal.
6. Para textos longos, o custo quadrático da atenção exige truncamento, janelas, modelos eficientes ou estratégias hierárquicas.

## Limitações e cuidados

- Os experimentos originais avaliam tradução automática, não classificação de chamados, manutenção predial ou português brasileiro.
- BLEU mede qualidade de tradução e não substitui acurácia, precisão, revocação, F1, calibração e custo do erro em classificação.
- Os resultados foram obtidos com grandes conjuntos bilíngues e oito GPUs P100; custos e ganhos precisam ser reavaliados em bases institucionais menores.
- A atenção padrão cresce quadraticamente com o comprimento da sequência.
- O artigo não resolve diretamente desbalanceamento de classes, deriva temporal, explicabilidade operacional ou governança dos dados.
- A aplicação à UFSB requer ajuste ao vocabulário técnico, siglas, categorias do GLPI e padrões de escrita dos usuários.

## Aderência aos projetos

- **Classificação de chamados e PLN:** muito alta como fundamento arquitetural.
- **Malha IA:** muito alta para justificar modelos baseados em Transformers e comparações com métodos clássicos.
- **Manutenção preditiva:** indireta, quando registros sequenciais ou descrições textuais integram modelos de risco.
- **Governança:** média, pois a arquitetura precisa ser complementada por regras de validação, explicabilidade e monitoramento.
- **ODS/ESG:** indireta, por permitir classificação semântica de documentos relacionados aos objetivos.

## Como citar em pesquisas do acervo

Use o artigo para fundamentar autoatenção, atenção multi-head, codificação posicional e a substituição da recorrência por processamento paralelo em modelos de sequência. Não atribua ao estudo resultados de classificação de chamados ou desempenho em português, pois essas aplicações exigem validação própria.
