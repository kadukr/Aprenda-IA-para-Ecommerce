'# Lidando com Incertezas

Este README explica como lidar com incertezas usando **raciocínio probabilístico**, **estimativas**, **distribuições de probabilidade**, **Teorema de Bayes** e **Redes Bayesianas**.

A ideia principal é:

> No mundo real, nem sempre temos certeza do que vai acontecer. Por isso, precisamos modelar incertezas para fazer boas estimativas, previsões e decisões.

---

## 1. O que significa lidar com incertezas?

No dia a dia, nós usamos muitas informações de forma implícita.

Exemplos:

```text
Parece que vai chover.
Esse cliente provavelmente vai comprar.
Esse produto deve vender bem no fim de semana.
Essa campanha parece estar funcionando.
Esse pedido parece suspeito.
```

Muitas vezes fazemos isso com:

```text
experiência
intuição
heurísticas
dados anteriores
informações incompletas
observações do contexto
```

Mas na computação não dá para deixar tudo implícito.

O sistema precisa receber uma forma estruturada de representar essas incertezas.

Por isso usamos:

```text
probabilidade
estatística
modelos matemáticos
distribuições
raciocínio probabilístico
modelos preditivos
redes bayesianas
```

---

## 2. Heurísticas no dia a dia

Heurística é uma regra prática usada para tomar decisões rápidas.

Exemplo humano:

```text
Se o cliente já comprou antes,
passou bastante tempo no site
e clicou em uma promoção,
então ele tem boa chance de comprar novamente.
```

Isso é uma heurística.

Mas para um sistema computacional, precisamos transformar essa ideia em variáveis e probabilidades.

Exemplo estruturado:

```text
HistoricoCompras = sim ou não
TempoNoSite = pouco ou muito
ClicouEmPromocao = sim ou não
ProbabilidadeDeCompra = valor entre 0 e 1
```

Assim o sistema consegue calcular uma estimativa.

---

## 3. Por que isso é importante em e-commerce?

Em e-commerce, quase tudo envolve incerteza.

Exemplos:

```text
Quantas vendas teremos no próximo mês?
Qual produto vai vender mais?
Qual cliente tem maior chance de comprar?
Qual pedido tem risco de fraude?
Qual campanha deve performar melhor?
Qual produto pode acabar no estoque?
Qual cliente pode abandonar o carrinho?
Qual desconto aumenta a chance de conversão?
```

Nenhuma dessas perguntas tem resposta 100% certa.

Por isso usamos modelos probabilísticos para estimar o que pode acontecer.

---

## 4. Eventos e estimativas

Um evento é algo que pode acontecer ou não.

Exemplos de eventos em e-commerce:

```text
cliente comprar
cliente abandonar o carrinho
pedido ser fraude
produto ficar sem estoque
campanha converter
cliente clicar em promoção
cliente voltar ao site
```

Uma estimativa é uma tentativa de calcular a chance ou o valor esperado de algo.

Exemplo:

```text
Probabilidade de compra: 70%
Probabilidade de abandono: 35%
Vendas esperadas no mês: 1.200 pedidos
Receita esperada: R$ 250.000
```

---

## 5. Raciocínio probabilístico

Raciocínio probabilístico é uma forma de tomar decisões considerando incertezas.

Em vez de dizer:

```text
Esse cliente vai comprar.
```

Dizemos:

```text
Esse cliente tem 80% de chance de comprar.
```

Em vez de dizer:

```text
Esse produto vai acabar.
```

Dizemos:

```text
Existe 75% de chance desse produto acabar nos próximos 7 dias.
```

Isso ajuda a tomar decisões melhores.

---

## 6. Modelagem de incertezas

Modelar incertezas significa transformar um problema incerto em variáveis, eventos e probabilidades.

Exemplo:

```text
Problema:
Quero prever se um cliente vai comprar.

Variáveis:
- histórico de compras
- tempo no site
- clique em promoção
- valor do carrinho
- origem do tráfego
- dispositivo usado
- frequência de visitas

Evento:
- compra realizada

Resultado:
- probabilidade de compra
```

