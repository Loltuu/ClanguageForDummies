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
## Estruturas de condição
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

E também temos o Switch, o switch é usado para testar várias condições diferentes e executar um bloco de código específico para cada condição.
```c
switch(expressão) {
  case x:
    // código 
    break;
  case y:
    // código
    break;
  default:
    // código
}
```  
## Estruturas de repetição
O while é usado para executar um bloco de código enquanto uma condição for verdadeira.
```c
while (condição) {
  // código
}
```
E também temos uma variante do while que é o do/while, que executa o código dentro do bloco ao menos uma vez antes de verificar a condição, mesmo que a condição seja falsa, o código dentro do bloco será executado ao menos uma vez.
```c
do {
  // código
} while (condição);
```
E também temos o for, ele é diferente do while porque o while é usado para executar o código enquanto a condição for verdadeira. O for é usado para executar o código um número específico de vezes.
```c
for (declaração 1; declaração 2; declaração 3) {
  // código
}
``` 
## Arrays
Arrays são estruturas de dados que armazenam um conjunto de elementos de um mesmo tipo, e ele pode armazenar qualquer tipo de elemento. O Array serve para organizar os dados.
```c
int numeros[] = {10, 20, 30, 40};
```
E Arrays multidimensionais são arrays que contêm outros arrays, ele é útil organizar dados complexos.
```c
int matrix[2][3] = { {1, 2, 3}, {6, 5, 4} };
``` 
## Memory Address
O Memory Address é um endereço de memória que armazena um valor específico, ele é usado para manipular dados armazenados na memória. Um endereço de memória é um número único que identifica uma localização específica na memória. 

E é possível acessar o endereço de memória de uma variável usando o operador &.
```c
int x = 10;
printf("Endereço de memória de x: %p\n", &x);
``` 
## Ponteiros 
Ponteiros são variáveis especiais em C que armazenam o endereço de memória de outras variáveis. Eles são usados para passar informações entre funções, alocar memória dinamicamente e para acessar arrays e estruturas de dados.
```c
int x = 10; // variável inteira
int *ptr; // declaração de um ponteiro

ptr = &x; // atribui o endereço de memória de x ao ponteiro

printf("Valor de x: %d\n", x); // imprime o valor de x
printf("Valor do ponteiro: %p\n", ponteiro); // imprime o valor do ponteiro
```
## Struct
Struct é uma forma de agrupar dados de diferentes tipos em um único nome.
```c
struct pessoa {    // declaração
  char nome[50];  // membro
  int idade;     // membro
  float altura; // membro
};
```
