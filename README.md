# ClanguageForDummies

C é uma linguagem de alto nível, que foi projetada por Dennis Ritchie em 1972 para o desenvolvimento do sistema operacional Unix. Desde então, ela se tornou uma das linguagens de programação mais populares no mundo, utilizada em incontavéis aplicações.

> Por que aprender C?

Irei falar alguns motivos para se aprender a linguagem de programação C:

1. Eficiência
2. Flexibilidade
3. Portabilidade
4. Carreira

Mas antes de começarmos a criar nosso códigos, temos que aprender a base.

## Básico

![image](https://user-images.githubusercontent.com/123683822/218906237-08968c02-f3e5-4a42-a27a-a5cd172590f0.png)

Pré-Processamento: A etapa de pré-processamento envolve a execução do pré-processador, que é um programa que lê o código-fonte C e executa operações para transformar o código original em um arquivo-fonte modificado que será posteriormente compilado.

Compilação: É a transformação do código-fonte em linguagem C em um programa executável. Esse processo inclui a análise léxica e sintática, a análise semântica, a geração de código intermediário, a otimização de código e a geração de código objeto e executável.

Assembler: É a etapa que transforma o código objeto gerado pelo compilador em linguagem de montagem em código de máquina executável pelo computador.

Linker: É a etapa que combina os diferentes módulos de um programa em um único arquivo executável.

## Sintaxe Básica
```c
#include <stdio.h>

int main() {
  printf("Hello World!");
  return 0;
}
```
Essa é a sintaxe básica de C, agora vamos entender a parte teórica do que estamos fazendo nesse pequeno código:
```c
#include <stdio.h> #Esta linha é uma diretiva de pré-processador que inclui o arquivo de cabeçalho stdio.h. 

int main() { #Esta é a declaração da função principal do programa, denominada main(). Que é executada automáticamente quando o programa é iniciado 
  printf("Hello World!"); #Esta chamando à função printf(), que é usada para imprimir o texto "Hello World!" na tela. 
  return 0; #Retorna um valor inteiro de 0 ao concluir sua execução. O valor 0 é usado para indicar que o programa foi executado com sucesso.
}
``` 
## Variáveis 

Em resumo, variáveis em são usadas para armazenar valores e são declaradas especificando o tipo de dado que será armazenado.

```c
int idade = 20; # A variável int é usada para armazenar números inteiros.

float altura = 1.80; # A variável float é usada para armazenar números de ponto flutuante.

double peso = 75.0; # A variável é semelhante ao float, mas pode armazenar números com mais casas decimais.

char nome[] = "paciente"; # A variável string é usada para armazenar uma sequência de caracteres.

char letra = 'x'; # A variável é usada para armazenar caracteres.

bool vivo = true; # A variável é usada para armazenar valores booleanos (true ou false).

void criar(){ } # A variável é usada para indicar que uma função não retorna nenhum valor.

enum week {monday, tuesday, wednesday, thursday, friday}; # A variável é usada para criar um tipo de dado com um conjunto de valores pré-definidos.

long populacao = 10000000; # A variável é semelhante ao int, mas pode armazenar números maiores

short temperatura = -10; # A variável é semelhante ao int, mas ocupa menos espaço na memória.
```
## Condições
A estrutura de controle if/else é usada para executar diferentes blocos de código dependendo de uma condição. Nesse exemplo:
```c
if (condição) {
  // código
} else if (condição) {
  // código
} else {
  // código
}
``` 
O script avalia a primeira condição. Se ela for verdadeira, o primeiro bloco de código é executado e as demais condições são ignoradas. Se a primeira condição for falsa, a segunda condição é avaliada. Se ela for verdadeira, o segundo bloco de código é executado e as demais condições são ignoradas. Se todas as condições forem falsas, o bloco de código do else é executado.

Também temos o Operador Ternário, é uma sintaxe alternativa para escrever uma instrução if/else em uma única linha de código:
```c
variável = (condição) ? expressãoVerdadeira : expressãoFalsa;
```
A variável é avaliada primeiro. Se a variável for verdadeira, o expressãoVerdadira é retornado. Caso contrário, o expressãoFalsa é retornado.