---

# Exemplo em e-commerce: previsão de vendas

Imagine que queremos prever as vendas dos próximos meses.

A pergunta é:

```text
Quantas vendas teremos nos próximos meses?
```

Como não sabemos o futuro, usamos dados históricos e distribuição de probabilidade para modelar a demanda.

Exemplo:

```text
Mês 1: 950 vendas
Mês 2: 1.020 vendas
Mês 3: 1.100 vendas
Mês 4: 1.080 vendas
Mês 5: 1.150 vendas
```

Com esses dados, podemos estimar:

```text
média de vendas
variação
tendência
sazonalidade
probabilidade de vender acima de certo valor
probabilidade de vender abaixo de certo valor
```

Resultado possível:

```text
Vendas esperadas no próximo mês: 1.180 pedidos
Intervalo provável: entre 1.050 e 1.300 pedidos
```

Isso é melhor do que dizer apenas:

```text
Acho que vai vender bem.
```

---

## 7. Quantificando incertezas

Quantificar incertezas significa transformar dúvidas em números.

Exemplo:

```text
Chance de compra: 70%
Chance de não comprar: 30%
```

Ou:

```text
Demanda esperada: 1.200 unidades
Desvio possível: 150 unidades
```

Com isso, conseguimos:

```text
prever eventos
tomar decisões
calcular riscos
planejar estoque
avaliar campanhas
priorizar clientes
reduzir perdas
```

---

# Conceitos fundamentais

---

## 8. Variáveis aleatórias

Uma variável aleatória representa um valor incerto.

Ela pode assumir diferentes valores dependendo do evento.

Exemplo:

```text
Quantidade de vendas amanhã
Número de pedidos cancelados
Número de clientes que clicaram em uma campanha
Tempo médio de entrega
Valor do carrinho
```

---

## 9. Variáveis discretas

Variáveis discretas têm valores contáveis.

Exemplo:

```text
0 vendas
1 venda
2 vendas
3 vendas
100 vendas
```

Em e-commerce:

```text
quantidade de pedidos
quantidade de produtos vendidos
número de cliques
número de clientes
número de carrinhos abandonados
```

A quantidade de vendas é um exemplo de variável discreta, porque os valores são números definidos e contáveis.

---

## 10. Variáveis contínuas

Variáveis contínuas podem assumir muitos valores dentro de um intervalo.

Exemplo:

```text
tempo no site
tempo médio de entrega
valor do pedido
temperatura
peso
distância
```

Em e-commerce:

```text
tempo médio de navegação: 3,52 minutos
valor do pedido: R$ 187,43
tempo de entrega: 4,7 dias
```

Quando lidamos com tempo médio, valor monetário ou medidas em geral, normalmente estamos lidando com variáveis contínuas.

---

## 11. Distribuições de probabilidade

Distribuição de probabilidade descreve como as chances estão distribuídas entre os possíveis valores de uma variável.

Exemplo simples:

```text
Probabilidade de vender 0 unidades: 5%
Probabilidade de vender 1 unidade: 10%
Probabilidade de vender 2 unidades: 20%
Probabilidade de vender 3 unidades: 30%
Probabilidade de vender 4 unidades: 20%
Probabilidade de vender 5 unidades: 15%
```

Isso forma uma distribuição.

---

## 12. Distribuição para demanda

Para prever demanda, podemos usar distribuições.

Exemplo:

```text
Produto X pode vender:

80 unidades com baixa probabilidade
100 unidades com probabilidade média
120 unidades com alta probabilidade
150 unidades com baixa probabilidade
```

Em vez de trabalhar com um único número fixo, trabalhamos com um intervalo provável.

Isso é importante para estoque.

---

## 13. Exemplo prático: estoque

Sem modelar incerteza:

```text
Acho que vou vender 100 unidades.
Então vou comprar 100 unidades.
```

Com modelagem de incerteza:

