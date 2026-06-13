# Outros Modelos Probabilísticos: Cadeias de Markov, Redes de Markov e Inferência

Este README é uma introdução curta sobre outros modelos usados para lidar com incertezas, prever comportamentos e tomar decisões.

Aqui vamos falar de:

```text
Cadeias de Markov
Propriedade de Markov
Redes de Markov
Inferência
Sistemas de recomendação
Exemplos em e-commerce
```

A ideia principal é:

> Usamos modelos probabilísticos quando queremos tomar decisões ou fazer previsões mesmo sem ter certeza absoluta.

---

## 1. Por que estudar esses modelos?

Em muitos problemas reais, não temos certeza absoluta do que vai acontecer.

Exemplos em e-commerce:

```text
O cliente vai comprar?
O cliente vai abandonar o carrinho?
Qual produto ele pode querer ver depois?
Qual item devo recomendar?
Qual etapa do checkout está causando perda?
```

Esses problemas envolvem incerteza.

Por isso usamos modelos probabilísticos para estimar o que pode acontecer.

---

# 2. Cadeias de Markov

## O que é?

Uma Cadeia de Markov é um modelo usado para representar um sistema que muda de estado ao longo do tempo.

A ideia principal é:

> O próximo estado de um sistema depende apenas do seu estado atual.

Isso é chamado de **Propriedade de Markov**.

---

## 3. Propriedade de Markov

A Propriedade de Markov diz:

```text
O futuro depende do presente, não de todo o passado.
```

Ou seja:

```text
Próximo estado = depende apenas do estado atual
```

Exemplo:

```text
Se o cliente está no carrinho agora,
a próxima ação mais provável depende principalmente desse estado atual.
```

Ele pode:

```text
ir para o checkout
voltar para o produto
abandonar o site
finalizar a compra
```

---

# 4. Exemplo em e-commerce

Imagine uma jornada simples de compra:

```text
Home
Categoria
Produto
Carrinho
Checkout
Compra
Abandono
```

Uma Cadeia de Markov tenta estimar a probabilidade de o cliente sair de um estado e ir para outro.

Exemplo:

```text
Home → Categoria: 50%
Home → Produto: 30%
Home → Abandono: 20%

Produto → Carrinho: 30%
Produto → Categoria: 20%
Produto → Abandono: 50%

Carrinho → Checkout: 60%
Carrinho → Produto: 10%
Carrinho → Abandono: 30%

Checkout → Compra: 70%
Checkout → Abandono: 30%
```

Com isso, conseguimos entender melhor a jornada do cliente.

---

## 5. Análise simplificada dos problemas

Cadeias de Markov simplificam problemas complexos.

Em vez de analisar todo o histórico do cliente, analisamos o estado atual.

Exemplo:

```text
Estado atual: Carrinho
```

A partir disso, estimamos os próximos estados:

```text
Checkout: 60%
Produto: 10%
Abandono: 30%
```

Isso ajuda a responder:

```text
Qual a próxima ação provável?
Onde o cliente mais abandona?
Qual etapa precisa melhorar?
```

---

# 6. Tutorial simples em Python

```python
transicoes = {
    "Home": {
        "Categoria": 0.5,
        "Produto": 0.3,
        "Abandono": 0.2
    },
    "Categoria": {
        "Produto": 0.6,
        "Home": 0.2,
        "Abandono": 0.2
    },
    "Produto": {
        "Carrinho": 0.3,
        "Categoria": 0.2,
        "Abandono": 0.5
    },
    "Carrinho": {
        "Checkout": 0.6,
        "Produto": 0.1,
        "Abandono": 0.3
    },
    "Checkout": {
        "Compra": 0.7,
        "Abandono": 0.3
    }
}

estado_atual = "Carrinho"

print(f"Estado atual: {estado_atual}")
print("Próximos estados possíveis:")

for proximo_estado, probabilidade in transicoes[estado_atual].items():
    print(f"{proximo_estado}: {probabilidade:.0%}")
```

