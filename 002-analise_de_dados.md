# Tipos de Análise de Dados

Este README explica os quatro tipos principais de análise de dados:

```text
1. Análise Descritiva
2. Análise Diagnóstica
3. Análise Preditiva
4. Análise Prescritiva
```

Essas análises ajudam a transformar dados em entendimento, previsão e decisão.

---

## Visão geral

```text
Análise Descritiva   → O que aconteceu?
Análise Diagnóstica  → Por que aconteceu?
Análise Preditiva    → O que pode acontecer?
Análise Prescritiva  → O que devo fazer?
```

Elas podem ser vistas como uma evolução:

```text
Dados → Entendimento → Causa → Previsão → Decisão
```

---

# 1. Análise Descritiva

## O que é?

A Análise Descritiva responde:

```text
O que está acontecendo?
O que aconteceu?
```

Ela olha para os dados existentes e tenta resumir a situação atual ou passada.

É o tipo de análise mais básico e normalmente é o primeiro passo antes das outras análises.

---

## Exemplos de perguntas

```text
Quantos pedidos foram feitos hoje?
Qual foi o faturamento do mês?
Qual produto mais vendeu?
Qual categoria teve mais acesso?
Quantos clientes abandonaram o carrinho?
Qual foi a taxa de conversão?
```

---

## Técnicas comuns

```text
relatórios
dashboards
médias
percentuais
totais
rankings
gráficos
análise exploratória de dados - EDA
correlação
```

---

## Exemplo em e-commerce

```text
A loja teve R$ 150.000 de faturamento no mês.

O produto mais vendido foi uma camiseta preta.

A taxa de conversão foi de 2,4%.

O carrinho teve 800 abandonos.
```

Aqui a análise apenas descreve o que aconteceu.

Ela ainda não explica o motivo.

---

## Resumo

```text
Análise Descritiva = entender o passado e o presente dos dados.
```

---

# 2. Análise Diagnóstica

## O que é?

A Análise Diagnóstica responde:

```text
Por que isso aconteceu?
```

Ela tenta encontrar causas, relações e explicações para os resultados observados na análise descritiva.

---

## Exemplos de perguntas

```text
Por que as vendas caíram?
Por que a conversão subiu?
Por que uma campanha performou melhor?
Por que os clientes abandonaram o carrinho?
Por que o frete impactou a compra?
Por que uma categoria vendeu mais que outra?
```

---

## Técnicas comuns

```text
comparação entre períodos
segmentação de clientes
análise de funil
correlação
experimentos
teste A/B
análise de causa raiz
análise por canal
análise por dispositivo
```

---

## Exemplo em e-commerce

A análise descritiva mostrou:

```text
A conversão caiu de 2,4% para 1,6%.
```

A análise diagnóstica tenta descobrir o motivo:

```text
O frete ficou mais caro.
O prazo de entrega aumentou.
O checkout apresentou erro em dispositivos móveis.
Uma campanha trouxe tráfego pouco qualificado.
O produto principal ficou sem estoque.
```

---

## Exemplo com Teste A/B

Você testa duas versões de uma página de produto:

```text
Versão A: botão "Comprar agora" embaixo da descrição.
Versão B: botão "Comprar agora" próximo ao preço.
```

Resultado:

```text
Versão B converteu 18% mais.
```

A análise diagnóstica ajuda a entender que a posição do botão influenciou a conversão.

---

## Resumo

```text
Análise Diagnóstica = entender as causas do que aconteceu.
```

---

# 3. Análise Preditiva

## O que é?

A Análise Preditiva responde:

```text
O que vai acontecer?
O que provavelmente pode acontecer?
```

Ela usa dados históricos para prever cenários futuros.

Normalmente envolve estatística, Machine Learning e modelos matemáticos.

---

## Exemplos de perguntas

```text
Quanto vou vender no próximo mês?
Qual cliente tem chance de cancelar?
Qual produto pode acabar no estoque?
Qual pedido tem risco de fraude?
Qual lead tem mais chance de comprar?
Qual será a demanda futura?
```

---

## Técnicas comuns

```text
regressão
classificação
previsão
séries temporais
modelos estatísticos
Machine Learning
árvores de decisão
random forest
redes neurais
```

---

## Exemplos de uso

### Previsão de vendas

```text
Com base nos últimos 12 meses,
o modelo prevê que a loja venderá R$ 220.000 no próximo mês.
```

### Risco de fraude

```text
Pedido com score de fraude: alto.
Probabilidade de fraude: 87%.
```

### Previsão de churn

```text
Cliente X tem 72% de chance de parar de comprar.
```

### Previsão de estoque

```text
O produto Y provavelmente ficará sem estoque em 8 dias.
```

---

## Diferença importante

A análise preditiva não garante o futuro.

Ela trabalha com probabilidade.

```text
Ela não diz: isso vai acontecer com certeza.
Ela diz: isso tem alta chance de acontecer.
```

---

## Resumo

```text
Análise Preditiva = prever o que pode acontecer usando dados.
```

---

# 4. Análise Prescritiva

## O que é?

A Análise Prescritiva responde:

```text
O que devo fazer?
Qual é a melhor decisão?
Qual ação devo tomar?
```

Ela vai além da previsão.

A análise preditiva diz o que pode acontecer.

A análise prescritiva sugere o que fazer diante disso.

---

## Exemplos de perguntas