```text
Venda esperada: 100 unidades
Cenário baixo: 80 unidades
Cenário alto: 140 unidades
Chance de vender mais de 120 unidades: 30%
```

Agora a decisão fica melhor.

Você pode decidir:

```text
comprar 120 unidades
manter estoque de segurança
negociar reposição rápida
reduzir risco de ruptura
```

---

# Teorema de Bayes

---

## 14. O que é o Teorema de Bayes?

O Teorema de Bayes é uma forma de atualizar uma probabilidade com base em uma nova evidência.

Ele responde perguntas do tipo:

```text
Dado que o evento A aconteceu,
qual é a probabilidade do evento B acontecer?
```

Exemplo:

```text
Dado que o cliente clicou em uma promoção,
qual é a probabilidade dele comprar?
```

Ou:

```text
Dado que o pedido tem comportamento suspeito,
qual é a probabilidade dele ser fraude?
```

---

## 15. Fórmula do Teorema de Bayes

```text
P(A | B) = P(B | A) * P(A) / P(B)
```

Onde:

```text
P(A | B) = probabilidade de A acontecer dado que B aconteceu
P(B | A) = probabilidade de B acontecer dado que A aconteceu
P(A) = probabilidade inicial de A
P(B) = probabilidade inicial de B
```

---

## 16. Exemplo em e-commerce

Pergunta:

```text
Dado que um cliente clicou em uma promoção,
qual é a chance dele comprar?
```

Podemos representar assim:

```text
A = cliente comprar
B = cliente clicar em promoção
```

Queremos calcular:

```text
P(Compra | ClicouEmPromocao)
```

Ou seja:

```text
probabilidade de compra dado que o cliente clicou em uma promoção
```

Esse tipo de raciocínio é útil em sistemas que lidam com informações dinâmicas.

---

## 17. Onde Bayes aparece?

O Teorema de Bayes aparece em sistemas como:

```text
detecção de fraude
filtros de spam
recomendação de produtos
diagnóstico médico
classificação de risco
previsão de compra
análise de comportamento
sistemas de decisão
```

---

# Redes Bayesianas

---

## 18. O que são Redes Bayesianas?

Redes Bayesianas são modelos gráficos usados para representar dependências entre variáveis.

Elas ajudam a calcular probabilidades de eventos considerando várias evidências.

Exemplo:

```text
Histórico de compras influencia a chance de compra.
Tempo no site influencia a chance de compra.
Clique em promoção influencia a chance de compra.
```

Então podemos modelar:

```text
HistoricoCompras → Compra
TempoNoSite → Compra
ClicouEmPromocao → Compra
```

---

## 19. Estrutura de uma Rede Bayesiana

Uma Rede Bayesiana tem:

```text
nós
arestas
tabelas de probabilidade condicional
```

### Nós

Representam variáveis.

Exemplo:

```text
HistoricoCompras
TempoNoSite
ClicouEmPromocao
Compra
```

### Arestas

Representam relação de dependência entre variáveis.

Exemplo:

```text
HistoricoCompras → Compra
TempoNoSite → Compra
ClicouEmPromocao → Compra
```

### Tabelas de Probabilidade Condicional

Representam a probabilidade de um evento dado o estado das variáveis relacionadas.

Exemplo:

```text
Se tem histórico de compra,
passou muito tempo no site
e clicou em promoção,
então a chance de comprar é 90%.
```

---

## 20. Exemplo visual

```text
HistoricoCompras ─┐
                  │
TempoNoSite ──────┼──> Compra
                  │
ClicouPromocao ───┘
```

Aqui, a variável Compra depende de três evidências:

```text
HistoricoCompras
TempoNoSite
ClicouEmPromocao
```

---

# Exemplo prático em Python

---

## 21. Rede Bayesiana simples sem biblioteca externa

Este exemplo calcula a probabilidade de compra com base em três evidências:

```text
HistoricoCompras
TempoNoSite
ClicouEmPromocao
```

Estados usados:

```text
0 = Não
1 = Sim
```

Código:

