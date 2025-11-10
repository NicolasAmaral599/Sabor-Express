Rota Inteligente: Otimização de Entregas com Algoritmos de IA
1. Descrição do Problema e Objetivos
   Este projeto foi desenvolvido para atender à demanda da empresa "Sabor Express", que enfrenta desafios logísticos críticos, como atrasos nas entregas e rotas ineficientes durante horários de pico. O objetivo principal é implementar uma solução baseada em Inteligência Artificial para automatizar o planejamento de rotas, visando a redução do tempo de entrega e dos custos operacionais.

O desafio consiste em modelar a cidade como um grafo e utilizar algoritmos para agrupar entregas próximas e determinar o caminho mais eficiente para cada entregador.
2. Abordagem Adotada
A solução foi estruturada em duas etapas principais para garantir eficiência e escalabilidade:

Agrupamento de Pedidos (Clustering): Inicialmente, aplica-se o algoritmo K-Means para segmentar os pontos de entrega em zonas distintas. Essa estratégia permite distribuir a carga de trabalho de forma equilibrada entre os entregadores disponíveis, garantindo que cada um opere em uma região geográfica restrita.

Roteamento Otimizado (Busca em Grafos): Após a definição das zonas, o problema é tratado como um grafo onde os locais de entrega são vértices. Utiliza-se uma abordagem heurística de busca (baseada no princípio do vizinho mais próximo) para determinar a sequência de visitas que minimiza a distância total percorrida por cada entregador, partindo e retornando ao ponto central (HUB).

3. Algoritmos Utilizados
   K-Means: Algoritmo de aprendizado não supervisionado utilizado para o agrupamento espacial dos pedidos em $k$ clusters, onde $k$ representa o número de entregadores6666.
   Busca Heurística (Nearest Neighbor): Técnica de otimização empregada para solucionar o Problema do Caixeiro Viajante (TSP) dentro de cada cluster, definindo uma rota subótima, porém eficiente, em tempo computacional viável7777.

4. Tecnologias e Ferramentas
O projeto foi implementado em Python no ambiente Google Colab, utilizando as seguintes bibliotecas para suporte matemático e visualização:

scikit-learn: Implementação do algoritmo K-Means.

networkx: Modelagem e manipulação de estruturas de grafos.

numpy: Operações vetoriais e cálculo de distâncias.


matplotlib: Geração de gráficos para análise visual dos resultados   


5. Análise dos Resultados
A simulação demonstrou a eficácia da abordagem híbrida (clustering + roteamento).

Visualização dos Agrupamentos
O mapa abaixo ilustra a segmentação eficaz da área de atendimento em zonas distintas, validando a aplicação do K-Means para divisão territorial.

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/ccfd542c-0b95-4893-9251-0fd7914a9da5" />

Rotas Geradas
As rotas calculadas para cada zona demonstram caminhos lógicos e sequenciais, reduzindo deslocamentos desnecessários e otimizando o tempo total de rota.

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/80af3421-2497-48e3-93f8-75493da5e56b" />


Limitações e Melhorias Futuras

A solução atual utiliza distâncias euclidianas (linha reta), o que representa uma simplificação do cenário real. Para trabalhos futuros, sugere-se a integração com APIs de mapas (como Google Maps ou OpenStreetMap) para considerar a malha viária real e variáveis dinâmicas como o tráfego em tempo real.

6. Instruções de Execução
Para reproduzir os resultados deste projeto:

Acesse o notebook .ipynb através do Google Colab.

No menu principal, navegue até "Ambiente de execução" e selecione "Executar tudo".

O script instalará as dependências necessárias e executará a simulação automaticamente.


   
