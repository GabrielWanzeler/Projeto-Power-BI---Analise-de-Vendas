# Projeto Power BI - Dashboard de Vendas



# Objetivo do projeto

Criar um dashboard interativo no Power BI para analisar o desempenho comercial da empresa fictícia Superstore, com foco em faturamento, lucro, margem de lucro e comportamento ao longo do tempo, auxiliando na tomada de decisão estratégica.







## Dataset

Base de vendas fictícia (Superstore) obtida no Kaggle.







## Ferramentas

* Power BI Desktop
* Power Query (ETL)
* DAX (medidas e KPIs)







## Estrutura do Projeto

dashboard-powerbi-superstore/
│
├── dashboard/
│   └── dashboardSuperstore.pbix
│
├── dataset/
│   └── superstore.xlsx
│
├── docs/
│   └── anotacoes\_modelagem\_e\_dax.md

│
├── imagens/
│   └── dashboard\_preview.png

│
└── README.md



## Descrição

### Estrutura dos Dados

Fonte: superstore.xlsx

Modelagem: Esquema estrela

Fato: Fato\_Vendas

Dimensões: Dim\_Produto; Dim\_Local; Dim\_Tempo; Dim\_Clientes.



### Principais Métricas

* Faturamento Total
* Lucro Total
* Margem de Lucro (%)
* Quantidade Vendida
* Ticket Médio



### Análises no Dashboard

* Evolução do faturamento ao longo do tempo
* Comparação de faturamento por categoria
* Desempenho financeiro por categoria e subcategoria
* Ticket médio por produto



### Filtros interativos por:

* Segmento
* Região
* Período







## Principais Insights

* A categoria Technology apresenta o maior faturamento e margem de lucro
* Algumas subcategorias apresentam alto faturamento com baixa margem
* O faturamento apresenta crescimento gradual ao longo dos anos analisados







## Observações Técnicas

* Modelagem realizada em esquema estrela para garantir performance e clareza analítica;
* Uso de Dimensão de Tempo dedicada para análises temporais consistentes;
* Métricas financeiras implementadas como medidas DAX, assegurando consistência nos totais;
* Tratamento e organização dos dados realizados no Power Query;
* Layout desenvolvido com foco em hierarquia visual e facilidade de interpretação