```python
# 1. Criando as probabilidades da Rede Bayesiana

probabilidades = {
    "HistoricoCompras": {
        0: 0.7,  # 0: Não tem histórico
        1: 0.3   # 1: Tem histórico
    },

    "TempoNoSite": {
        0: 0.6,  # 0: Pouco tempo
        1: 0.4   # 1: Muito tempo
    },

    "ClicouEmPromocao": {
        0: 0.8,  # 0: Não clicou
        1: 0.2   # 1: Clicou
    },

    "Compra": {
        # (HistoricoCompras, TempoNoSite, ClicouEmPromocao): Probabilidade de compra

        (0, 0, 0): 0.1,  # Não tem histórico, pouco tempo, não clicou
        (0, 0, 1): 0.3,  # Não tem histórico, pouco tempo, clicou
        (0, 1, 0): 0.2,  # Não tem histórico, muito tempo, não clicou
        (0, 1, 1): 0.6,  # Não tem histórico, muito tempo, clicou

        (1, 0, 0): 0.4,  # Tem histórico, pouco tempo, não clicou
        (1, 0, 1): 0.7,  # Tem histórico, pouco tempo, clicou
        (1, 1, 0): 0.8,  # Tem histórico, muito tempo, não clicou
        (1, 1, 1): 0.9   # Tem histórico, muito tempo, clicou
    }
}


# 2. Função para calcular a probabilidade de compra

def calcular_probabilidade_compra(evidencias):
    historico = evidencias["HistoricoCompras"]
    tempo = evidencias["TempoNoSite"]
    promocao = evidencias["ClicouEmPromocao"]

    prob_compra = probabilidades["Compra"][(historico, tempo, promocao)]
    prob_nao_compra = 1 - prob_compra

    return {
        "Comprar": prob_compra,
        "Não Comprar": prob_nao_compra
    }


# 3. Testando com um cenário

evidencias = {
    "HistoricoCompras": 1,  # Cliente tem histórico de compras
    "TempoNoSite": 0,       # Cliente passou pouco tempo no site
    "ClicouEmPromocao": 1   # Cliente clicou em promoções
}

resultados = calcular_probabilidade_compra(evidencias)

print("Probabilidades de Compra:")

for resultado, probabilidade in resultados.items():
    print(f"{resultado}: {probabilidade:.2f}")
```

Saída esperada:

```text
Probabilidades de Compra:
Comprar: 0.70
Não Comprar: 0.30
```

Interpretação:

```text
Como o cliente tem histórico de compra,
passou pouco tempo no site
e clicou em promoção,
a estimativa de compra é 70%.
```

---

## 22. Exemplo com NumPy

```python
import numpy as np

vendas_historicas = np.array([950, 1020, 1100, 1080, 1150])

media = np.mean(vendas_historicas)
desvio = np.std(vendas_historicas)

print(f"Média de vendas: {media:.2f}")
print(f"Desvio padrão: {desvio:.2f}")

estimativa_proximo_mes = media

print(f"Estimativa para o próximo mês: {estimativa_proximo_mes:.0f} vendas")
```

Esse exemplo usa dados históricos para calcular uma estimativa simples.

---

## 23. Bibliotecas Python úteis

Algumas bibliotecas comuns para trabalhar com probabilidade, estatística e modelos probabilísticos:

```text
NumPy
SciPy
pandas
scikit-learn
pgmpy
PyMC
```

Exemplos de uso:

```text
NumPy → cálculo numérico
SciPy → estatística e distribuições
pandas → manipulação de dados
scikit-learn → modelos de Machine Learning
pgmpy → modelos gráficos probabilísticos e Redes Bayesianas
PyMC → modelagem probabilística bayesiana
```

---

# Exemplo prático em Node.js

---

## 24. Rede Bayesiana simples sem biblioteca externa

Este exemplo faz a mesma ideia do Python, mas em Node.js.

