# Projeto de Mineração de Dados


## 🧑‍💻 Autores  
- Vinícius Cavalcante Barbosa (202311250049) - cavalcante.barbosa@academico.ifpb.edu.br  
- Nivaldo Pereira da Silva Neto (202021250035) - nivaldo.neto@academico.ifpb.edu.br


## 🎯 Tema e Motivação  
A NBA passou por grandes transformações desde sua criação, refletidas em mudanças no estilo de jogo, nas regras e no perfil dos jogadores. Nas últimas décadas, observamos uma crescente valorização dos arremessos de três pontos, maior ritmo de jogo e diferentes estratégias ofensivas e defensivas. Este projeto tem como objetivo analisar a evolução estatística da NBA ao longo das décadas, identificando como o jogo mudou de forma quantitativa. Além disso, a possibilidade de se encontrar outliers em que na verdade seriam os conhecidos jogadores de destaque daquela década e, com os ajustes necessários, verificar se ele continuaria sendo um outlier em difentes décadas.

A motivação para esse estudo surgiu do interesse em compreender como essas transformações se manifestam nos dados. Será possível visualizar, por exemplo, o aumento nos arremessos de 3 pontos, a queda no número de rebotes, a mudança no tempo médio em quadra ou até o quanto um determinado jogador (outlier) está influenciando nas estatísticas gerais? Essa análise permite observar tendências históricas e entender como o jogo se adaptou às novas gerações de atletas e à dinâmica moderna do basquete.


## 📊 Conjunto de Dados Selecionado  
- List of all the NBA and ABA Players
- List of all the NBA & ABA Teams
- NBA & ABA League Index
- NBA & ABA Leaders and Records
- NBA Players stats since 1950


