# O Raciocínio Lógico

Este README explica, de forma prática, o que são **lógicas formais** e como elas se conectam com **raciocínio lógico** em sistemas de e-commerce.

A ideia é entender como transformar regras, permissões, hipóteses e decisões em estruturas que um sistema consegue processar.

---

## 1. O que são lógicas formais?

Lógicas formais são formas estruturadas de representar raciocínio usando regras claras.

Elas ajudam a responder perguntas como:

```text
Essa regra é verdadeira ou falsa?
Esse cliente pode usar esse cupom?
Esse pedido deve ser bloqueado?
Esse produto pode aparecer para esse grupo de clientes?
Essa condição permite finalizar a compra?
```

Em computação, lógica formal é importante porque o computador não entende intuição humana.

Ele precisa de regras explícitas.

Exemplo humano:

```text
Esse pedido parece suspeito.
```

Exemplo lógico:

```text
SE valor_do_pedido > 5000
E cliente_novo = verdadeiro
E tentativas_pagamento > 3
ENTÃO pedido_suspeito = verdadeiro
```

---

## 2. Raciocínio lógico

Raciocínio lógico é o processo de chegar a uma conclusão usando informações, regras ou evidências.

Existem três tipos muito importantes:

```text
Dedutivo
Indutivo
Abdutivo
```

Cada um funciona de uma forma diferente.

---

# 3. Raciocínio Dedutivo

## O que é?

Raciocínio dedutivo é baseado em regras.

Você parte de regras gerais e aplica em um caso específico.

Se as regras forem verdadeiras e os dados estiverem corretos, a conclusão também será verdadeira.

Formato:

```text
Regra geral + caso específico = conclusão lógica
```

---

## Exemplo simples

Regra:

```text
Todo pedido acima de R$ 500 tem frete grátis.
```

Caso:

```text
Pedido do cliente é R$ 650.
```

Conclusão:

```text
Esse pedido tem frete grátis.
```

---

## Exemplo em e-commerce

Regra:

```text
SE cliente é VIP
E carrinho >= 300
ENTÃO aplicar desconto de 15%.
```

Dados:

```text
cliente_vip = verdadeiro
valor_carrinho = 450
```

Conclusão:

```text
aplicar_desconto = verdadeiro
```

Isso é dedução.

---

## Dedutivo em regras ou permissões

O raciocínio dedutivo é muito usado em permissões e regras de negócio.

Exemplos:

```text
Usuário admin pode acessar painel.
Cliente sem endereço não pode ir para pagamento.
Produto sem estoque não pode ser vendido.
Cupom expirado não pode ser aplicado.
Pedido pago pode ser faturado.
Pedido cancelado não pode ser enviado.
```

---

# 4. Raciocínio Indutivo

## O que é?

Raciocínio indutivo é quando você observa casos específicos e tenta criar uma regra geral.

Formato:

```text
vários exemplos específicos → provável regra geral
```

Ele não garante certeza absoluta.

Ele gera uma generalização provável.

---

## Exemplo simples

Observações:

```text
Cliente 1 abandonou o carrinho quando o frete passou de R$ 40.
Cliente 2 abandonou o carrinho quando o frete passou de R$ 40.
Cliente 3 abandonou o carrinho quando o frete passou de R$ 40.
```

Conclusão indutiva:

```text
Frete acima de R$ 40 pode aumentar abandono de carrinho.
```

Isso é uma generalização baseada em exemplos.

---

## Exemplo em e-commerce

Observações:

```text
Produtos com foto profissional vendem mais.
Produtos com vídeo vendem mais.
Produtos com descrição completa vendem mais.
```

Conclusão indutiva:

```text
Produtos com conteúdo mais completo tendem a converter melhor.
```

---

# 5. Raciocínio Abdutivo

## O que é?

Raciocínio abdutivo é a busca da melhor explicação possível para um conjunto de dados.

Formato:

```text
fatos observados → hipótese mais provável
```

Ele não prova com certeza.

Ele tenta encontrar a explicação mais plausível.

---

## Exemplo simples

Fatos:

```text
As vendas caíram.
O tráfego continua igual.
O abandono no checkout aumentou.
O erro aparece mais em mobile.
```

Melhor explicação possível:

```text
Provavelmente existe um problema no checkout mobile.
```

Isso é raciocínio abdutivo.

---

## Exemplo em e-commerce

Fatos:

```text
Muitos clientes entram no produto.
Poucos adicionam ao carrinho.
Preço está maior que concorrentes.
Avaliações estão baixas.
```

Hipótese abdutiva:

