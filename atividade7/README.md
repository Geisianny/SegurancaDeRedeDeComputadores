##Atividade

1) Qual é a diferença entre aleatoriedades estatísticas e imprevisibilidade?
	A aleatoriedade é a propriedade estatística que refere-se à variabilidade natural em fenômenos, é utilizado métodos e modelos para entender
 e quantificar essa aleatoriedadede.
       Por sua vez, a impresivibilidade é a incapacidade de prever com precisão o resultado de um evento ou comportamento em um sistema particular. 
Sendo assim, a diferença entre aleatoriedades estatísticas e imprevisibilidade está na forma como são aplicadas. A aleatoriedade é usada para descrever 
uma propriedade estatística bem definida, usada em estudos estatísticos para representar a incerteza inerente aos resultados de um experimento ou evento.
Por outro lado, a imprevisibilida implica que não há maneira de prever com certeza os resultados futuros com base nos conhecimentos atuais. 

2) Liste considerações de projeto importantes para uma cifra de fluxo.
Considerações de projeto importantes para uma cifra de fluxo:
 1. A sequência de encriptação deverá ter um período grande.
 2. O fluxo de chaves deverá se aproximar o máximo possível das propriedades de um fluxo de número aleatório verdadeiro.
 3. Para a proteção contra ataques de força bruta, a chave precisa ser suficientemente longa.

3)Por que não é desejável reutilizar uma chave de cifra de fluxo?
	A reutilização de uma chave de cifra de fluxo não é recomendada devido às vulnerabilidades que podem surgir. Um dos riscos é o ataque de chave 
reutilizada,onde um adversário intercepta duas mensagens criptografadas com a mesma chave e pode calcular facilmente o xor das duas mensagens, expondo 
potencialmente parte ou todo o conteúdo da mensagem mais longa. Outro perigo é o ataque de alteração de bits, em que um adversário pode modificar o 
conteúdo de uma mensagem sem conhecer a chave, realizando o xor da porção do texto cifrado que ele conhece com a alteração desejada.Esse ataque pode 
ser prevenido incluindo um código de autenticação de mensagem. 

4)Que operações primitivas são usadas no RC4?
O algoritmo RC4 utiliza várias operações primitivas para seu funcionamento. Algumas dessas operações incluem:
- Inicialização de vetores: O algoritmo começa inicializando dois vetores, o vetor de estado (S) e o vetor de fluxo (T). Esses vetores são preenchidos 
com valores sequenciais de 0 a 255.
- Permutação de vetores baseada na chave fornecida: A chave fornecida pelo usuário é usada para permutar o vetor de estado (S). Essa permutação envolve 
trocas de elementos do vetor com base nos valores da chave.
- Geração de sequência de bytes pseudoaleatória: Com base na permutação do vetor de estado (S), o algoritmo gera uma sequência de bytes pseudoaleatória. 
Essa sequência de bytes é usada como fluxo de chave para criptografar ou descriptografar os dados.

5) Se apanharmos um algoritmo de congruência linear com um componente aditivo de 0:

Xn+1 = (aXn) mod m

então, podemos mostrar que, se m é primo, e se determinado valor de a produz o período
máximo de m − 1, então a k também produzirá o período máximo, desde que k seja menor que
m e que m − 1 não seja divisível por k. Demonstre isso usando X0 = 1 e m = 31, e produzindo
as sequências para ak = 3, 3^2, 3^3 e 3^4

k = 1 (a^1 = 3):

X0 = 1

X1 = (3 * 1) mod 31 = 3

X2 = (3 * 3) mod 31 = 9

X3 = (3 * 9) mod 31 = 27

X4 = (3 * 27) mod 31 = 19

X5 = (3 * 19) mod 31 = 26

X6 = (3 * 26) mod 31 = 17

X7 = (3 * 17) mod 31 = 20

X8 = (3 * 20) mod 31 = 25

X9 = (3 * 25) mod 31 = 11

X10 = (3 * 11) mod 31 = 4

X11 = (3 * 4) mod 31 = 12

X12 = (3 * 12) mod 31 = 1

O período dessa sequência é 12.

k = 2 (a^2 = 9):

X0 = 1

X1 = (9 * 1) mod 31 = 9

X2 = (9 * 9) mod 31 = 19

X3 = (9 * 19) mod 31 = 25

X4 = (9 * 25) mod 31 = 12

X5 = (9 * 12) mod 31 = 4

X6 = (9 * 4) mod 31 = 5

X7 = (9 * 5) mod 31 = 8

X8 = (9 * 8) mod 31 = 7

X9 = (9 * 7) mod 31 = 28

X10 = (9 * 28) mod 31 = 22

X11 = (9 * 22) mod 31 = 20

X12 = (9 * 20) mod 31 = 26

X13 = (9 * 26) mod 31 = 17

X14 = (9 * 17) mod 31 = 10

X15 = (9 * 10) mod 31 = 30

X16 = (9 * 30) mod 31 = 16

X17 = (9 * 16) mod 31 = 23

X18 = (9 * 23) mod 31 = 14

X19 = (9 * 14) mod 31 = 3

