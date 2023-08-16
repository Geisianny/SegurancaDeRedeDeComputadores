## Atividade 8

1. Por que mdc(n, n + 1) = 1 é para dois inteiros consecutivos n e n + 1?
Dado que n e n+1 são dois inteiros consecutivos. Vamos supor que mdc(n,n+1) = p . Então p|n e p|n+1 . O que implica que p|n+1−n ou p|1 . Não há número que divida 1 exceto 1. Então p=1 ou mdc(n,n+1)=p=1. o que implica n e n+1 são co-primos.
2. Usando o teorema de Fermat, encontre 3^201 mod 11.
O Teorema de Fermat afirma que se "p" é um número primo e "a" é um número inteiro não divisível por "p", então:
a^(p-1) ≡ 1 (mod p)
De acordo com o Teorema de Fermat (com "p" sendo 11), temos:
3^(11-1) ≡ 1 (mod 11)
3^10 ≡ 1 (mod 11)
3^201 ≡ (3^10)^20 * 3^1 ≡ 1^20 * 3 ≡ 3 (mod 11)
Portanto, 3^201 mod 11 é igual a 3.
3. Use o teorema de Fermat para encontrar um número a entre 0 e 72, com a congruente a 9794 módulo 73.
Para usamos o teorema de Fermat para encontrar um número a que seja congruente a 9794 módulo 73, podemos seguir os seguintes passos:
Primeiro, precisamos encontrar o valor de φ(Fi )(73), onde φ é a função de Euler. Para um número primo p, φ(p) = p - 1. Portanto, φ(73) = 73 - 1 = 72. Em seguida,
dividimos o expoente 9794 por φ(73) para obter o quociente e o resto: 9794 ÷ 72 = 136 com resto 2.
Agora, aplicamos o teorema de Fermat para encontrar o valor de a. O teorema afirma que se a e p são primos entre si, então a^(φ(p)) ≡ 1 (mod p). Neste caso, a^(72) ≡ 1 (mod 73).
Portanto,
a^(9794) ≡ a^(72 * 136 + 2) ≡ (a^72)^(136) * a^2 ≡ 1^136 * a^2 ≡ a^2 (mod 73).
Agora, precisamos encontrar um número a cujo quadrado seja congruente a 2 módulo 73. Podemos fazer isso testando os valores de a de 0 a 72 até encontrar o valor correto. Implementamos um código que realiza esse procedimento, assim, encontramos que a = 36 é o número que procuramos, pois 36^2 ≡ 2 (mod 73). Portanto, a resposta é a = 36.
4. Use o teorema de Euler para encontrar um número a entre 0 e 9, tal que a seja congruente a 7^1000 módulo 10. (Observe que isso é o mesmo que o último dígito da expansão decimal de7^1000.)
Usando o teorema de Euler, precisamos primeiro calcular o valor de φ(10), onde φ(n) é a função de Euler.Essa função retorna o número de inteiros positivos menores que n que são co-primos com n. No caso de n = 10, os números co-primos com 10 são 1, 3, 7 e 9. Portanto, φ(10) = 4.
Agora, podemos usar o teorema de Euler, que afirma que se a e n são coprimos, então a^(φ(n)) é congruente a 1 módulo n. Em outras palavras,
a^(φ(n)) ≡ 1 (mod n).
Como, queremos encontrar um número a entre 0 e 9 que seja congruente a 7^1000 módulo 10. Podemos reescrever isso como
7^(1000 % φ(10))
7^(100 % 4))
≡ 7^0
≡ 1 (mod 10)
Portanto, o número a que satisfaz essa condição é 1.
5. Use o teorema de Euler para encontrar um número x entre 0 e 28, com x^85 congruente a 6 módulo 35 (Você não precisará usar qualquer pesquisa por força bruta).
Para encontrar um x entre 0 e 28 que seja congruente a 6 módulo 35, podemos usar o teorema de Euler. Primeiro, precisamos determinar φ(35), que é a função de 35. Para isso, fatoramos 35 em seus fatores primos: 35 = 5 * 7.
A função  de um número primo p:  é  p - 1, então
φ(5) = 4 e φ(7) = 6. Como 5 e 7 são primos entre si,
φ(35) = φ(5) * φ(7) = 4 * 6 = 24.
Agora, podemos usar o teorema de Euler: se 'a' e 'n' são primos entre si, então a^(φ(n)) é congruente a 1 módulo n.
Neste caso, queremos encontrar x' que seja congruente a 6 módulo 35. Temos que 6^85 ≡ 6^(85 % φ(35)) ≡ 6^13 ≡ 1 (mod 35).
Portanto, o número x que satisfaz a condição é x é 1, assim, x ≡ 6 (mod 35).
6. Observe, na Tabela 8.2, que φ(n) é par para n > 2. Isso é verdadeiro para todo n > 2. Dê um argumento conciso para explicar por que isso acontece.
A função de Euler, conta o número de inteiros positivos menores que n e co-primos com n. Para n > 2, a função sempre resulta em um número par. Isso ocorre porque quando n é um número primo, todos os números menores que n são co-primos com n, resultando em  φ(n) = n - 1, que é par. Quando n é um número composto, ele pode ser fatorado em primos distintos. Nesse caso, o valor de φ(n) é calculado multiplicando (p-1) para cada fator primo p de n. Como cada fator primo é ímpar, o produto de números ímpares resulta em um número par. Portanto, φ(n) é sempre par para n > 2.
7. Se n é composto e passa no teste de Miller-Rabin para a base a, então n é chamado de pseudoprimo forte à base a. Mostre que 2047 é um pseudoprimo à base 2.
Para mostrar que 2047 é um pseudoprimo forte à base 2, podemos usar o teste de Miller-Rabin.
Primeiro, escrevemos 2047 como 2^11 * 1 + 1. Portanto, temos n = 11 e a = 2.
Agora, vamos executar o teste de Miller-Rabin para a base 2.
Passo 1: 2^r * d + 1. Neste caso, 2047 = 2^11 * 1 + 1. Portanto, r = 11 e d = 1.
Passo 2: Escolhe um número aleatório a entre 2 e n-2. Neste caso, escolhemos a = 2.
Passo 3: Calcula x = a^d mod n. Neste caso, 2^1 mod 2047 = 2.
Passo 4: Se x for congruente a ±1 mod n, o teste é inconclusivo e n é um pseudoprimo forte à base a. Caso contrário, continue para o próximo passo.
Passo 5: Repita o seguinte processo r vezes:
Calcule x = x^2 mod n.
Se x for congruente a -1 mod n, o teste é inconclusivo e n é um pseudoprimo forte à base a. Caso contrário, continue para a próxima iteração.
No nosso caso, temos r = 11. Portanto, repetiremos o processo 11 vezes.
x = (2^1)^2 mod 2047 = 4 mod 2047
x = (4^2) mod 2047 = 16 mod 2047
x = (16^2) mod 2047 = 256 mod 2047
x = (256^2) mod 2047 = 65536 mod 2047 = 1 mod 2047
Como x é congruente a 1 mod n, o teste é inconclusivo e 2047 é um pseudoprimo forte à base 2.
Portanto, podemos concluir que 2047 é um pseudoprimo forte à base 2
8. O exemplo usado por Sun-Tsu para ilustrar o CRT foi
x = 2 (mod 3); x = 3 (mod 5); x = 2 (mod 7)
usando o Teorema Chinês do Resto (CRT), temos
Primeiro, representamos o sistema de congruências
x ≡ 2 (mod 3)
x ≡ 3 (mod 5)
x ≡ 2 (mod 7)
Em seguida, encontramos o valor de N, que é o produto dos módulos das congruências. N = 3 * 5 * 7 = 105.
Agora, encontramos os valores de N', que são os quocientes de N dividido por cada módulo. N' = N/ M.
N1 = 105/3 = 35
N2 = 105/5 = 21
N3 = 105/7 = 15
Em seguida, encontramos os valores de y', que são os inversos multiplicativos de N', módulo o respectivo módulo. y' * N' ≡ 1 (mod M).
y1 = 2, porque 2 * 35 ≡ 1 (mod 3)
y2 = 1, porque 1 * 21 ≡ 1 (mod 5)
y3 = 1, porque 1 * 15 ≡ 1 (mod 7)
Agora, podemos encontrar o valor de x somando com os produtos de cada congruência, assim
x = (2 * 35 * 2 + 3 * 21 * 1 + 2 * 15 * 1) % 105
x = (140 + 63 + 30) % 105
x = 233 % 105
x = 23
Portanto, a solução para o sistema de congruências é x = 23.
