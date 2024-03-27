# Compiladores
## Visão Geral - Arquitetura de compiladores

- [O compilador](#o-compilador)
- [Tabela de símbolos](#tabela-de-símbolos)
- [Fases de análise/front-end](#fases-de-análisefront-end)
  - [Análise léxica](#análise-léxica)
  - [Análise sintática](#análise-sintática)
  - [Análise semântica](#análise-semântica)
- [Fases de síntese/back-end](#fases-de-sínteseback-end)
  - [Geração de código intermediário](#geração-de-código-intermediário)
  - [Otimização de código](#otimização-de-código)
  - [Geração de código](#geração-de-código)


### O compilador
#### Até agora...
<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img01.png">

<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img02.png">


#### Fatores que capacitam o processo de compilação
1. Formalismo - a estrutura do texto é conhecida;
2. A semântica do texto é descrita em termos dessa estrutura;
3. Exemplo: estrutura de repetição
```c
while l < 100 do l := l + 1>
```

<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img03.png">

#### Como funciona cada etapa de processamento?
* Utilizaremos como o exemplo do livro abaixo.
* Cada etapa será estudada separadamente, o objetivo do exemplo é ter uma visão geral do processo.

<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img04.png">

### Tabela de símbolos
* Estrutura de dados contendo um registro para cada nome de variável com campos para seus atributos.
* Os atributos, dependente do projeto do compilador, podem ser:
1. Espaço alocado para um nome de variável;
2. Tipo;
3. Escopo;
4. Se for nome de procedimento
    * Quantidade e tipos dos argumentos
    * Tipo de retorno
    * Método de passagem: valor/referência.

<hr/>
<hr/>
<hr/>

### Fases de análise

#### Análise léxica
#### Conceitos fundamentais - Análise (Front-end):
```Análise Léxica (scanner)```: é o processo de conversão de uma sequência de caracteres em uma sequência de tokens. Um token é uma string de caracteres que é tratada como uma unidade lógica. Por exemplo, em uma linguagem de programação, palavras-chave, identificadores, constantes e símbolos de operação são tokens.

<u>Exemplo</u>:
Código-fonte: int a = 5;
<br/>
<u>Tokens</u>: 'int', 'a', '=', '5', ';'

<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img05.png">

* Também chamado de scanner;
* Separa sequências de caracteres em entidades e as classifica
* Para cada sequência lidada é gerado, de maneira geral, um par <classificação, valor>. Valor neste exemplo pode ser o endereço de memória ou a própria sequẽncia de caracteres.

<hr/>

#### Análise sintática
```Análise Sintática (parser)```: é o processo de análise de uma sequência de tokens para determinar sua estrutura gramatical com respeito a uma dada gramática formal. Esta etapa verifica se a sequência de tokens pode ser gerada pela gramática da linguagem de programação, geralmente representada por uma gramática livre de contexto.

<u>Exemplo</u>:
<br/><u>Código-fonte</u>: if (a > b) c = 1;
<br/><u>Árvore Sintática</u>:<br/>
```
        if
       / | \
      /  |  \
     a   >   b
    / \      |
   c   =     1
```

<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img06.png">

* Também chamado de parser
* Recebe as entidades classificadas do analisador léxico e os agrupo em estruturas sintáticas.
* Cria uma representação intermediária tipo árvore que mostra a estrutura gramática da sequência obtida do analisador léxico.
* Identifica também erros sintáticos.


<hr/>

#### Análise semântica


```Análise Semântica```: é a fase em que o compilador verifica aspectos que vão além da estrutura gramatical do programa, como a compatibilidade de tipos, a declaração de variáveis e a correta utilização de identificadores. Ela assegura que os componentes do programa se comportem de acordo com suas definições.

<u>Exemplo</u>:<br/>
<u>Código-fonte</u>: a = 5 + "teste";<br/>
<u>Erro Semântico</u>: Tentativa de somar um inteiro com uma string.

<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img07.png">

Nesta fase são respondidas perguntas como:
1. O identificador position foi declarado? Em caso negativo, ERRO SEMÂNTICO;
2. O identificador position é uma variável? Em caso negativo, ERRO SEMÂNTICO.
3. Qual o escopo da declaração da variável position é local? Global?
4. Qual o tipo da variável position?
5. Está recebendo valores permitidos?

E também,
    * Reúne informações sobre tipos e os incorpora à tabela de símbolos ou dependendo da situação e estratégia, pode salvar essas informações na árvore de sintaxe.


<hr/>
<hr/>
<hr/>

### Fase de síntese

#### Geração de código intermediário
<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img08.png">

* Fase em que uma ou mais representações intermediárias do código fonte é gerada.
* Existem várias possibilidades para representação intermediária.
* Propriedades importantes:
    * Ser acurada (capaz de representar o código fonte sem perda de informação).
    * Ser facilmente reproduzida.
    * Ser facilmente traduzida para a máquina alvo.

<hr/>


#### Otimização de código
<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img09.png">

* Processo para melhorar o código intermediário.
* Pode ter como objetivo transformar o código para:
    * Obter maior velociade;
    * Obter código menor;
    * Obter código que consuma menor energia.


<hr/>

#### Geração de código
<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte02/img10.png">

* Fase final da compilação;
* Recebe a representação intermediária da fase anterior e realiza o mapeamento desta representação em uma lingaugem final, geralmente de montagem.


### Considerações sobre um compilador
#### Propriedades de um bom compilador:
* Gerar código correto
* Manipular programas de tamanho arbitrário.
* Compilação rápida.
* Bom relatório de erros.
* Tamanho de código gerado conveniente ao propósito do compilador.

#### Portabilidade
* Esforço para que o programa funcione em diferentes máquinas
    * Portabilidade do compilador
        * Quando está disponível para mais de uma plataforma.
    * Portabilidade de geração de código.
        * Quando o compilador consegue gerar código para mais de uma plataforma.

