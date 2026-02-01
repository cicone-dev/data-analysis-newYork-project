# 🗽 Airbnb NYC Analytics: Estratégias de Precificação e Segmentação

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=for-the-badge&logo=pandas)
![Status](https://img.shields.io/badge/Status-Concluído-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

> **Resumo:** Uma análise profunda de dados focada em estratégias para Business Insight, onde decisões de negócio se sobrepuseram a regras estatísticas padrão para preservar o mercado Nova York.
---
## LINK DO PROJETO
  Convido a darem uma olhada no meu artigo que publiquei no Medium com todas as minhas análises:
[clique aqui](https://medium.com/@cauan.cicone/al%C3%A9m-da-localiza%C3%A7%C3%A3o-desvendando-a-precifica%C3%A7%C3%A3o-do-airbnb-em-nyc-com-python-ef15c652d6f7)

## 💼 O Problema de Negócio
Você foi contratado como Analista de Dados para a expansão do Airbnb em Nova York. O desafio não é apenas "limpar dados", mas responder a perguntas estratégicas 
cruzando variáveis de preço, localização e comportamento dos anfitriões, chegando a insights sobre como esse mercado opera na cidade mais influente do mundo.

## 💡 O Diferencial do Projeto (Business Acumen)
Durante a Análise Exploratória (EDA), deparei-me com um dilema comum em Data Science: **Seguir a estatística cega ou o contexto de negócio?**

* **A Regra Estatística (IQR):** O cálculo matemático sugeriu remover qualquer diária acima de **$334** como *outlier*.
* **A Realidade de Mercado:** Nova York possui um mercado de luxo vibrante. Cortar em $334 significaria cegar a empresa para o segmento de alta renda.

**Decisão Estratégica:** Optei por ignorar o corte estatístico padrão e expandir o limite para **$800**, preservando dados vitais sobre o mercado *High-End* e Corporativo.

---

## 📊 Principais Insights

### 1. Manhattan vs. Brooklyn
Enquanto Manhattan dita os preços mais altos e uma alta densidade esmagadora de imóveis, Brooklyn, por sua vez, atua como uma zona de suporte, absorvendo a demanda excedente com preços ligeiramente mais competitivos, mas ainda elevados pela proximidade com a ilha.

### 2. O Que Move o Preço? (Falha do Modelo Linear)
Ao aplicar uma Regressão Linear, obtivemos um **R² de 0.32**.
* **Interpretação:** O preço em NY **não** é explicado apenas por *Bairro* ou *Tipo de Quarto*. Variáveis 'invisíveis' (luxo, proximidade específica de hubs e design) têm peso desproporcional. Isso indica a necessidade de modelos de Machine Learning mais complexos para precificação automática.

### 3. A Profissionalização dos Hosts
Identificamos *hosts* com centenas de propriedades listadas. Isso aponta para a existência de **gestores imobiliários profissionais** operando dentro da plataforma, focados no público de *Business Travel* (ticket médio > $180).

## 📢 Conclusão e Próximos Passos
A análise comprovou que estratégias de precificação únicas não funcionam em NY. A recomendação final para a diretoria é segmentar a plataforma:
  - Segmento Turismo: Foco em reviews e giro rápido ($100-$140).
  - Segmento Corporativo: Parcerias com "Super Hosts" profissionais ($180+).
---

## 📸 Algumas Visualizações do Projeto

| Grafico de Relação | Mapa de Calor NYC |
|:--------------------------------:|:------------------------------:|
| <img width="797" height="486" alt="relacao_preco_e_num_avaliacoes_tipo_de_quarto" src="https://github.com/user-attachments/assets/a1bcd76e-d6d4-4892-b717-282f94e9bb02" />| <img width="797" height="486" alt="heatmapNYC_image" src="https://github.com/user-attachments/assets/50f84394-6290-44f5-a6a0-c18c2eedea9e" />|



---


## 🛠️ Tecnologias Utilizadas


* **Google Colab** Analise dos Dados
* **Pandas & NumPy:** Manipulação e limpeza de dados.
* **Visualização:** Seaborn, Matplotlib, PyWaffle.
* **Geolocalização:** Folium & HeatMaps (Mapas de calor de densidade de preço).
* **Scikit-Learn:** Modelagem preditiva (Regressão Linear).


## 🚀 Como Executar
  - 1- Clone o repositório:

git clone [https://github.com/cicone-dev/data-analysis-newYork-project](https://github.com/cicone-dev/data-analysis-newYork-project)
  - 2- Instale as dependências:
```text
pip install -r requirements.txt
```
  - 3- Execute o Jupyter Notebook:
```text
jupyter notebook notebooks/Analise_de_Dados_NYC_airbnb_final.ipynb
```

## 📂 Estrutura do Projeto

```text
├── data/
│   ├── raw/                   # Dados brutos
│   └── processed/             # Dados limpos após tratamento
├── images/                    # Gráficos gerados (Mapas, Boxplots)
├── notebooks/
│   └── Analise_de_Dados_NYC_airbnb_final.ipynb
├── README.md
└── requirements.txt           # Dependencias