```javascript
// 1. Criando as probabilidades da Rede Bayesiana

const probabilidades = {
  HistoricoCompras: {
    0: 0.7, // 0: Não tem histórico
    1: 0.3  // 1: Tem histórico
  },

  TempoNoSite: {
    0: 0.6, // 0: Pouco tempo
    1: 0.4  // 1: Muito tempo
  },

  ClicouEmPromocao: {
    0: 0.8, // 0: Não clicou
    1: 0.2  // 1: Clicou
  },

  Compra: {
    // Chave: "HistoricoCompras,TempoNoSite,ClicouEmPromocao"
    "0,0,0": 0.1,
    "0,0,1": 0.3,
    "0,1,0": 0.2,
    "0,1,1": 0.6,

    "1,0,0": 0.4,
    "1,0,1": 0.7,
    "1,1,0": 0.8,
    "1,1,1": 0.9
  }
};


// 2. Função para calcular a probabilidade de compra

function calcularProbabilidadeCompra(evidencias) {
  const historico = evidencias.HistoricoCompras;
  const tempo = evidencias.TempoNoSite;
  const promocao = evidencias.ClicouEmPromocao;

  const chave = `${historico},${tempo},${promocao}`;

  const probCompra = probabilidades.Compra[chave];
  const probNaoCompra = 1 - probCompra;

  return {
    Comprar: probCompra,
    "Não Comprar": probNaoCompra
  };
}


// 3. Testando com um cenário

const evidencias = {
  HistoricoCompras: 1, // Cliente tem histórico de compras
  TempoNoSite: 0,      // Cliente passou pouco tempo no site
  ClicouEmPromocao: 1  // Cliente clicou em promoções
};

const resultados = calcularProbabilidadeCompra(evidencias);

console.log("Probabilidades de Compra:");

for (const [resultado, probabilidade] of Object.entries(resultados)) {
  console.log(`${resultado}: ${probabilidade.toFixed(2)}`);
}
```

Saída esperada:

```text
Probabilidades de Compra:
Comprar: 0.70
Não Comprar: 0.30
```

---

## 25. Exemplo simples de estimativa em Node.js

```javascript
const vendasHistoricas = [950, 1020, 1100, 1080, 1150];

function media(valores) {
  return valores.reduce((total, valor) => total + valor, 0) / valores.length;
}

function desvioPadrao(valores) {
  const m = media(valores);

  const variancia = valores.reduce((total, valor) => {
    return total + Math.pow(valor - m, 2);
  }, 0) / valores.length;

  return Math.sqrt(variancia);
}

const mediaVendas = media(vendasHistoricas);
const desvio = desvioPadrao(vendasHistoricas);

console.log(`Média de vendas: ${mediaVendas.toFixed(2)}`);
console.log(`Desvio padrão: ${desvio.toFixed(2)}`);
console.log(`Estimativa para o próximo mês: ${mediaVendas.toFixed(0)} vendas`);
```

---

## 26. Bibliotecas Node.js úteis

Em Node.js, você pode começar sem biblioteca externa, como nos exemplos acima.

Para projetos maiores, pode usar bibliotecas para:

```text
estatística
machine learning
manipulação de dados
probabilidade
visualização
```

Exemplos de categorias:

```text
mathjs → cálculos matemáticos e estatísticos
simple-statistics → estatística básica
danfojs-node → manipulação de dados estilo pandas
tensorflow.js → modelos de Machine Learning e redes neurais
```

---

# Aplicando isso em e-commerce

---

## 27. Caso 1: previsão de compra

Pergunta:

```text
Esse cliente vai comprar?
```

Variáveis:

```text
histórico de compras
tempo no site
clique em promoção
origem do tráfego
valor do carrinho
dispositivo
```

Resultado:

```text
Probabilidade de compra: 70%
```

Decisão:

```text
mostrar cupom
priorizar atendimento
recomendar produto
enviar lembrete
```

---

## 28. Caso 2: previsão de demanda

Pergunta:

```text
Quanto vou vender no próximo mês?
```

Variáveis:

```text
vendas históricas
sazonalidade
campanhas
estoque
preço
feriados
tendência
```

Resultado:

```text
Demanda esperada: 1.200 unidades
Intervalo provável: 1.050 a 1.350 unidades
```

