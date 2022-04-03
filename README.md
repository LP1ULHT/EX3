# wierdcalculator
Linguagens de Programação 1 - Exercício Prático #3

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

* opção `h`
   Se o utilizador escolher a opção `h`, o programa deverá apresentar de novo o menu.

* opções `+`, `-`, `*`, `/`, `%`
   Estas opções recebem dois números do tipo `int`, denominados `a` e `b`. Consoante a opção escolhida o programa deverá realização a operação matemática correspondente. O resultado deverá ser impresso utilizando o seguinte formado `%d`. Nas operações de divisão, se o divisor for 0, o programa deverá imprimir o seguinte erro: `Error division by zero`.

* opção `h`
   Deverá ser lido um inteiro do tipo `short int` em base decimal e o resultado deverá ser apresentao em hexadecimal com o prefixo `0x` e com os dígitos hexadecimais em letras maiúsculas. O resultado deverá ocupar sempre dois dígitos a seguir ao prefixo e para isso deverá, caso necessário, ser adicionado um zero à esquerda. Exemplo:
```
h 10
> 0x0A
```

* opção `o`
   Deverá ser lido um inteiro do tipo `short int` em base decimal e o resultado deverá ser apresentao em octal com o prefixo `0o`. 
O resultado deverá apresentar sempre três dígitos a seguir ao prefixo - deverão ser adicionados zeros à esquerda caso seja necessário.

* opções `H`, `O`, `c`, `C`
   Deverá ser lido um inteiro do tipo `unsigned short int` em base decimal e o resultado deverá ser apresentao em hexadecimal ou octal respeitando as indicações para apresentação do resultado das opções `h` e `o`, respectivamente.


* opção `!`
   Esta opção recebe um número `n` do tipo `unsigned int` e em seguida deverá calcular o factorial desse número.
 
* opção `b`
   Esta opção recebe um número `n` do tipo `unsigned int` e em seguida escreve a sequência do jogo buzz. Nesta sequência os números acabados em 7 ou multiplos de 7 são substituidos pela palavra `buzz` enquanto que os restantes números são mostrados na consola. Um número por linha.

### Notas adicionais

O código deverá estar correctamente indentado e comentado. É estritamente proibida a utilização da instrução `goto`. 
A utilização de variáveis globais (excepto constantes) é também proibida. 