```text
Qual desconto devo aplicar?
Qual produto devo comprar mais para o estoque?
Qual campanha devo pausar?
Qual cliente devo priorizar?
Qual rota de entrega é melhor?
Qual preço maximiza lucro e conversão?
Como alocar recursos limitados?
```

---

## Técnicas comuns

```text
otimização
alocação
tomada de decisão
planejamento
simulações
regras de negócio
modelos de decisão
sistemas de recomendação
```

---

## Exemplo em e-commerce

A análise preditiva mostra:

```text
O produto X deve acabar em 8 dias.
```

A análise prescritiva recomenda:

```text
Comprar mais 500 unidades.
Priorizar fornecedor com prazo menor.
Aumentar o preço em 5% enquanto o estoque está baixo.
Reduzir campanha paga até o estoque ser reposto.
```

---

## Exemplo com desconto

A análise preditiva mostra:

```text
Clientes do grupo A têm alta chance de comprar com 10% de desconto.
Clientes do grupo B só compram com 20% de desconto.
```

A análise prescritiva decide:

```text
Enviar cupom de 10% para o grupo A.
Enviar cupom de 20% apenas para o grupo B.
Evitar dar desconto alto para quem compraria de qualquer forma.
```

---

## Resumo

```text
Análise Prescritiva = recomendar a melhor ação a partir dos dados.
```

---

# Comparação entre as análises

| Tipo de análise | Pergunta principal | Foco | Exemplo |
|---|---|---|---|
| Descritiva | O que aconteceu? | Entender dados passados/presentes | Faturamento do mês |
| Diagnóstica | Por que aconteceu? | Encontrar causas | Vendas caíram por causa do frete |
| Preditiva | O que pode acontecer? | Prever futuro | Produto pode acabar em 8 dias |
| Prescritiva | O que devo fazer? | Recomendar ação | Comprar mais estoque |

---

# Exemplo completo

Imagine uma loja virtual.

## 1. Análise Descritiva

```text
As vendas caíram 20% esta semana.
```

Aqui você sabe o que aconteceu.

---

## 2. Análise Diagnóstica

```text
As vendas caíram porque o frete aumentou,
o prazo de entrega ficou maior
e o checkout teve erro no mobile.
```

Aqui você entende por que aconteceu.

---

## 3. Análise Preditiva

```text
Se nada for feito,
as vendas podem cair mais 15% na próxima semana.
```

Aqui você prevê o que pode acontecer.

---

## 4. Análise Prescritiva

```text
Reduzir o frete para pedidos acima de R$ 199.
Corrigir o erro no checkout mobile.
Criar uma campanha para produtos com maior margem.
```

Aqui você decide o que fazer.

---

# Relação com IA e Machine Learning

Essas análises podem usar IA em diferentes níveis.

## Análise Descritiva

Normalmente usa:

```text
SQL
BI
dashboards
relatórios
estatística básica
```

Pode ter IA, mas não precisa.

---

## Análise Diagnóstica

Pode usar:

```text
estatística
correlação
segmentação
testes A/B
análise de causa
```

Pode usar IA para encontrar padrões mais difíceis.

---

## Análise Preditiva

Aqui Machine Learning aparece bastante.

Exemplos:

```text
modelo para prever vendas
modelo para detectar fraude
modelo para prever churn
modelo para prever demanda
```

---

## Análise Prescritiva

Pode usar IA, otimização e regras de negócio para recomendar ações.

Exemplos:

```text
qual preço usar
qual campanha ativar
qual cliente priorizar
qual estoque comprar
qual rota seguir
```

---

# Relação com IA Generativa

IA Generativa também pode ajudar nessas análises.

Exemplos:

## Na análise descritiva

```text
Resumir relatórios.
Explicar dashboards.
Transformar números em texto.
```

## Na análise diagnóstica

```text
Ajudar a levantar hipóteses.
Comparar períodos.
Explicar possíveis causas.
```

## Na análise preditiva

```text
Explicar previsões de modelos.
Gerar relatórios sobre risco e tendência.
```

## Na análise prescritiva

```text
Sugerir ações.
Criar planos.
Explicar decisões.
Gerar recomendações para negócio.
```

Importante:

```text
A IA Generativa não substitui automaticamente a análise de dados.
Ela ajuda a interpretar, explicar e transformar dados em decisões.
```

---

# Frases para memorizar

```text
Descritiva = o que aconteceu.
```

```text
Diagnóstica = por que aconteceu.
```

```text
Preditiva = o que pode acontecer.
```

```text
Prescritiva = o que devo fazer.
```

---

# Mapa mental

```text
Análise de Dados
│
├── Descritiva
│    └── O que aconteceu?
│
├── Diagnóstica
│    └── Por que aconteceu?
│
├── Preditiva
│    └── O que pode acontecer?
│
└── Prescritiva
     └── O que devo fazer?
```

---

# Ordem prática de uso

Na prática, você geralmente começa pela descritiva e evolui até a prescritiva:

```text
1. Olhar os dados
2. Entender o que aconteceu
3. Descobrir o motivo
4. Prever o que pode acontecer
5. Decidir o que fazer
```

Ou:

```text
Descritiva → Diagnóstica → Preditiva → Prescritiva
```

---

# Resumo final

As quatro análises representam níveis diferentes de maturidade no uso dos dados.

```text
Descritiva:
mostra o que aconteceu.

Diagnóstica:
explica por que aconteceu.

Preditiva:
estima o que pode acontecer.

Prescritiva:
recomenda o que fazer.
```

Quanto mais avançada a análise, mais ela se aproxima de decisão, automação e uso de IA.

