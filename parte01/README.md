# Compiladores
## Introdução

- [O estudo de compiladores](#o-estudo-de-compiladores)
- [Outros tipos de tradutores](#outros-tipos-de-tradutores)
- [Linguagens de programação](#linguagens-de-programação)
- [Uso da teoria em aplicações](#uso-da-teoria-em-aplicações)

## O estudo de compiladores
* Tradução para um formato que permita a execução em uma máquina
* Ideias básicas para construção de tradutores para grande variedade de linguagens e máquinas.
* Princípioos e técnicas que podem ser aplicadas em vários outros domínios.

* Alguns tópicos envolvidos:
1.  Linguagens de programação
2. Arquitetura de máquina
3. Teoria de linguagem
4. Algoritmos e estruturas de dados
5. Engenharia de software

* O que será visto:
1. Tipos de tradutores
2. Visão geral da arquitetura de um compilador
3. Recursos das linguagens de programação e arquiteturas de máquinas
4. Aplicações da tecnologia de compilador

* O que é um compilador?

```
Sistema que recebe como entrada um programa escrito em uma linguagem de programação (Linguagem fonte) e produz como saída um programa equivalente em outra linguagem (Linguagem objeto).
```

* <b>Compiladores</b>: tradutores que mapeiam programas escritos em linguagem de alto nível para programas equivalentes em linguagem símbólica ou de máquina.

---------------- Tempo de compilação --------------

Programa fonte -> Compilador -> Programa objeto

<hr/>

---------------- Tempo de execução --------------

Dados de entrada -> Programa objeto -> Resultados

* Princípios fundamentais
1. Preparação da significado do programa a ser compilado
2. Geração de código eficiente

* <b>Complexidade</b>: processo com múltiplas etapas, baseadas em vários fundamentos teóricos e diferentes opções de abordagem.
* <b>Automatização</b>: tecnologia madura, com ferramentas que geram códigos para partes críticas de um compilador.

* Atividades são agrupadas em 2 fases:
1. Análise (Front-end)
2. Síntese (Back-end)

* Pontos positivos de compiladores:
1. Tempo de execução menor.
2. Código objeto é gerado apenas se a fonte não tiver erros.
3. Apresenta lista de erros, fornecendo uma visão geral dos problemas.
4. Permite otimização de código.

```Exemplos de linguagens compiladas: c/c++, Go, Rust, Zig, ...```

* Itens importantes no desenvolvimento:
1. Tempo de compilação
2. Otimização, i.e., esforço para produção de uma compiladore que gere um código mais eficiente.
* Etapa importante e complexa:
1. Diferentes objetivos: menor tempo de execução, menor consumo de energia.
2. Diferentes arquiteturas de processadores.
<
### Processo de tradução
|Código fonte| ---compilador---> |Código objeto| ---Ligador/carregador---> |Código executável| ---Execução-->

- Código fonte: Editor de texto/IDE
- Código execuável: criação de código executável e alocação de memória.

* <b>Ligador</b>: resolve pendências de endereços e produz um arquivo objeto executável.
* <b>Carregador</b>: componente do Sistema Operacional responsável por carregar o execurável na memória.


## Outros tipos de tradutores
* <b>Montadores</b> (Assemblers):
1. Mapeiam instruções em linguagem simbólica ou de montagem (assembly) para linguagem de máquina.
2. <b>Desmontadores</b> (disassemblers): fazem o processo inverso.
3. <b>Interpretador</b>: executa diretamente as operações específicas no programa sobre as entradas fornecidas pelo usuário.

                      Dados de entrada      
---Programa fonte--->|Intepretador|---Resultados--->

### Interpretadores
1. Não há tradução de linguagem
2. Apresenta melhor diagnóstico de erros, pois executa o programa fonte instrução por instrução.
3. Exemplos de linaguagens interpretadas: Python, Ruby, JavaScript, PHP, ...

* Pontos negativos de interpretadores:
1. Tempo de execução maior, pois decodifica cada instrução de alto nível para o SO durante a execução.
2. Exige mais espaço em memória para execução, pois precisa mantar o interpretador carregado.
3. Processo difícil para linguagens complexas, pois o significado de cada instrução deve ser determinado em tempo de execução.

### Sistema híbrido
* Recebe como entrada o programa fonte, gerando um código intermediário que é executado diretamente sobre as entradas fornecidas pelo usuário.

---Programa fonte--->|Compilador ou Tradutor|---Programa intermediário--->|Interpretador ou Máquina Virtual|---Resultados--->

* Traduz linguagem de alto nível para uma intermediária.
* É mais rápido do que interpretação pura.
* Aenas o código intermediário é interpretado.
* É mais portável, pois a linguagem intermediária não precisa ser recompilada.
* Tenta combinar o melhor de compiladores e interpretadores.

```Exemplos de linguagens com sistema híbrido: Java, C#, Kotlin, ...```

* Linguagem Java
1. Compina compilação e interpretação
2. Compilação gere bytecode (Código portável)
    * Interpretação do bytecode é feita pela Java Virtual Machine (JVM)
    * JVM usa compilação just-in-time (JIT) que permite que partes do código (mais utilizadas) sejam compiladas para código de máquina para otimização da execução.



## Linguagens de programação
#### Gerações de linguagens
* Primeira: linguagens de máquina
* Segunda: linguagens simbólicas ou de montagem
* Terceira: linguagens procedurais
    * Exemplo: C/C++, Java, Python, PHP, Pearl, C#, Rust, ...
* Quarta: linguagens orientadas a aplicação
    * Exemplos: Unix shell, SQL, R, ...
* Quinta: linguagens baseadas na solução de problemas usando restrições (em especial, em IA)
    * Exemplo: Prolog, Mercury, ICAD, ...

## Uso da teoria em aplicações
Construir um compilador pode envolver várias áreas:
* Linguagens de programação
* Arquiteturas de computadores
* Sistemas Operacionais
* Linguagem de montagem
* Estruturas de dados
* Complexidade de algoritmos
* Linguagens formais e autômatos

#### Construção de ferramentas para processamento de linguagens:
* Linguagens de programação
* Formatadores de textos (HTML, Latex)
* Interpretadores de consultas em bancos de dados (queries)
#### Outras aplicações:
* Construção de programas para conversão de base de dados
* Rotinas para leitura de arquivos estruturados
* Analisadores ortográficos
* Otimizações de arquiteturas de computador
* Projeto de novas arquiteturas de computador
* Geração de código para hardware específico
* Automação de tarefas em TIC.
