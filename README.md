##### Baseado no artigo Review of deep learning: concepts, CNN architectures, challenges, applications, future directions (Alzubaidi, L. 2021), descreva os principais desafios e limitações de DL. Quais alternativas os autores dão aos problemas?

1) A necessidade de grandes volumes de dados para treinamento é uma tarefa árdua para que se alcançe um modelo de desempenho bem comportado, ou seja, à medida que os dados aumentam, um modelo de desempenho extra bem comportado pode ser alcançado;

2) O desbalanceamento de dados pode influenciar diretamente na capacidade de generalização para todas as classes e gerar vieses indesejados em direção às classes majoritárias;

3) As técnicas de DL são verdadeiras "caixas-pretas", tornando difícil entender como as decisões do modelo são tomadas e explicá-las para a partes interessadas;

4) Obter escores de confiança para previsões do modelo;

5) A introdução de novas informações pode levar ao esquecimento de informações aprendidas anteriormente;

6) A falta de restrições suficientes ou informações para definir uma solução única e inequívoca. Essa questão é particularmente evidente quando os modelos de ML mostram comportamentos inesperados ou baixos desempenhos em casos de teste do mundo real, apesar de terem sido treinados e avaliados em conjuntos de dados reais; 

As possíveis soluções sugeridas pelos autores são: utilização da transferência de aprendizado após a coleta de dados de tarefas semelhantes, aumento de dados, como tradução, espelhamento e rotação de imagens; utilização de perda ponderada de _cross entropy_ para equilibrar o desempenho em classes pequenas e grandes; uso de técnicas baseadas em _backpropagation_ e perturbação para interpretar o modelo; ajustar as saídas _softmax_ para obter _scores_ de probabilidade confiáveis; aprendizado com memória dupla para lidar com o esquecimento catastrófico; aplicar "testes de resistência" para examinar até que ponto um modelo funciona bem em dados do mundo real e para descobrir os possíveis problemas. 

##### Cite 3 aplicações de algoritmos de Deep Learning. Uma delas tem que usar uma solução com CNN e uma delas tem que usar uma solução de RNNs. Explique a aplicação e os resultados obtidos. Não deixe de citar a fonte utilizada, sendo preferencialmente artigos.

```1. Reconhecimento facial com CNNs```

É uma técnica amplamente utilizada para identificar indivíduos com base em suas características faciais, sendo aplicada em diversas áreas, como segurança, biometria, saúde, educação.

Uma abordagem comum para realizar o reconhecimento facial é por meio do uso de redes neurais convolucionais (CNNs) que são particularmente eficazes na identificação de padrões em imagens. No processo de reconhecimento facial com CNNs, a rede é treinada para aprender a identificar características únicas do rosto de uma pessoa, como a forma do rosto, a posição dos olhos, boca e nariz, bem como as linhas da pele. Após o treinamento da CNN, ela se torna capaz de identificar indivíduos ao comparar as características faciais presentes em uma imagem com as características aprendidas durante o treinamento. Essa comparação é fundamental para a capacidade da rede em reconhecer e distinguir diferentes pessoas. Além disso, as CNNs extraem automaticamente características hierárquicas das imagens, passando de bordas e texturas simples em camadas iniciais para características faciais mais complexas em camadas mais profundas.

O treinamento da CNN ocorre de maneira supervisionada, utilizando pares de imagens e rótulos correspondentes durante o processo. O resultado final desse processo é um vetor de características conhecido como _embedding facial_, que representa de forma compacta as características essenciais da face e é utilizado para comparações.

O reconhecimento facial enfrenta alguns desafios, como a necessidade de conjuntos de dados extensos para treinamento, considerações éticas relacionadas à privacidade e questões de viés étnico. No entanto, suas aplicações vão além da segurança, abrangendo autenticação, organização de fotos e entretenimento em redes sociais.

A pesquisa contínua busca aprimorar o reconhecimento facial, explorando arquiteturas avançadas, técnicas de aumento de dados e considerações éticas para garantir uma aplicação mais precisa, robusta e ética dessa tecnologia em constante evolução.

**Artigo**: https://arxiv.org/pdf/1503.03832.pdf


```2. Reconhecimento de voz com RNNs```

A técnica de reconhecimento de voz viabiliza a identificação de palavras por meio da voz humana, encontrando aplicação em diversas áreas, como tradutores automáticos, assistentes virtuais, reconhecimento de falas, segurança, acessibilidade, dentre outras.

Para realizar o reconhecimento de voz, uma abordagem comum é empregar redes neurais recorrentes (RNNs),que são especializadas na identificação de padrões em sequências de dados.

No contexto do reconhecimento de voz, as RNNs desempenham o papel de aprender a discernir as características específicas da fala associadas a cada palavra, onde essas características englobam a frequência e a duração dos sons emitidos e a ordem em que eles ocorrem. Após o treinamento da RNN, ela se torna apta a identificar palavras o que é feito por meio da comparação entre as sequências de sons de entrada e aquelas que a rede neural absorveu durante o treinamento.

O reconhecimento de voz com o uso de RNNs destaca-se por sua precisão e tem demonstrado eficácia em diversas aplicações. A habilidade dessas redes neurais em compreender a estrutura sequencial das informações sonoras as torna uma escolha robusta para lidar com a complexidade da fala humana em variados contextos e cenários.

**Artigo**: https://arxiv.org/pdf/1303.5778.pdf


```3. Produção de textos com LSTMs```

É uma técnica que viabiliza a produção de conteúdo textual inédito e original, sendo aplicada em diversas situações, como na geração de conteúdo, tradução automática, automação de respostas, marketing digital, dentre outras.

Um método comum para realizar a geração de texto é empregar redes neurais de memória de longo prazo (LSTMs). As LSTMs, são tipos de redes neurais recorrentes e destacam-se por sua habilidade em reter informações ao longo de períodos extensos.

No contexto da geração de texto, as LSTMs são empregadas para aprender a sequência de caracteres mais provável de ocorrer em seguida. Esse processo envolve a consideração da sequência de caracteres anterior e das informações previamente adquiridas pela LSTM. Após o treinamento da LSTM, ela torna-se apta a gerar texto inédito que é alcançado gerando um caractere de cada vez, levando em conta a sequência de caracteres precedente e as informações previamente aprendidas.

**Artigo**: https://arxiv.org/pdf/2005.00048.pdf
