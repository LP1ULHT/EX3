**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**

*Linguagens de Programação I*

# Exercício 3 - Calculator

Este exercício serve os seguintes objectivos:
- Utilização de operadores
- Utilização de variáveis
- Utilização de ciclos
- Praticar pensamento algoritmico

Na resolução destes exercícios deve ser utilizada a Linguagem de Programação C. Para além da correta implementação dos requisitos, tenha em conta os seguintes aspetos:
- O código apresentado deve ser bem indentado. 
- O código deve compilar sem erros ou *warnings* utilizando o *gcc* com as seguintes flags:
- `-g -Wvla -Wall -Wpedantic -Wextra -Wdeclaration-after-statement`
- Tenha em atenção os nomes dados das variáveis, para que sejam indicadores daquilo que as mesmas vão conter.
- Não se pode utilizar a biblioteca `math.h`
- O trabalho deve ser desenvolvido e submetido de forma individual.

Este exercício deverá ser submetido na plataforma Pandora até às 23:59 do dia 10/4/2022 e será contabilizado para a nota final da unidade curricular de acordo com os critérios disponibilizados na página da disciplina, concretamente nos slides da primeira aula.

## Descrição do problema
Faça um programa que apresente um menu e fique à espera que o utilizador escolha uma das opções. Em seguida o programa deve executar a operação escolhida. Após a realização da operação, o programa deverá ficar à espera de um novo *input* do utilizador. Se o utilizador introduzir uma opçao desconhecida, o programa deverá imprimir a mensagem `Unknown option`.

O progama deverá apresentar o seguinte menú:
```C
puts("+-Simple Math -----------------------+");
puts("|  + <a> <b> - compute a + b         |");
puts("|  - <a> <b> - compute a - b         |");
puts("|  * <a> <b> - compute a * b         |");
puts("|  / <a> <b> - compute a / b         |");
puts("|  % <a> <b> - compute a % b         |");
puts("+-Conversions -----------------------+");
puts("|  h <x>     - x from dec to hex     |");
puts("|  H <x>     - x from hex to dec     |");
puts("|  o <x>     - x from dec to oct     |");
puts("|  O <x>     - x from oct to dec     |");
puts("|  c <x>     - x from hex to oct     |");
puts("|  C <x>     - x from oct to hex     |");
puts("+-Advanced --------------------------+");
puts("|  ! <n>     - factorial of n        |");
puts("|  b <n>     - plays buzz up to n    |");
puts("+-Interface -------------------------+");
puts("|  h         - print this menu       |");
puts("|  q         - end program           |");
puts("+------------------------------------+");
```

* opção `q`
   O programa deverá correr até que o utilizador seleccione a opção `q`. Nesse caso o programa deverá apresentar a mensagem `Bye` e em seguida deverá terminar.

* opção `s`
   Se o utilizador escolher a opção `s`, o programa deverá apresentar de novo o menu.

* opções `+`, `-`, `*`, `/`, `%`
   Estas opções recebem dois números do tipo `int`, denominados `a` e `b`. Consoante a opção escolhida o programa deverá realização a operação matemática correspondente. O resultado deverá ser impresso utilizando o seguinte formado `%d`. Nas operações de divisão, se o divisor for 0, o programa deverá imprimir o seguinte erro: `Error division by zero`. As divisões são inteiras.

* opção `h`
   Deverá ser lido um inteiro do tipo `short int` em base decimal e o resultado deverá ser apresentao em hexadecimal com o prefixo `0x` e com os dígitos hexadecimais em letras maiúsculas. O resultado deverá ocupar sempre 4 dígitos a seguir ao prefixo e para isso deverão, caso necessário, ser adicionados zeros à esquerda. Exemplo:
```
h 10
0x000A
```

* opção `o`
   Deverá ser lido um inteiro do tipo `short int` em base decimal e o resultado deverá ser apresentao em octal com o prefixo `0o`. 
O resultado deverá apresentar sempre seis dígitos a seguir ao prefixo - deverão ser adicionados zeros à esquerda caso seja necessário.

* opções `H`, `O`
   Deverá ser lido um inteiro do tipo `unsigned short int` em base hexadecimal ou octal (dependendo da opção escolhida) e o resultado deverá ser apresentao em base decimal (com sinal) ocupando 5 dígitos (com zeros à esquerda se necessário).
   

* opções `c`, `C`
   Deverá ser lido um inteiro do tipo `unsigned short int` em base hexadecimal ou octal (dependendo da opção escolhida) e o resultado deverá ser apresentao em hexadecimal ou octal respeitando as indicações para apresentação do resultado das opções `h` e `o`, respectivamente.


* opção `!`
   Esta opção recebe um número `n` do tipo `unsigned int` e em seguida deverá calcular o factorial desse número.
 
* opção `b`
   Esta opção recebe um número `n` do tipo `unsigned int` e em seguida escreve a sequência do jogo buzz. Nesta sequência os números acabados em 7 ou multiplos de 7 são substituidos pela palavra `buzz` enquanto que os restantes números são mostrados na consola. Um número por linha. Exemplo:

```b 18
1
2
3
4
5
6
buzz
8
9
10
11
12
13
buzz
15
16
buzz
18```

### Notas adicionais

O código deverá estar correctamente indentado e comentado. É estritamente proibida a utilização da instrução `goto`. 
A utilização de variáveis globais (excepto constantes) é também proibida. 


## Honestidade Académica

Nesta disciplina, espera-se que cada aluno siga os mais altos padrões de honestidade académica. Trabalhos que sejam identificados como cópias serão anulados e os alunos envolvidos terão nota zero - quer tenham copiado, quer tenham deixado copiar.
Para evitar situações deste género, recomendamos aos alunos que nunca partilhem ou mostrem o seu código.
A decisão sobre se um trabalho é uma cópia cabe exclusivamente aos docentes da unidade curricular.
Os alunos são encorajados a discutir os problemas com outros alunos mas não deverão, no entanto, copiar códigos, documentação e relatórios de outros alunos. Em nenhuma circunstância deverão partilhar os seus próprios códigos, documentação e relatórios. De facto, não devem sequer deixar códigos, documentação e relatórios em computadores de uso partilhado.

*Todos os entregues serão comparados utilizando um algoritmo de detecção de plágio [(3)](#ref3) que automaticamente atribui uma percentagem de semelhança entre os trabalhos. Este algoritmo é extremamente robusto e será utilizado nesta disciplina em todos os trabalhos ao longo do ano.* 

## Referências

<a name="ref1"></a>

* (1) Pereira, A. (2017). C e Algoritmos, 2ª edição. Sílabo.

<a name="ref2"></a>

* (2)  PANDORA - Yet Another Automated Assessment Tool, https://saturn.ulusofona.pt/.

<a name="ref3"></a>

* (3)  Saul Schleimer, Daniel S. Wilkerson, and Alex Aiken. 2003. Winnowing: local algorithms for document fingerprinting. In Proceedings of the 2003 ACM SIGMOD international conference on Management of data (SIGMOD '03). Association for Computing Machinery, New York, NY, USA, 76–85. DOI:https://doi.org/10.1145/872757.872770

## Metadados

* Autor: [Pedro Serra]
* Instituição: [Universidade Lusófona de Humanidades e Tecnologias][ULHT]
