# Compiladores
## Linguagens Regulares

- [Definições](#definicoes)
- [Expressões regulares](#expressoes-regulares)

### Definições
* Alfabeto
    * Conjunto finito de símbolos.
    * Σ
* Palavra:
    * conjunto finito de símbolos (do alfabeto) justapostos.
* Prefixo
    * conjunto de símbolos justapostos iniciais de uma palavra.
* Sufixo
    * conjunto de símbolos justapostos finais de uma palavra.
* Palavra vazia
    * palavra com zero ocorrências de símbolos
    * ε
* Linguagem
    * Uma linguagem L sobre um alfabeto Σ, é um conjunto de palavras sobre Σ.

#### Implementando o analisador Léxico
<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte03/img01.png">

#### Linguagens regulares e o analisador Léxico
* Para o analisador léxico, o programa fonte é uma sequência de palavras de uma linguagem regular.
* O conjunto de tokens de uma linguagem de programação é uma linguagem regular.
* Então, escreve-se os padrões das palavras possíveis da linguagem computacional utilizando os formalismos para linguagens regulares.

#### Implementando o analisador léxico
As linguagens regulares ou do Tipo 3 são representadas através dos formalismos:
```
1. Expressões regulares
2. Autômatos finitos
3. Gramáticas regulares
```

A análise léxica é um processo que pode ser formalmente descrito através de expressões regulares, produzindo uma rotina que realiza essa análise. Essa rotina modela um autômato finito determinístico derivado matematicamente das expressões regulares espeficiadas.
    
* Geradores de analisadores léxicos.

<img src="https://raw.githubusercontent.com/Compilers-INF0337-2024-1/studies/main/parte03/img02.png">

### Expressões regulares
#### Implementando o analisador léxico
1. Expressões regulares
Definições sobre um alfabeto Σ:

<table>
    <tr>
        <td>ε</td>
        <td>Linguagem que contém exclusivamente a palavra vazia.</td>
    </tr>
    <tr>
        <td>x</td>
        <td>Seja x um símbolo do alfabeto, x é um ER.</td>
    </tr>
</table>

Se r e s são ERs e denotam as linguagens R e S respectivamente,

<table>
    <tr>
        <td>r|s</td>
        <td>r ou s</td>
    </tr>
    <tr>
        <td>(rs)</td>
        <td>Concatenação</td>
    </tr>
</table>

Definições sobre um alfabeto Σ:

<table>
    <tr>
        <td>r+</td>
        <td>Concatenação sucessiva (com uma ou várias ocorrências)</td>
    </tr>
    <tr>
        <td>r?</td>
        <td>Zero ou uma ocorrência</td>
    </tr>
     <tr>
        <td>. (ponto)</td>
        <td>Curinga (representa um caractere qualquer do alfabeto)</td>
    </tr>
     <tr>
        <td>\</td>
        <td>Caractere seguinte não é definição (i.e., escape)</td>
    </tr>
     <tr>
        <td>r*</td>
        <td>Concatenação sucessiva (com zero ou várias ocorrências)</td>
    </tr>
     <tr>
        <td>(...)</td>
        <td>agrupamento</td>
    </tr>
</table>

Definição regular é o nome dado a uma expressão regular

```
Letra -> a | b | c | d | ... | z
Dígito -> 0 | 1 | 2 | ... | 9
Identificador -> Letra (Letra|Dígito)*
```

Definição regular de números inteiros:
```Dígito+```

#### Exemplos:
* Identificadores válidos na linguagem C:
```_*L(L|D|_)*```

* Identificadores válidos em JAVA:
```(_|$)*L(L|D|_|$)*```

### Autômato Finito

