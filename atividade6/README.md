## Atividade 6 - capitulo 6

Estudante: Geisianny Bernardo da Silva

1. O que é encriptação tripla?
A encriptação tripla, também conhecida como Triple DES (3DES), é um algoritmo de criptografia que é usado para proteger
 informações sensíveis. Ele utiliza três passos consecutivos do algoritmo DES para encriptar os dados. Basicamente, o 
algoritmo aplica o DES três vezes em sequência, usando duas ou três chaves diferentes. As chaves geralmente são de 56
 bits cada, mas no total, a combinação de três chaves resulta em uma chave efetiva de 168 bits.
A aplicação do 3DES oferece uma camada extra de segurança em relação ao DES original, tornando-o mais resistente a 
ataques. No entanto, devido à sua complexidade e ao aumento do poder computacional atual, o 3DES tem sido gradualmente
 substituído por algoritmos mais avançados, como o AES (Advanced Encryption Standard). O AES é considerado mais seguro 
e eficiente em comparação ao 3DES.

2. O que é ataque meet-in-the-middle?
O ataque meet-in-the-middle (encontro no meio) é um tipo de ataque criptográfico que visa quebrar uma criptografia que 
utiliza duas etapas de encriptação diferentes. O princípio básico do ataque meet-in-the-middle é aproveitar a propriedade
 das funções de encriptação e desencriptação reversíveis. Ele explora a ideia de que a criptografia em duas etapas pode ser
 revertida para encontrar as chaves secretas envolvidas no processo.

3. Quantas chaves são usadas na encriptação tripla?
São utilizadas 3 chaves . A encriptação tripla é uma técnica de criptografia que consiste em aplicar três etapas de 
encriptação consecutivas para aumentar a segurança dos dados. Cada etapa utiliza uma chave diferente para realizar a 
encriptação. Portanto, são necessárias três chaves distintas para executar o processo de encriptação tripla. Esse tipo de
 encriptação representa uma contramedida para o ataque meet-in-the-middle.Porém, como alternativa, Tuchman propôs um método 
de encriptação triplo que utiliza apenas duas chaves, tornando o processo mais eficiente em termos de complexidade e 
gerenciamento de chaves.

4. Por que a parte do meio do 3DES é decriptação, em vez de encriptação?
Esse processo de decriptação foi criado para permitir a compatibilidade com o algoritmo DES original(criado como um algoritmo
 de  encriptação simétrica de 64 bits que recebe uma chave de 56 bits).Com o avanço da tecnologia, a segurança do DES começou 
a ser questionada devido ao tamanho relativamente curto da chave, assim,Para fortalecer a segurança dessa encriptação, foi 
desenvolvida uma estrategia de encriptação-decriptação-encriptação é conhecida como EDE (Encrypt-Decrypt-Encrypt).

5. Por que alguns modos de operação de cifra de bloco só utilizam a encriptação, enquanto outros
empregam encriptação e decriptação?
Umas cifras de bloco pode estender a aplicação de algoritmos de criptografia de bloco, como o AES ou o DES, a dados maiores 
que o tamanho de bloco padrão. Essas operações determinam como os blocos de dados são processados e combinados para formar o 
resultado final da criptografia. Alguns modos de operação, como o ECB (Electronic Codebook), empregam exclusivamente a encriptação 
para cifrar os blocos de dados individualmente, sem qualquer interdependência entre eles. Nesse modo, cada bloco é tratado 
de maneira isolada, o que implica que blocos idênticos na entrada resultarão em blocos idênticos na saída. Essa abordagem pode 
apresentar vulnerabilidades de segurança, uma vez que padrões e informações sobre os dados originais podem ser revelados, 
comprometendo a confidencialidade dos dados.

6. Você deseja construir um dispositivo de hardware para realizar encriptação de bloco no modo cipher block chaining (CBC) 
usando um algoritmo mais forte do que DES. 3DES é um bom candidato. A Figura 1 mostra duas possibilidades, ambas 
acompanhando a definição do CBC.Qual das duas você escolheria:
(a) Por segurança?(figura 2)
O uso de múltiplos loops no modo CBC pode aumentar a segurança da criptografia. Quanto mais loops forem aplicados, 
maior será a complexidade e a difusão dos dados, o que pode dificultar ainda mais a recuperação da chave e a análise 
criptográfica. Portanto, a opção  ideal seria a figura mostrada no item b) CBC com 3 loops.
(b) Por desempenho?(figura 1)
No entanto, é importante considerar que o uso de múltiplos loops também pode aumentar a carga de processamento e afetar o 
desempenho do dispositivo de hardware. Cada loop adicional requer mais operações de criptografia, o que pode resultar em 
um aumento do tempo de processamento. Portanto,  a opção  ideal seria a figura mostrada no item b) CBC com 3 loops.

 7. Crie um software que possa encriptar e decriptar no modo cipher block chaining usando umadas seguintes cifras: módulo affine
 256, módulo Hill 256, S-DES, DES. Teste os dados para S-DES usando um vetor de inicialização binário de 1010 1010. Um texto 
claro binário de 0000 0001 0010 0011 encriptado com uma chave binária de 01111 11101 deverá dar um texto claro binário de 
1111 0100 0000 1011. A decriptação deverá funcionar de modo correspondente. Resposta no arquivo de extensão "ipynb".