```text
O preço alto e as avaliações ruins podem estar reduzindo a conversão.
```

---

# 6. Diferença entre dedutivo, indutivo e abdutivo

| Tipo | Parte de quê? | Chega em quê? | Certeza? |
|---|---|---|---|
| Dedutivo | Regras gerais | Conclusão necessária | Alta, se as regras forem corretas |
| Indutivo | Exemplos específicos | Regra provável | Média/probabilística |
| Abdutivo | Fatos observados | Melhor explicação possível | Hipótese provável |

Resumo:

```text
Dedutivo = aplicar regras.
Indutivo = generalizar a partir de exemplos.
Abdutivo = encontrar a melhor explicação.
```

---

# 7. Tipos de lógicas formais

## 7.1 Lógica proposicional

Trabalha com proposições que podem ser verdadeiras ou falsas.

Exemplo:

```text
A = cliente é VIP
B = carrinho maior que R$ 300
C = aplicar desconto
```

Regra:

```text
A E B → C
```

Em linguagem comum:

```text
Se cliente é VIP e o carrinho é maior que R$ 300, então aplicar desconto.
```

---

## 7.2 Operadores lógicos

```text
E / AND
OU / OR
NÃO / NOT
SE...ENTÃO / IMPLICAÇÃO
```

Exemplo:

```text
cliente_vip AND valor_carrinho >= 300 → aplicar_desconto
```

---

## 7.3 Lógica de predicados

A lógica de predicados permite trabalhar com objetos e propriedades.

Exemplo:

```text
Cliente(Kadu)
VIP(Kadu)
CarrinhoMaiorQue300(Kadu)
```

Regra:

```text
Para todo cliente X:
SE VIP(X) E CarrinhoMaiorQue300(X)
ENTÃO TemDesconto(X)
```

Em e-commerce:

```text
Todo cliente VIP com carrinho acima de R$ 300 tem desconto.
```

---

## 7.4 Lógica fuzzy

A lógica tradicional trabalha com verdadeiro ou falso.

Mas alguns problemas têm graus.

Exemplo:

```text
cliente muito engajado
produto quase sem estoque
frete relativamente caro
risco médio de fraude
```

A lógica fuzzy permite trabalhar com valores entre 0 e 1.

Exemplo:

```text
risco_fraude = 0.75
engajamento_cliente = 0.82
frete_caro = 0.60
```

Isso é útil quando não queremos apenas sim ou não.

---

# 8. Exemplo dedutivo em Python

```python
def pode_aplicar_desconto(cliente_vip, valor_carrinho):
    if cliente_vip and valor_carrinho >= 300:
        return True
    return False

cliente_vip = True
valor_carrinho = 450

if pode_aplicar_desconto(cliente_vip, valor_carrinho):
    print("Aplicar desconto de 15%")
else:
    print("Não aplicar desconto")
```

Saída esperada:

```text
Aplicar desconto de 15%
```

Explicação:

```text
A regra foi aplicada diretamente.
Isso é raciocínio dedutivo.
```

---

# 9. Exemplo dedutivo em Node.js

```javascript
function podeAplicarDesconto(clienteVip, valorCarrinho) {
  return clienteVip && valorCarrinho >= 300;
}

const clienteVip = true;
const valorCarrinho = 450;

if (podeAplicarDesconto(clienteVip, valorCarrinho)) {
  console.log("Aplicar desconto de 15%");
} else {
  console.log("Não aplicar desconto");
}
```

---

# 10. Exemplo indutivo em Python

Neste exemplo, observamos vários pedidos abandonados e tentamos encontrar um padrão.

```python
pedidos = [
    {"frete": 45, "abandonou": True},
    {"frete": 50, "abandonou": True},
    {"frete": 42, "abandonou": True},
    {"frete": 20, "abandonou": False},
    {"frete": 18, "abandonou": False},
]

abandonos_com_frete_alto = 0
total_frete_alto = 0

for pedido in pedidos:
    if pedido["frete"] >= 40:
        total_frete_alto += 1
        if pedido["abandonou"]:
            abandonos_com_frete_alto += 1

proporcao = abandonos_com_frete_alto / total_frete_alto

print(f"Abandono com frete alto: {proporcao:.0%}")

if proporcao > 0.7:
    print("Hipótese: frete alto aumenta abandono de carrinho")
```

Saída esperada:

```text
Abandono com frete alto: 100%
Hipótese: frete alto aumenta abandono de carrinho
```

Explicação:

```text
O sistema olhou exemplos específicos e criou uma hipótese geral.
Isso é raciocínio indutivo.
```