- **Fonte:**  
  [Kaggle - NBA Player Stats](https://www.kaggle.com/datasets/drgilermo/nba-players-stats/data)
  
  [Basketball Reference - Jogadores](https://www.basketball-reference.com/players/)
  
  [Basketball Reference - Times](https://www.basketball-reference.com/teams/)
  
  [Basketball Reference - Temporadas](https://www.basketball-reference.com/leagues/)
  
  [Basketball Reference - Líderes](https://www.basketball-reference.com/leaders/)
  

- **Descrição breve:**  
  
  O primeiro conjunto de dados contém estatísticas por temporada de todos os jogadores da NBA por volta dos anos 1950 até 2022. As variáveis incluem pontos por jogo (PPG), assistências (APG), rebotes (RPG), arremessos tentados e convertidos (FG, 3P, FT), entre outras métricas relevantes. O escopo é histórico e permite uma análise temporal das tendências da liga ao longo de mais de 70 anos.

  Os outros conjunto de dados, os do basketball reference, contém estatísticas dos jogadores, times, das temporadas da liga e dos líderes de uma determinada estatística em uma determinada temporada. Dessa forma, contém dados semelhantes aos descritos no primeiro parágrafo, além de dados também que podem ser encontrados na fase de playoffs, caso se necessite de uma maior detalhamento nas fases e comparações ao longo das décadas.
  

- **Justificativa para a escolha:**  
  Por conter dados extensos e bem organizados por temporada, esse conjunto é ideal para analisar a evolução do jogo ao longo do tempo. Ele permite identificar tendências, mudanças de estilo e transformações estratégicas que ocorreram nas diferentes eras da NBA.


---


## ❓ Perguntas ou Hipóteses  
- Como evoluíram as médias de pontos, assistências e rebotes por jogador ao longo das décadas?
- Em que momento os arremessos de 3 pontos passaram a ser mais utilizados?
- Houve uma mudança significativa no perfil estatístico dos jogadores (por exemplo, alas que arremessam mais ou pivôs que passam mais)?
- Quais métricas mais refletem a modernização do estilo de jogo?
- A mudança se dá por causa da necessidade que um time tem de jogar daquele modo ou por causa do impacto de um determinado jogador (outlier)?
- Na fase dos playoffs existe alguma mudança significativa na maneira em que os dados serão apresentados em cada década?
  

Técnicas estatísticas utilizadas:
- Análise exploratória
- Correlações
- Modelos Preditivos: Regressão Linear, Random Forest e Rede Neural


## 🛠️ Ferramentas Utilizadas    
Quais linguagens, bibliotecas ou softwares serão utilizados no projeto.
- Linguagem utilizada: Python
- Bibliotecas utilizadas: Pandas, Seaborn, Matplotlib, Numpy, Requests, StringIO, Combinations, tensorflow, sklearn
- Ambiente utilizado: Google Colab



## 📈 Resultados  
Com base na análise exploratória e nos modelos de regressão, podemos destacar os seguintes resultados principais:

- Evolução das Estatísticas Ofensivas: A análise temporal mostrou um aumento significativo na média de tentativas de arremessos de 3 pontos (3PA) por jogo ao longo das décadas, especialmente a partir dos anos 80, refletindo a crescente importância do perímetro no jogo moderno. A média de pontos por jogo (PTS/G) também mostrou variações, com um pico nos anos 60 e uma tendência de aumento nas décadas mais recentes. A taxa de uso (USG%) teve uma leve queda nas últimas décadas, sugerindo uma distribuição mais equilibrada das posses. O True Shooting Percentage (TS%) tem uma tendência de aumento, indicando maior eficiência ofensiva geral.

- Mudança no Perfil Posicional: A análise do Player Efficiency Rating (PER) e do TS% por posição, bem como a contagem de jogadores por posição ao longo do tempo, demonstrou uma mudança na dinâmica do jogo. Houve uma convergência nas medianas de PER entre as posições, indicando maior versatilidade dos jogadores. O número de pivôs (C) diminuiu, enquanto o de alas (SF/SG) e armadores (PG) aumentou, refletindo a preferência por jogadores que "abrem a quadra". Alas (SF) mostraram uma mediana de pontos por jogo mais alta em muitos casos, destacando sua importância como jogadores híbridos.
  
- Modelos de Predição de Pontos por Jogo: Três modelos de regressão (Regressão Linear, Random Forest Regression e Rede Neural) foram construídos para prever os pontos por jogo (pts_pg). Todos os modelos apresentaram alto desempenho (R² próximo de 1), indicando que as features selecionadas são altamente preditivas para essa métrica. O modelo Random Forest Regression identificou as features mais importantes para prever pts_pg, com destaque para arremessos convertidos (fg) e jogos disputados (g_player_totals).


## 📌 Conclusões  
As análises estatísticas e a modelagem preditiva confirmam a hipótese de que a NBA passou por uma evolução estatística significativa ao longo das décadas, impulsionada principalmente pela crescente valorização do arremesso de três pontos e por uma maior versatilidade posicional. O jogo moderno favorece jogadores que podem contribuir de diversas formas, não apenas em suas posições tradicionais. Os modelos de predição demonstraram que as estatísticas coletadas são eficazes na previsão do desempenho ofensivo individual, e a análise de importância das features valida que as métricas relacionadas à pontuação e tempo de jogo são os principais determinantes dos pontos por jogo. Essa transformação tática tem implicações diretas na forma como os times são montados e as estratégias de jogo são planejadas.


## ⚠️ Limitações e Trabalhos Futuros  
Dados Ausentes: Alguns datasets apresentaram uma quantidade considerável de valores ausentes em certas colunas, como birth_year e métricas avançadas em temporadas mais antigas. Embora tenhamos lidado com alguns ausentes (como na preparação para os modelos de regressão), a exclusão ou imputação pode impactar a análise, especialmente para as décadas iniciais.
Abrangência dos Dados: Embora os datasets sejam extensos, métricas mais detalhadas ou dados de rastreamento de jogadores (player tracking data) não estavam disponíveis, o que poderia fornecer insights mais profundos sobre movimentação, espaçamento e interações em quadra.
Foco na Temporada Regular: A análise se concentrou principalmente nos dados da temporada regular, sem uma comparação aprofundada com o desempenho nos playoffs, onde a dinâmica do jogo pode mudar.
Variáveis Explicativas: A análise de causalidade (se a mudança se deve a táticas de time ou jogadores específicos) foi explorada de forma qualitativa com base nas tendências, mas não quantificada diretamente através de modelos causais.

Trabalhos Futuros:
- Análise de Outliers: Investigar os outliers estatísticos em diferentes décadas para identificar jogadores excepcionais e analisar como suas métricas se comparariam em outras eras da NBA.
- Análise de Métricas Defensivas: Realizar uma análise similar focada em métricas defensivas para entender a evolução desse aspecto do jogo.
- Modelos de Classificação: Desenvolver modelos para classificar jogadores (por exemplo, em categorias como "All-Star", "Role Player") ou prever resultados de jogos com base nas estatísticas.
---
