## Capitulo 9

1. Quais são os principais elementos de um criptossistema de chave pública?
Ele possui cinco elementos:

Texto claro: essa é a mensagem ou dados legíveis que são alimentados no algoritmo como entrada.
Algoritmo de encriptação: realiza várias transformações no texto claro.
Chaves pública e privada: esse é um par de chaves que foi selecionado de modo que, se uma for usada para encriptação, a outra é usada para decriptação. As transformações exatas realizadas pelo algoritmo dependem da chave pública ou privada que é fornecida como entrada.
Texto cifrado: essa é a mensagem embaralhada produzida como saída. Ela depende do texto claro e da chave. Para determinada mensagem, duas chaves diferentes produzirão dois textos cifrados diferentes.
Algoritmo de decriptação: aceita o texto cifrado e a chave correspondente e produz o texto claro original.

2. Quais são os papéis da chave pública e da privada?
A chave pública é usada para criptografar dados. Quando alguém deseja enviar informações confidenciais para outra pessoa de forma segura, ele usa a chave pública do destinatário para criptografar os dados.
A chave privada é usada para descriptografar os dados que foram criptografados com a chave pública correspondente. Somente o dono da chave privada deve ser capaz de realizar essa operação, garantindo a confidencialidade dos dados.
3. Que requisitos os criptossistemas de chave pública precisam cumprir para serem um algoritmo seguro?


É computacionalmente fácil para uma parte B gerar um par (chave pública PUb, chave privada PRb).


É computacionalmente fácil que um emissor A, conhecendo a chave pública e a mensagem a ser encriptada, M, gere o texto cifrado correspondente:


C = E(PUb, M)

É computacionalmente fácil que o receptor B decripte o texto cifrado resultante usando a chave privada para recuperar a mensagem original:

M = D(PRb, C) = D[PRb, E(PUb, M)]

É computacionalmente inviável que um invasor, conhecendo a chave pública, PUb, determine a chave privada, PRb.
É computacionalmente inviável que um invasor, conhecendo a chave pública, PUb, e um texto cifrado, C, recupere a mensagem original, M.

4. Descreva, em termos gerais, um procedimento eficiente para se escolher um número primo.
No momento, não existem técnicas úteis que geram números primos de qualquer tamanho, de modo que é preciso que haja algum outro meio de resolver o problema. O procedimento geralmente usado é escolher um número ímpar aleatório da ordem de grandeza desejada e testar se ele é primo. Se não, é escolhido números aleatórios sucessivos até que seja encontrado um primo.
Porém, existem algoritmos que podem auxiliar na predição de números primos. Um dos algoritmos mais eficientes e populares, o Miller-Rabin segue os seguintes passos:

Escolha um inteiro ímpar n aleatoriamente (por exemplo, usando um gerador de número pseudoaleatório).
Escolha um inteiro a < n aleatoriamente.
Realize o teste probabilístico de números primos, como Miller-Rabin, usando a como parâmetro. Se n falhar no teste, rejeite o valor dele e vá para a etapa 1.
Se n tiver passado por um número de testes suficiente, aceite-o; caso contrário, vá para a etapa 2.

5. Antes da descoberta de quaisquer esquemas de chave pública especificas, como RSA, uma prova de existência foi desenvolvida, cuja finalidade era demonstrar que a encriptação de chave pública é possível em teoria. Considere as funções  1(x1) = z1; f2(x2, y2) = z2; f3(x3, y3) = z3, onde todos os valores são inteiros com 1 ≤ xi, yi, zi ≤ N. A função f1, pode ser representada por um vetor M1 de tamanho N, em que a k-ésima entrada é o valor de f1(k). De modo semelhante, f2 e f3 podem ser representados pelas matrizes M2 e M3 de tamanho N × N. A intenção é indicar o processo de encriptação/decriptação por pesquisas de tabela para aquelas com valores muito grandes de N. Essas tabelas seriam impraticavelmente grandes, mas, a princípio, poderiam ser construídas. O esquema funciona da seguinte forma: construa M1 com uma permutação aleatória de todos os inteiros entre 1 e N; ou seja, cada inteiro aparece exatamente uma vez em M1. Construa M2, de modo que cada linha contenha uma permutação aleatória dos primeiros N inteiros. Finalmente, preencha M3 para satisfazer a seguinte condição:
f3(f2(f1(k), p), k) = p para todo k, p com 1 ≤ k, p ≤ N
Resumindo,
1. M1 toma uma entrada k e produz uma saída x.
2. M2 toma as entradas x e p, dando a saída z.
3. M3 toma as entradas z e k e produz p.
As três tabelas, uma vez construídas, se tornam públicas.
a) Deverá ficar claro que é possível construir M3 para satisfazer a condição anterior. Como um exemplo, preencha M3 para o caso simples a seguir:

Convenção: o i-ésimo elemento de M1 corresponde a k = i. A i-ésima linha de M2 diz respeito ax = i; a j-ésima coluna de M2 equivale a p = j. A i-ésima linha de M3 indica z = i; a j-ésima coluna de MB relaciona-se a k = j.
(a) Descreva o uso desse conjunto de tabelas para realizar a encriptação e decriptação entre dois usuários.
O conjunto de tabelas M1, M2 e M3 é utilizado para realizar o processo de criptografia e descriptografia entre dois usuários. Vamos descrever como cada tabela é usada nesse processo:
Tabela M1: Essa tabela é usada para criptografar a entrada inicial k e produzir a saída x. Cada entrada k é mapeada para um valor correspondente x usando a tabela M1. A tabela M1 contém uma permutação aleatória de todos os inteiros entre 1 e N, garantindo que cada inteiro apareça exatamente uma vez.
Tabela M2: Após obter a saída x da tabela M1, ela é combinada com outra entrada p para produzir a saída z usando a tabela M2. A tabela M2 contém permutações aleatórias dos primeiros N inteiros em cada linha. Portanto, a linha correspondente a x na tabela M2 é selecionada e combinada com p para obter z.
Tabela M3: Finalmente, a saída z da tabela M2 é combinada com a entrada k original para produzir a saída p usando a tabela M3. A tabela M3 é preenchida de forma a satisfazer a condição f3(f2(f1(k), p), k) = p para todo k, p com 1 ≤ k, p ≤ N.
O processo de criptografia consiste em aplicar as tabelas M1, M2 e M3 sequencialmente para obter a mensagem criptografada a partir da entrada k e p. O resultado final é a saída p obtida após a aplicação da tabela M3.Já a descriptografia é o inverso do processo de criptografia. A mensagem criptografada, representada por p, é usada como entrada para a tabela M3, que a combina com a entrada k para produzir a saída z. Em seguida, a tabela M2 é usada para combinar z com a entrada x e obter a saída p. Por fim, a tabela M1 é usada para obter a entrada original k a partir de x.
(b) Demonstre que esse é um esquema seguro:
A segurança de um esquema criptográfico depende de sua resistência a ataques e da dificuldade de quebrar a criptografia sem a chave privada correspondente. No caso desse esquema, a segurança está relacionada à construção das tabelas M1, M2 e M3.
Uma vez que as tabelas são construídas com permutações aleatórias, cada entrada é mapeada para um valor diferente, garantindo que a função seja unidirecional. Isso significa que é computacionalmente difícil inverter o processo e obter a entrada original a partir da saída.
Além disso, a condição f3(f2(f1(k), p), k) = p para todo k, p com 1 ≤ k, p ≤ N é satisfeita pela construção da tabela M3. Isso significa que, mesmo que um adversário tenha acesso às tabelas públicas M1, M2 e M3, ele não será capaz de encontrar uma entrada k correspondente a uma saída p específica sem a chave privada correspondente.
Portanto, com base nessas considerações, pode-se afirmar que esse é um esquema seguro de criptografia de chave pública , desde que a construção das tabelas seja feita de forma adequada e segura.

6. Realize a encriptação e decriptação usando o algoritmo RSA, como na Figura 9.5, para o seguinte:
(a) p = 3; q = 11, e = 7; M = 5;
(b) p = 5; q = 11, e = 3; M = 9;
Usando os valores fornecidos (p = 5, q = 11, e = 3, M = 9), a encriptação e decriptação, seria
n: n = p * q = 5 * 11 = 55
C: C = (M^e) mod n = (9^3) mod 55 = 729 mod 55 = 14
Portanto, a encriptação de M = 9 resulta em C = 14.
Decriptação:
d = (1 * 40 + 1) / 3
d = 41 / 3
d ≈ 13.6667
Como o resultado deve ser um número inteiro, vamos tentar com 2:
d = (2 * 40 + 1) / 3
d = 81/ 3
d = 27
Então,
M: M = (C^d) mod n = (14^27) mod 55 = 9
Portanto, usando o algoritmo RSA, a decriptação de C = 14 resulta em M = 9.
(c) p = 7; q = 11, e = 17; M = 8;
(d) p = 11; q = 13, e = 11; M = 7;
(e) p = 17; q = 31, e = 7; M = 2.
Dica: a decriptação não é tão difícil quanto você pensa; use alguma sutileza.
7. Em um sistema de chave pública usando RSA, você intercepta o texto cifrado C = 10 enviado a um usuário cuja chave pública é e = 5, n = 35. Qual é o texto claro M?
No sistema de chave pública RSA, o texto claro M é obtido através da fórmula M = C^e mod n.
Dado que C = 10, e = 5 e n = 35, podemos calcular o texto claro da seguinte forma:
M = 10^5 mod 35
Utilizando o método de exponenciação modular, temos:
M = (10^5)  mod 35
M = 100^4 mod 35
M = 100.000  mod 35
M = 100.000 = 35  2857 + 5
M = 5
Portanto, o texto claro M é igual a 5.