---

# 11. Exemplo indutivo em Node.js

```javascript
const pedidos = [
  { frete: 45, abandonou: true },
  { frete: 50, abandonou: true },
  { frete: 42, abandonou: true },
  { frete: 20, abandonou: false },
  { frete: 18, abandonou: false }
];

let abandonosComFreteAlto = 0;
let totalFreteAlto = 0;

for (const pedido of pedidos) {
  if (pedido.frete >= 40) {
    totalFreteAlto++;

    if (pedido.abandonou) {
      abandonosComFreteAlto++;
    }
  }
}

const proporcao = abandonosComFreteAlto / totalFreteAlto;

console.log(`Abandono com frete alto: ${(proporcao * 100).toFixed(0)}%`);

if (proporcao > 0.7) {
  console.log("Hipótese: frete alto aumenta abandono de carrinho");
}
```

---

# 12. Exemplo abdutivo em Python

Neste exemplo, temos sintomas do problema e buscamos a melhor explicação.

```python
def diagnosticar_queda_vendas(dados):
    hipoteses = []

    if dados["trafego"] == "normal" and dados["conversao"] == "baixa":
        hipoteses.append("Problema na experiência de compra")

    if dados["abandono_checkout"] == "alto" and dados["erros_mobile"] == "alto":
        hipoteses.append("Possível problema no checkout mobile")

    if dados["produto_sem_estoque"]:
        hipoteses.append("Produtos importantes podem estar sem estoque")

    if dados["frete"] == "alto":
        hipoteses.append("Frete alto pode estar reduzindo conversão")

    return hipoteses


dados = {
    "trafego": "normal",
    "conversao": "baixa",
    "abandono_checkout": "alto",
    "erros_mobile": "alto",
    "produto_sem_estoque": False,
    "frete": "normal"
}

hipoteses = diagnosticar_queda_vendas(dados)

print("Possíveis explicações:")
for h in hipoteses:
    print(f"- {h}")
```

Saída esperada:

```text
Possíveis explicações:
- Problema na experiência de compra
- Possível problema no checkout mobile
```

Explicação:

```text
O sistema não provou a causa.
Ele sugeriu as explicações mais prováveis com base nos dados.
Isso é raciocínio abdutivo.
```

---

# 13. Exemplo abdutivo em Node.js

```javascript
function diagnosticarQuedaVendas(dados) {
  const hipoteses = [];

  if (dados.trafego === "normal" && dados.conversao === "baixa") {
    hipoteses.push("Problema na experiência de compra");
  }

  if (dados.abandonoCheckout === "alto" && dados.errosMobile === "alto") {
    hipoteses.push("Possível problema no checkout mobile");
  }

  if (dados.produtoSemEstoque) {
    hipoteses.push("Produtos importantes podem estar sem estoque");
  }

  if (dados.frete === "alto") {
    hipoteses.push("Frete alto pode estar reduzindo conversão");
  }

  return hipoteses;
}

const dados = {
  trafego: "normal",
  conversao: "baixa",
  abandonoCheckout: "alto",
  errosMobile: "alto",
  produtoSemEstoque: false,
  frete: "normal"
};

const hipoteses = diagnosticarQuedaVendas(dados);

console.log("Possíveis explicações:");
for (const h of hipoteses) {
  console.log(`- ${h}`);
}
```

---

# 14. Casos práticos para e-commerce

Esses casos podem ser usados como exercícios.

---

## Caso 1: cupom de desconto

Regra:

```text
Cliente VIP com carrinho acima de R$ 300 recebe 15% de desconto.
```

Dados:

```text
cliente_vip = verdadeiro
valor_carrinho = 420
```

Pergunta:

```text
O desconto deve ser aplicado?
```

Tipo de raciocínio:

```text
Dedutivo
```

---

## Caso 2: frete grátis

Regra:

```text
Pedidos acima de R$ 199 têm frete grátis.
```

Dados:

```text
valor_carrinho = 180
```

Pergunta:

```text
O cliente tem direito a frete grátis?
```

Tipo de raciocínio:

```text
Dedutivo
```

---

## Caso 3: abandono por frete alto

Observações:

```text
80% dos clientes abandonaram o carrinho quando o frete passou de R$ 40.
```

Pergunta:

```text
Podemos generalizar que frete alto aumenta abandono?
```

Tipo de raciocínio:

```text
Indutivo
```

---

## Caso 4: queda de vendas

Fatos:

```text
Vendas caíram 30%.
Tráfego continua igual.
Checkout mobile começou a apresentar erro.
Abandono no pagamento aumentou.
```