X20 = (9 * 3) mod 31 = 27

X21 = (9 * 27) mod 31 = 1

O período dessa sequência é 21.

k = 3 (a^3 = 27):

X0 = 1

X1 = (27 * 1) mod 31 = 27

X2 = (27 * 27) mod 31 = 23

X3 = (27 * 23) mod 31 = 4

X4 = (27 * 4) mod 31 = 19

X5 = (27 * 19) mod 31 = 8

X6 = (27 * 8) mod 31 = 7

X7 = (27 * 7) mod 31 = 28

X8 = (27 * 28) mod 31 = 22

X9 = (27 * 22) mod 31 = 10

X10 = (27 * 10) mod 31 = 30

X11 = (27 * 30) mod 31 = 16

X12 = (27 * 16) mod 31 = 14

X13 = (27 * 14) mod 31 = 3

X14 = (27 * 3) mod 31 = 13

X15 = (27 * 13) mod 31 = 29

X16 = (27 * 29) mod 31 = 25

X17 = (27 * 25) mod 31 = 28

O período dessa sequência é 17.

k = 4 (a^4 = 81):

X0 = 1

X1 = (81 * 1) mod 31 = 19

X2 = (81 * 19) mod 31 = 12

X3 = (81 * 12) mod 31 = 5

X4 = (81 * 5) mod 31 = 8

X5 = (81 * 8) mod 31 = 25

X6 = (81 * 25) mod 31 = 11

X7 = (81 * 11) mod 31 = 22

X8 = (81 * 22) mod 31 = 10

X9 = (81 * 10) mod 31 = 30

X10 = (81 * 30) mod 31 = 26

X11 = (81 * 26) mod 31 = 17

X12 = (81 * 17) mod 31 = 20

X13 = (81 * 20) mod 31 = 1

O período dessa sequência é 13.

6) (a) Qual é o período máximo que pode ser obtido do seguinte gerador?
(Xn+1 = (aXn) mod 2^4)
	O período máximo que pode ser obtido do gerador Xn+1 = (aXn) mod 2^4 é 16. Isso ocorre porque o gerador é baseado em uma aritmética modular com um módulo de 16 (2^4). 
Portanto, o valor máximo que Xn pode assumir é 15 (2^4 - 1), e uma vez que Xn atinge esse valor, o próximo valor será 0, reiniciando o ciclo.

b)Qual deverá ser o valor de a?
	 O valor de a deve ser um número primo relativo a 16 para que o período máximo de 16 seja alcançado. Isso significa que a e 16 não podem ter fatores primos em comum, 
exceto 1. Por exemplo, a = 3, 5, 7, 11, ou 13 seriam valores adequados para obter o período máximo.

c)Que restrições são exigidas na semente?
	 A restrição para a semente é que ela deve ser um número inteiro entre 0 e 15 (inclusive) para garantir a geração de números aleatórios dentro do intervalo desejado.
 A semente deve ser escolhida aleatoriamente para garantir a aleatoriedade dos números gerados.

7) Que valor de chave RC4 deixará S inalterado durante a inicialização? Ou seja, após a permu-
tação inicial de S, as entradas de S serão quais aos valores de 0 a 255 na ordem crescente.
	A chave RC4 que deixará o vetor S inalterado durante a inicialização é uma sequência de números de 0 a 255 em ordem crescente. Isso significa que a chave deve ser composta
 por valores de 0 a 255 em uma ordem ascendente para que o vetor S permaneça inalterado após a permutação inicial. O uso dessa chave específica garante que o vetor S seja inicializado 
corretamente e que as operações de geração de byte pseudoaleatório do RC4 funcionem corretamente.

8. O algoritmo Blum Blum Shub é baseado na teoria dos resíduos quadráticos e utiliza três números
inteiros para realizar os cálculos: p, q e s.  Resposta em código.

a) Escolha dois números primos grandes p e q, onde p e q sejam congruentes a 3 mod 4 e não
tenham fatores primos comuns. Por exemplo, você pode escolher p = 499 e q = 503.
b) Calcule n = p ∗ q. Neste caso, n seria igual a 499 ∗ 503 = 250997.
c) Escolha um número inteiro s entre 1 e n − 1 que seja co-primo com n. Por exemplo, você
pode escolher s = 17.
d) Calcule o valor inicial x0 = (s2) mod n. Neste caso, x0 seria igual a (172) mod 250997 = 289.
e) Agora, vamos gerar uma sequência de números aleatórios usando o algoritmo Blum Blum
Shub. Para gerar cada número da sequência, use a seguinte fórmula: xi = (x2 i−1) mod n.
f) Execute a fórmula várias vezes para gerar uma sequência de números aleatórios. Por
exemplo, você pode executar a fórmula 10 vezes para obter 10 números aleatórios.
Aqui está a sequência de números aleatórios gerados usando o algoritmo Blum Blum Shub com
os valores do exemplo: 289, 253306, 14107, 23546, 67740, 144593, 79829, 46219, 132936, 9863

Qual foi a sua sequência? [1, 1, 0, 0, 0, 0, 1, 1, 1, 0].




