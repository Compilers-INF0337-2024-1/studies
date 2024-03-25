# Compiladores

- [O estudo de compiladores](#O-estudo-de-compiladores)
- [Outros tipos de tradutores](#Outros-tipos-de-tradutores)
- [Linguagens de programação](#Linguagens-de-programação)
- [Uso da teoria em aplicações](#Uso-da-teoria-em-aplicações)

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

### Processo de tradução
|Código fonte| ---compilador---> |Código objeto| ---Ligador/carregador---> |Código executável| ---Execução-->

- Código fonte: Editor de texto/IDE
- Código execuável: criação de código executável e alocação de memória.

* <b>Ligador</b>: resolve pendências de endereços e produz um arquivo objeto executável.
* <b>Carregador</b>: componente do Sistema Operacional responsável por carregar o execurável na memória.


## Outros tipos de tradutores
* <b>Montadores</b> (Assemblers):
1. Mapeiam instruções em linguagem simbólica ou de montagem (assembly) para linguagem de máquina.
2. Desmontadores (disassemblers) fazem o processo inverso.
 

## Linguagens de programação

## Uso da teoria em aplicações