Saída esperada:

```text
Estado atual: Carrinho
Próximos estados possíveis:
Checkout: 60%
Produto: 10%
Abandono: 30%
```

Interpretação:

```text
Se o cliente está no carrinho,
a chance maior é ele ir para o checkout.

Mas ainda existe 30% de chance de abandono.
```

---

# 7. Exemplo simples em Node.js

```javascript
const transicoes = {
  Home: {
    Categoria: 0.5,
    Produto: 0.3,
    Abandono: 0.2
  },
  Categoria: {
    Produto: 0.6,
    Home: 0.2,
    Abandono: 0.2
  },
  Produto: {
    Carrinho: 0.3,
    Categoria: 0.2,
    Abandono: 0.5
  },
  Carrinho: {
    Checkout: 0.6,
    Produto: 0.1,
    Abandono: 0.3
  },
  Checkout: {
    Compra: 0.7,
    Abandono: 0.3
  }
};

const estadoAtual = "Carrinho";

console.log(`Estado atual: ${estadoAtual}`);
console.log("Próximos estados possíveis:");

for (const [proximoEstado, probabilidade] of Object.entries(transicoes[estadoAtual])) {
  console.log(`${proximoEstado}: ${(probabilidade * 100).toFixed(0)}%`);
}
```

---

# 8. Redes de Markov

## O que são?

Redes de Markov são modelos probabilísticos usados para representar dependências entre múltiplas variáveis simultaneamente.

Enquanto a Cadeia de Markov olha uma sequência de estados, a Rede de Markov olha várias variáveis ao mesmo tempo.

Exemplo:

```text
Preço
Frete
Prazo
Estoque
Cupom
Histórico do cliente
Compra
```

Essas variáveis podem influenciar umas às outras.

---

## 9. Diferença entre Cadeia de Markov e Rede de Markov

```text
Cadeia de Markov:
modela transições entre estados ao longo do tempo.

Rede de Markov:
modela dependências entre várias variáveis ao mesmo tempo.
```

Exemplo de Cadeia de Markov:

```text
Home → Produto → Carrinho → Checkout → Compra
```

Exemplo de Rede de Markov:

```text
Preço ─────┐
Frete ─────┤
Cupom ─────┼── Compra
Estoque ───┤
Histórico ─┘
```

---

# 10. Aplicação mais complexa em e-commerce

Imagine que queremos estimar a chance de compra considerando várias variáveis:

```text
Preço
Frete
Prazo de entrega
Estoque
Histórico de compras
Tempo no site
Cupom aplicado
Dispositivo usado
```

Exemplos de dependências:

```text
Frete alto reduz chance de compra.
Cupom aumenta chance de compra.
Histórico de compra aumenta confiança.
Estoque baixo pode acelerar a decisão.
Prazo longo pode reduzir conversão.
Mobile ruim pode aumentar abandono.
```

Uma Rede de Markov ajuda a modelar essas relações simultâneas.

---

# 11. Inferência

## O que é inferência?

Inferência é o processo de calcular uma conclusão provável a partir de evidências.

Exemplo:

```text
Evidências:
- cliente tem histórico de compra
- está no carrinho
- clicou em promoção
- frete está baixo

Inferência:
- probabilidade de compra é alta
```

Inferência não é certeza.

É uma conclusão provável com base nos dados disponíveis.

---

## Exemplo de inferência em e-commerce

Pergunta:

```text
Dado que o cliente está no carrinho e clicou em promoção,
qual é a chance dele comprar?
```

Evidências:

```text
EstadoAtual = Carrinho
ClicouEmPromocao = Sim
HistoricoCompras = Sim
Frete = Baixo
```

Resultado possível:

```text
Probabilidade de compra: 78%
Probabilidade de abandono: 22%
```

Decisão:

```text
não dar desconto extra
mostrar prazo de entrega
destacar botão de finalizar compra
```

---

# 12. Sistema de recomendação

Um sistema de recomendação tenta responder:

```text
Qual produto devo mostrar para esse cliente?
```

Ele pode usar vários sinais:

```text
produtos visitados
produtos comprados
categorias vistas
itens no carrinho
histórico de busca
clientes parecidos
produtos parecidos
estado atual da navegação
```

---

## 13. Casos de recomendação em e-commerce

### Caso 1: recomendação por produto visitado

Cliente visualizou:

```text
Tênis de corrida
```

Sistema recomenda:

```text
meias esportivas
garrafa de água
short de corrida
camiseta dry fit
```

---

### Caso 2: recomendação por carrinho

Carrinho atual:

```text
Notebook
```

Sistema recomenda:

```text
mouse
mochila
suporte
teclado
garantia estendida
```

---

### Caso 3: recomendação por comportamento

Cliente navega muito em:

```text
produtos fitness
suplementos
roupas esportivas
```

Sistema recomenda:

```text
novidades fitness
kits promocionais
produtos mais vendidos da categoria
```

---

### Caso 4: recomendação por clientes parecidos

Cliente A comprou:

```text
Produto X
Produto Y
Produto Z
```

Cliente B comprou:

```text
Produto X
Produto Y
```

Sistema pode recomendar para o Cliente B:

```text
Produto Z
```

---

# 14. Ligando Markov com recomendação

Cadeias de Markov também podem ajudar em recomendação.

Exemplo:

```text
Se muitos clientes fazem:

Produto A → Produto B → Produto C
```

Então, quando um cliente está no Produto B, o sistema pode recomendar:

```text
Produto C
```

Exemplo:

```text
Cliente viu: Camiseta
Depois viu: Calça
Depois comprou: Tênis
```

Se outro cliente viu Camiseta e Calça, o sistema pode recomendar Tênis.

---

# 15. Exemplo simples de recomendação por transição

```python
transicoes_produtos = {
    "Camiseta": {
        "Calça": 0.4,
        "Tênis": 0.3,
        "Boné": 0.3
    },
    "Calça": {
        "Tênis": 0.5,
        "Cinto": 0.3,
        "Camiseta": 0.2
    },
    "Notebook": {
        "Mouse": 0.4,
        "Mochila": 0.3,
        "Teclado": 0.3
    }
}

produto_atual = "Calça"

recomendacoes = transicoes_produtos[produto_atual]

print(f"Produto atual: {produto_atual}")
print("Recomendações:")

for produto, probabilidade in recomendacoes.items():
    print(f"{produto}: {probabilidade:.0%}")
```

Saída esperada:

```text
Produto atual: Calça
Recomendações:
Tênis: 50%
Cinto: 30%
Camiseta: 20%
```

Interpretação:

```text
Quem está vendo Calça tem maior chance de se interessar por Tênis.
```

---

# 16. Resumo final

```text
Cadeia de Markov:
o próximo estado depende apenas do estado atual.

Propriedade de Markov:
o futuro depende do presente, não de todo o passado.

Rede de Markov:
modela dependências entre múltiplas variáveis simultaneamente.

Inferência:
calcula uma conclusão provável com base em evidências.

Sistema de recomendação:
usa dados e probabilidades para sugerir produtos, conteúdos ou ações.
```

---

# 17. Mapa mental

```text
Modelos probabilísticos
│
├── Cadeias de Markov
│    ├── estados
│    ├── transições
│    └── próximo estado depende do atual
│
├── Redes de Markov
│    ├── múltiplas variáveis
│    ├── dependências simultâneas
│    └── problemas mais complexos
│
├── Inferência
│    ├── evidências
│    ├── probabilidades
│    └── conclusão provável
│
└── Recomendação
     ├── produtos visitados
     ├── compras anteriores
     ├── clientes parecidos
     └── próxima melhor sugestão
```
