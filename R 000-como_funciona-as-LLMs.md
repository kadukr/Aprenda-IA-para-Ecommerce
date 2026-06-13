# Como Funciona as LLMs

## LLMs

LLM é uma **tecnologia**, precisamente é um tipo de modelo de IA e significa **Large Language Model**.

São modelos treinados com muito texto para entender e gerar linguagem

Exemplos de LLMs: GPT, Claude, Gemini, Llama, Mistral, etc...

A ideia central é:

> Um LLM aprende padrões da linguagem e tenta prever o próximo token mais provável dentro de um contexto.

Token pode ser uma palavra, pedaço de palavra, símbolo ou caractere.

**Exemplo:**

Magento é uma plataforma de...

O modelo pode prever:

> e-commerce

Então, de forma simples:

> LLM = **modelo de IA treinado para entender e gerar linguagem.**

---

## NLP
Natural Language Processing (Processamento de Linguagem Natural)

É a área da IA que estuda como computadores podem entender, interpretar, processar e gerar linguagem humana.

Linguagem humana pode ser:

```text
texto
fala
perguntas
respostas
documentos
mensagens
e-mails
tickets
conversas
```

__NLP__ = área/problema\
__LLM__ = tecnologia/modelo usado hoje para resolver muitos problemas de NLP

Ou seja:

__NLP__ é o campo.\
__LLM__ é uma ferramenta moderna dentro desse campo.

Exemplos de tarefas de NLP

Antes dos LLMs, NLP já existia para tarefas como:

```text
tradução automática
análise de sentimento
classificação de texto
extração de entidades
correção ortográfica
resumo de texto
chatbots
busca semântica
resposta a perguntas
```
---

## Transformer

O Transformer é a **arquitetura neural** mais usada para construir LLMs modernos

LLM = o produto/modelo final

Transformer = a arquitetura/cérebro usado por trás

Em comparação:

```text
Carro = LLM
Motor = Transformer
```

O Transformer foi revolucionário porque **consegue olhar para várias partes do texto ao mesmo tempo** e entender quais palavras são mais importantes para responder.

Antes dele, muitos modelos liam texto mais “em sequência”, palavra por palavra. O Transformer consegue analisar o contexto inteiro com muito mais eficiência.

### O que o Transformer faz?

Ele pega uma frase, **divide em tokens**, transforma esses tokens em números e **calcula relações** entre eles.

**Exemplo:**

> O gato subiu no telhado porque ele estava assustado.

O modelo LLM precisa entender que "ele" provavelmente se refere ao gato, não ao telhado.

O Transformer faz isso usando um mecanismo chamado Attention ou em português Atenção.

---

### O que é Attention?

Attention é o **mecanismo que permite ao modelo decidir**:

> “Quais partes do texto são importantes para entender este token?”

**Exemplo:**

> A senha do cliente não funciona porque ele esqueceu o e-mail.

Para entender "ele", o modelo presta mais atenção em *cliente* e menos atenção em *senha*, então **attention é tipo um sistema de foco**.

---

## Multi-head Attention?

Multi-head Attention significa Atenção de Múltiplas Cabeças.

É como se o modelo tivesse várias “cabeças” olhando para a mesma frase, mas cada uma focando em coisas diferentes.

**Exemplo:**

> O cliente comprou o produto porque ele estava em promoção.

Uma cabeça pode focar em:

```text
cliente → comprou
```

Outra cabeça pode focar em:

```text
produto → promoção
```

Outra pode focar em:

```text
ele → produto
```

Outra pode focar na estrutura gramatical da frase.

Então:

**Single-head attention = uma análise de atenção**

**Multi-head attention = várias análises de atenção em paralelo**

Isso deixa o modelo muito mais poderoso, porque ele não entende a frase por um único ângulo. Ele entende várias relações ao mesmo tempo.

---

### Hierarquia como o modelo é construído

```text
IA
 └── Machine Learning
      └── Deep Learning
           └── Redes Neurais
                └── Transformer
                     └── LLM

```

---

## IA Generativa

É uma área de Machine Learning onde modelos aprendem padrões em dados gigantes e depois conseguem gerar conteúdo parecido com conteúdo humano.

Esse conteúdo pode ser:

```text
texto
imagem
vídeo
áudio
fala
código
```

__IA Generativa é parte de Machine Learning__\
Generative AI é um subconjunto do Machine Learning tradicional.

Ou seja:

LLM não é uma coisa isolada.\
LLM é um tipo de modelo dentro de IA Generativa, que por sua vez está dentro de Machine Learning.

---

### Hierarquia o que o modelo faz

```text
IA
 └── Machine Learning
      └── Generative AI
           └── Large Language Models
```
---

### Como esses modelos aprendem?

Os modelos aprendem encontrando __padrões estatísticos__ em quantidades absurdas de dados.\
LLMs, eles foram treinados com:

```text
trilhões de palavras
semanas ou meses de treinamento
muito poder computacional
bilhões de parâmetros
```

Então o modelo não “decorou” tudo como um banco de dados comum.

Ele aprendeu padrões como:

```text
quais palavras costumam aparecer juntas
como frases são estruturadas
como perguntas são respondidas
como código costuma ser escrito
como resumir textos
como seguir instruções
```
---

## Foundation Models / Base Models

São __modelos grandes já treinados__ que servem como base para várias aplicações.

Exemplos:
```text
GPT
Claude
Gemini
Llama
Mistral
Flan-T5
```

---

## Parâmetros do modelo

São os __“pesos internos”__ aprendidos durante o treinamento. É como se fossem a memória/capacidade interna do modelo.

Exemplo:

```text
1 bilhão de parâmetros
7 bilhões de parâmetros
30 bilhões de parâmetros
70 bilhões de parâmetros
100+ bilhões de parâmetros
```

Quanto mais parâmetros, geralmente mais capacidade o modelo pode ter.\
Mas isso não significa que sempre o maior é melhor para tudo.

---

## Parâmetros de geração

Exemplo:

```text
temperature
top-p
max tokens
frequency penalty
presence penalty
```

Pode ser ajustado na hora de usar o modelo, então tem dois tipos de “parâmetros” que aparecem no estudo:

__Parâmetros do modelo__ = pesos internos treinados\
__Parâmetros de geração__ = configurações usadas na resposta

---

## Propriedades emergentes

Modelos grandes começam a mostrar __emergent properties__.

Isso significa: capacidades que aparecem quando o modelo fica grande o suficiente, mesmo que ele não tenha sido treinado diretamente só para aquilo.

Exemplos:

```text
raciocinar em etapas
quebrar tarefas complexas
resolver problemas
seguir instruções
resumir
traduzir
gerar código
classificar texto
```

É como se, ao aprender muita linguagem, o modelo também aprendesse estruturas de pensamento e solução de problemas.

---

## Prompt

Com LLM, você pode passar uma instrução em linguagem natural.

Exemplo:

```text
Explique o que é RAG como se eu fosse desenvolvedor Magento.
```

Princípios:

```text
- Ter Clareza das instruções.
- Dividir tarefas complexas em subtarefas menores.
- Pedir para o modelo explicar seus passos antes de dar a resposta.
- Pedir para o modelo dar justificativas de suas respostas.
- Gerar vã́rias respostas diferentes epedir para o modelo escolher a melhor.
```

---

## Context Window

É o “espaço de memória temporária” que o modelo consegue considerar naquela conversa ou requisição.

Dentro dessa janela entram coisas como:

```text
sua pergunta
histórico recente
documentos enviados
instruções do sistema
exemplos
respostas anteriores
```

Se passar do limite, o modelo começa a perder ou cortar partes antigas.

---

## Completion

É a saída do modelo exemplo:

Prompt:
```text
Magento é uma plataforma de...
```

Completion:
```text
e-commerce usada para criar lojas virtuais.
```

O modelo completa o texto baseado no que ele acha mais provável.

---

## Inference

É ato de usar o modelo para gerar uma resposta exemplo:

```text
Treinamento = criar ou ajustar o modelo
Inferência = mandar um prompt e receber uma resposta
```

Quando você usa ChatGPT, Claude ou Gemini, você está fazendo inferência.

---

## Fine-tuning
É quando você pega um modelo já treinado, tipo um LLM pronto, e faz um treinamento adicional com dados específicos para ele ficar melhor em uma tarefa ou estilo.

Exemplo:

Modelo base sabe linguagem geral:\
GPT / Llama / Flan-T5

Mas você quer que ele fique bom em:
```text
resumir tickets de suporte
classificar reclamações
responder no tom da empresa
gerar descrições de produtos
identificar tipo de problema em pedido Magento
```

Aí você monta um dataset com exemplos:

```text
Entrada:
Cliente disse: "meu pedido não chegou e o rastreio não atualiza"

Saída esperada:
Categoria: problema_entrega
Prioridade: alta
Resposta sugerida: Olá, vamos verificar o rastreio...
```

## Tipos comuns de fine-tuning
### 1. Full fine-tuning

Treina muitos ou todos os pesos do modelo.\
É mais pesado, caro e exige mais infraestrutura.

```text
Mais poderoso
Mais caro
Mais arriscado
```
### 2. PEFT

Parameter Efficient Fine-Tuning

É um fine-tuning mais leve.\
Ele não altera o modelo inteiro. Ajusta só uma parte pequena.

Uma técnica famosa dentro disso é: LoRA

Vantagem:
```text
mais barato
mais rápido
menos GPU
mais fácil de testar
```

Por isso aparece muito em curso moderno de LLM.

### 3. Instruction fine-tuning

É treinar o modelo com exemplos de instrução e resposta.

Exemplo:
```text
Instrução:
Resuma o texto abaixo em 3 tópicos.

Resposta esperada:
- ...
- ...
- ...
```
Isso ensina o modelo a seguir comandos melhor.\
Muitos modelos chat passaram por esse tipo de ajuste.

---

## RAG
Retrieval-Augmented Generation, ou Geração Aumentada por Recuperação

Você usa quando quer que o modelo consulte informação externa.

Exemplo:

```text
política de troca
manual do sistema
documentação Magento
dados de pedido
FAQ da empresa
```

O modelo não precisa decorar isso. Ele busca a informação e responde.

RAG = dar conhecimento externo na hora da resposta

---

## Resumo

- __LLM__
= Modelo grande de linguagem, tipo GPT, Claude, Gemini.


- __Transformer__
= Arquitetura usada para criar a maioria dos LLMs modernos.


- __Attention__
= Mecanismo que decide quais partes do texto importam mais.


- __Multi-head Attention__
= Várias atenções funcionando em paralelo, cada uma olhando uma relação diferente no texto.


- __Generative AI__\
IA que gera conteúdo novo.


- __Foundation Model / Base Model__\
modelo grande pré-treinado usado como base.


- __Parameters__\
pesos internos do modelo, tipo a capacidade/memória aprendida.


- __Prompt__\
texto/instrução que você manda para o modelo.


- __Context Window__\
espaço que o modelo consegue considerar de uma vez.


- __Completion__\
resposta/texto gerado pelo modelo.


- __Inference__\
ato de usar o modelo para gerar uma resposta.


- __Fine-tuning__\
adaptar um modelo pronto para um uso específico.