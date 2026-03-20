# 🛒 Análise de Cestas de Compras (Market Basket Analysis)

## 📌 Introdução

Este projeto tem como objetivo analisar o comportamento de compra de clientes de um supermercado, utilizando técnicas de Market Basket Analysis. A proposta é identificar associações entre produtos para auxiliar na tomada de decisão gerencial, visando aumentar o ticket médio, melhorar o layout da loja e otimizar estratégias promocionais.

---

## ⚙️ Metodologia

Foi utilizado o algoritmo **Apriori** para identificar conjuntos frequentes de produtos no dataset. A partir desses conjuntos, foram geradas regras de associação com base nas métricas:

* **Suporte**: frequência com que a combinação de itens aparece
* **Confiança**: probabilidade de compra de um item dado outro
* **Lift**: força da associação entre os produtos

Para garantir relevância prática, foram filtradas apenas regras com:

* Confiança > 0.6
* Lift > 1.2
* No máximo 2 itens no antecedente e consequente

---

## 📊 Principais Resultados

As regras mais relevantes encontradas foram:

* Se o cliente compra **café e refrigerante**, há 87% de chance de também comprar **açúcar e cerveja** (lift = 6.61)
* Se o cliente compra **açúcar e refrigerante**, há 86% de chance de também comprar **café e cerveja** (lift = 6.58)
* Se o cliente compra **frango e refrigerante**, há 94% de chance de também comprar **feijão e cerveja** (lift = 5.64)
* Se o cliente compra **refrigerante e feijão**, há 92% de chance de também comprar **arroz e cerveja** (lift = 5.50)
* Se o cliente compra **arroz e café**, há 92% de chance de também comprar **açúcar e feijão** (lift = 4.56)

Esses resultados indicam fortes padrões de compra conjunta entre produtos alimentícios e bebidas.

---

## 🧠 Insights de Negócio

### 🧲 Produtos âncora

Produtos como **refrigerante, cerveja, arroz e feijão** aparecem frequentemente nas regras, indicando que funcionam como itens centrais nas compras.

---

### 💸 Oportunidades de promoção

* Criar combos promocionais como:

  * Refrigerante + cerveja
  * Café + açúcar
  * Arroz + feijão
* Oferecer descontos progressivos na compra conjunta desses itens

---

### 🛒 Organização do layout

* Posicionar produtos frequentemente comprados juntos próximos nas gôndolas:

  * Café próximo ao açúcar
  * Arroz próximo ao feijão
  * Bebidas agrupadas estrategicamente
* Alternativamente, separar alguns itens para estimular a circulação do cliente na loja

---

### ⚠️ Regras menos úteis

Regras com muitos produtos foram descartadas, pois apesar de apresentarem alto valor estatístico, são pouco práticas para aplicação real no supermercado.

---

## 🚀 Conclusão

A análise permitiu identificar padrões relevantes no comportamento de compra dos clientes, possibilitando a criação de estratégias mais eficientes de vendas e marketing. A aplicação dessas insights pode contribuir diretamente para o aumento do ticket médio e melhoria da experiência do cliente.

---

## 📁 Estrutura do Projeto

* `basket_supermercado_1000.csv` → Dataset utilizado
* `notebook.ipynb` → Código da análise
* `README.md` → Relatório do projeto

---

## 👨‍💻 Autor

Projeto desenvolvido para a disciplina de Inteligência Artificial.