Decisão:

```text
comprar mais estoque
planejar campanha
ajustar preço
negociar com fornecedor
```

---

## 29. Caso 3: risco de fraude

Pergunta:

```text
Esse pedido é suspeito?
```

Variáveis:

```text
valor do pedido
IP
país do cartão
histórico do cliente
tentativas de pagamento
endereço de entrega
tipo de produto
```

Resultado:

```text
Probabilidade de fraude: 85%
```

Decisão:

```text
segurar pedido para análise
pedir validação adicional
bloquear automaticamente
liberar se o risco for baixo
```

---

## 30. Caso 4: abandono de carrinho

Pergunta:

```text
Esse cliente vai abandonar o carrinho?
```

Variáveis:

```text
valor do frete
prazo de entrega
tempo parado no checkout
dispositivo
forma de pagamento
cupom aplicado
```

Resultado:

```text
Probabilidade de abandono: 65%
```

Decisão:

```text
mostrar incentivo
oferecer frete grátis
enviar e-mail de recuperação
simplificar checkout
```

---

# Diferença entre previsão e decisão

Previsão responde:

```text
O que pode acontecer?
```

Decisão responde:

```text
O que devo fazer com essa previsão?
```

Exemplo:

```text
Previsão:
Cliente tem 70% de chance de comprar.

Decisão:
Mostrar cupom apenas se a margem permitir.
```

Outro exemplo:

```text
Previsão:
Produto pode acabar em 7 dias.

Decisão:
Comprar mais estoque ou reduzir campanha.
```

---

# Ligação com análise preditiva e prescritiva

Modelagem de incerteza aparece muito em dois tipos de análise:

```text
Análise Preditiva
Análise Prescritiva
```

## Análise Preditiva

Usa dados para prever o que pode acontecer.

Exemplo:

```text
Prever vendas dos próximos meses.
```

## Análise Prescritiva

Usa previsões para recomendar ações.

Exemplo:

```text
Comprar mais estoque com base na previsão de demanda.
```

---

# Resumo final

Lidar com incertezas significa aceitar que nem tudo é certo, mas que podemos estimar probabilidades e tomar decisões melhores.

Em computação, precisamos transformar heurísticas humanas em modelos explícitos.

```text
Heurística humana:
Esse cliente parece ter chance de comprar.

Modelo probabilístico:
P(Compra | HistoricoCompras, TempoNoSite, ClicouEmPromocao) = 70%
```

Com isso, conseguimos:

```text
modelar eventos incertos
calcular probabilidades
prever demanda
estimar vendas
avaliar riscos
tomar decisões melhores
automatizar recomendações
```

---

# Frases para memorizar

```text
Incerteza não significa falta de controle.
Significa que precisamos trabalhar com probabilidades.
```

```text
No dia a dia usamos heurísticas implícitas.
Na computação precisamos transformar isso em variáveis, evidências e modelos.
```

```text
Raciocínio probabilístico ajuda a prever eventos e tomar decisões.
```

```text
O Teorema de Bayes atualiza probabilidades com base em novas evidências.
```

```text
Redes Bayesianas modelam dependências entre variáveis.
```

```text
Em e-commerce, incerteza aparece em vendas, estoque, fraude, demanda, campanha e comportamento do cliente.
```

---

# Mapa mental

```text
Lidando com Incertezas
│
├── Eventos incertos
│    ├── compra
│    ├── abandono
│    ├── fraude
│    └── demanda
│
├── Variáveis aleatórias
│    ├── discretas
│    └── contínuas
│
├── Distribuições de probabilidade
│    ├── vendas esperadas
│    ├── demanda provável
│    └── intervalo de incerteza
│
├── Teorema de Bayes
│    └── atualiza probabilidades com evidências
│
├── Redes Bayesianas
│    ├── nós
│    ├── arestas
│    └── tabelas de probabilidade condicional
│
└── Decisão
     ├── prever
     ├── estimar
     ├── reduzir risco
     └── agir melhor
```
