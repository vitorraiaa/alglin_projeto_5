# Desafio Netflix - Sistema de Recomendação de Filmes

Este projeto implementa um sistema de recomendação de filmes usando a decomposição de matrizes, especificamente a Singular Value Decomposition (SVD), para prever as avaliações que os usuários dariam a filmes que ainda não assistiram. Ele utiliza o [The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset) disponível no Kaggle.


## Partcipantes

- Vitor Raia
- João Citino

## Visão Geral

A abordagem utilizada é baseada na decomposição SVD para obter fatores latentes que representam perfis de usuários e características de filmes. A partir desses fatores, é possível reconstruir a matriz de avaliações e prever avaliações desconhecidas. O código do projeto segue as etapas abaixo:

1. **Carregamento e preparação dos dados**: Os dados de avaliações são carregados, filtrados, e uma matriz de avaliações é criada, onde as linhas representam usuários e as colunas representam filmes.
2. **Decomposição SVD**: A matriz de avaliações é decomposta em três componentes usando SVD. Os valores singulares são ajustados para reduzir o ruído, melhorando a capacidade de generalização do modelo.
3. **Predição de avaliações**: Avaliações desconhecidas são estimadas a partir da reconstrução da matriz, usando uma versão truncada dos valores singulares.
4. **Cálculo e análise de erro**: O modelo insere avaliações simuladas e compara com a avaliação original, calculando o erro de predição. O erro é registrado e exibido em um histograma.

## Requisitos

- Python 3.x
- Pandas
- NumPy
- SciPy
- Matplotlib

Você pode instalar as bibliotecas necessárias com o seguinte comando:
```bash
pip install pandas numpy scipy matplotlib
```


## Referências 

Este projeto é inspirado em técnicas de sistemas de recomendação populares, especialmente a abordagem de decomposição de matrizes. A técnica de fatoração de matrizes utilizada foi fundamentada no trabalho de Koren et al. (2009), que discute detalhadamente a aplicação de técnicas de fatoração de matrizes para sistemas de recomendação, como o Netflix Prize Challenge [1]. Além disso, o conceito de SVD em sistemas de recomendação foi influenciado pelas práticas sugeridas por Funk (2006) em seu artigo sobre atualizações para a recomendação de filmes no Netflix [2].

<a id="1"></a>Koren, Y., Bell, R., & Volinsky, C. (2009). Matrix Factorization Techniques for Recommender Systems. IEEE Computer, 42(8), 30-37.
<a id="2"></a>Funk, S. (2006). Netflix Update: Try This at Home.