Pergunta:

```text
Qual a melhor explicação possível?
```

Tipo de raciocínio:

```text
Abdutivo
```

Resposta provável:

```text
Problema no checkout mobile.
```

---

## Caso 5: produto sem conversão

Fatos:

```text
Produto tem muitas visitas.
Poucos clientes adicionam ao carrinho.
Preço está acima dos concorrentes.
Avaliações são ruins.
```

Pergunta:

```text
Qual hipótese explica a baixa conversão?
```

Tipo de raciocínio:

```text
Abdutivo
```

Possíveis explicações:

```text
Preço alto.
Baixa confiança por causa das avaliações.
Descrição ou fotos podem não estar boas.
```

---

## Caso 6: recomendação de produto

Observações:

```text
Clientes que compram notebook também compram mouse e mochila.
```

Pergunta:

```text
Quando um cliente colocar notebook no carrinho, o que recomendar?
```

Tipo de raciocínio:

```text
Indutivo
```

Resposta provável:

```text
Mouse, mochila, teclado ou suporte.
```

---

## Caso 7: bloqueio de pedido suspeito

Regra:

```text
SE valor do pedido > R$ 5000
E cliente é novo
E tentativas de pagamento > 3
ENTÃO enviar para análise antifraude.
```

Dados:

```text
valor_pedido = 6200
cliente_novo = verdadeiro
tentativas_pagamento = 4
```

Pergunta:

```text
O pedido deve ir para análise?
```

Tipo de raciocínio:

```text
Dedutivo
```

---

## Caso 8: problema de estoque

Fatos:

```text
Muitos clientes buscam o produto.
A página recebe visitas.
O botão comprar não aparece.
O produto está com estoque zerado.
```

Pergunta:

```text
Qual a melhor explicação?
```

Tipo de raciocínio:

```text
Abdutivo
```

Resposta provável:

```text
Produto sem estoque está impedindo compra.
```

---

## Caso 9: campanha performando bem

Observações:

```text
Campanhas com vídeo tiveram conversão maior.
Campanhas com imagem simples tiveram conversão menor.
Campanhas com prova social venderam mais.
```

Pergunta:

```text
Que regra podemos inferir?
```

Tipo de raciocínio:

```text
Indutivo
```

Resposta provável:

```text
Campanhas com vídeo e prova social tendem a converter melhor.
```

---

## Caso 10: acesso ao painel admin

Regra:

```text
Apenas usuários com perfil admin podem acessar configurações da loja.
```

Dados:

```text
usuario_perfil = editor
```

Pergunta:

```text
Esse usuário pode acessar configurações?
```

Tipo de raciocínio:

```text
Dedutivo
```

Resposta:

```text
Não.
```

---

# 15. Exercício guiado

Escolha um caso e classifique:

```text
1. É dedutivo, indutivo ou abdutivo?
2. Quais são as regras ou evidências?
3. Qual é a conclusão?
4. A conclusão é certeza ou hipótese?
5. Como isso poderia virar código?
```

Exemplo:

```text
Caso:
Muitos clientes abandonam o carrinho quando o frete passa de R$ 40.

Tipo:
Indutivo.

Evidências:
Vários casos específicos de abandono com frete alto.

Conclusão:
Frete alto provavelmente aumenta abandono.

Certeza?
Não. É uma hipótese provável.
```

---

# 16. Resumo final

```text
Lógicas formais ajudam a transformar raciocínio em regras claras.
```

```text
Raciocínio dedutivo aplica regras gerais em casos específicos.
```

```text
Raciocínio indutivo cria generalizações a partir de exemplos.
```

```text
Raciocínio abdutivo busca a melhor explicação possível para os dados.
```

Em e-commerce, esses raciocínios aparecem em:

```text
cupons
frete grátis
permissões
antifraude
recomendação
estoque
checkout
campanhas
precificação
análise de conversão
```

---

# 17. Mapa mental

```text
Lógicas Formais
│
├── Lógica proposicional
│    ├── verdadeiro/falso
│    ├── AND / OR / NOT
│    └── regras simples
│
├── Lógica de predicados
│    ├── objetos
│    ├── propriedades
│    └── relações
│
├── Lógica fuzzy
│    ├── graus de verdade
│    ├── risco médio
│    └── cliente muito engajado
│
└── Raciocínio lógico
     ├── Dedutivo
     │    └── aplica regras
     ├── Indutivo
     │    └── generaliza exemplos
     └── Abdutivo
          └── busca melhor explicação
```
