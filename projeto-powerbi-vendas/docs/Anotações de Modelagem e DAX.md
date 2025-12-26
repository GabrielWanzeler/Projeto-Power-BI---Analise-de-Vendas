# Anotações de Modelagem e DAX - Power BI



## Modelagem de Dados

### Estrutura em estrela (Star Schema)

### Separação entre:

* Tabela Fato (Fato\_Vendas)
* Tabelas Dimensão (Dim\_Produtos, Dim\_Cliente, Dim\_Locais, Dim\_Tempo)

### Relacionamentos:

* 1:\* (Dim → Fato)
* Direção de filtro: simples



### Tabela Dim\_Tempo

\####Coluna Data criada com DAX

#### Relacionamentos:

* 1:\* (Dim → Fato)
* Direção de filtro: simples
  ####Usada nas análises temporais



## Medidas DAX Criadas

### Faturamento

`Faturamento = SUM(Sales\[Sales]) `

### Lucro

`Lucro = SUM(Sales\[Profit]) `

### Margem de Lucro (%)

`Margem de Lucro (%) = DIVIDE(\[Lucro], \[Faturamento])`

### Quantidade Vendida

`Quantidade Vendida = SUM(Fato\_Vendas\[Quantity])`

### Ticket Médio

`Ticket Médio = DIVIDE(\[Faturamento], \[Quantidade Vendida])`



## Boas práticas aplicadas

* Uso de medidas ao invés de colunas calculadas
* Colunas técnicas ocultadas
* Nomes claros e padronizados
* Formatação correta (moeda, %)



## Observações Analíticas

* O faturamento apresenta forte concentração em poucas categorias e subcategorias, é responsável pela maior parte da receita total;
* Categorias com alto faturamento nem sempre apresentam margens de lucro elevadas. Volume de vendas não é sinônimo de rentabilidade;
* O faturamento apresenta variações com períodos de crescimento e retração. Há possível sazonalidade nas vendas;
* Variação significativa de faturamento e lucro entre regiões. Desempenho comercial  geograficamente não é homogêneo;
* Algumas subcategorias concentram tanto faturamento quanto lucro, enquanto outras apresentam baixa contribuição financeira.
