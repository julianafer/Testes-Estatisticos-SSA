# Teste de Hipótese em Dados de Varejo

Este repositório contém o desenvolvimento da atividade da disciplina **Métodos Estatísticos**, cujo objetivo é aplicar técnicas de inferência estatística utilizando um dataset analítico do domínio de varejo.

O estudo investiga se produtos que participaram de ações promocionais do tipo *display* apresentam maior quantidade média de unidades vendidas quando comparados a produtos que não participaram dessas ações.

## Objetivo

Avaliar a seguinte hipótese de pesquisa:

* **H₀ (Hipótese nula):** Produtos com e sem ações promocionais do tipo *display* apresentam a mesma média de unidades vendidas.
* **H₁ (Hipótese alternativa):** Produtos que participaram de ações promocionais do tipo *display* apresentam maior média de unidades vendidas.

## Dataset

Foi utilizado um **dataset analítico** construído na disciplina de Ciência de Dados, a partir da integração da base **Dunnhumby – The Complete Journey**.

O conjunto de dados reúne informações de produtos, vendas e promoções, permitindo a realização de análises estatísticas sobre o impacto de ações promocionais no desempenho de vendas.

## Estrutura do Projeto

```text
.
├── data/
│   └── df_analytical.csv
│
├── docs/
│   └── dataset_description.md
│
├── notebooks/
│   ├── 01_exploratory_data_analysis.ipynb
│   ├── 02_statistical_assumptions.ipynb
│   └── 03_statistical_hypothesis_testing.ipynb
│
├── .gitignore
└── README.md
```

## Etapas da Análise

O projeto foi desenvolvido seguindo as seguintes etapas:

1. Análise exploratória dos dados;
2. Verificação dos pressupostos estatísticos;
3. Aplicação do teste t de Welch;
4. Cálculo do intervalo de confiança;
5. Avaliação do tamanho do efeito (Cohen's *d*);
6. Interpretação dos resultados.

## Principais Ferramentas

* Python
* Pandas
* NumPy
* SciPy
* Statsmodels
* Matplotlib
* Seaborn

## Principais Resultados

Os testes indicaram diferença estatisticamente significativa entre produtos com e sem ações promocionais do tipo *display*. Entretanto, a análise do tamanho do efeito mostrou que essa diferença possui baixa magnitude prática, sugerindo que outros fatores além da participação em ações de *display* também influenciam o desempenho de vendas dos produtos.

## Autor

**Juliana Ferreira Cavalcante**

Disciplina: **Métodos Estatísticos**
