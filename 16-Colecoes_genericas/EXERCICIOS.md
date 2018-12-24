## Exercícios de revisão

16.1 Preencha as lacunas em cada uma das seguintes afirmações:

a) Um(a) ________ é utilizado(a) para iterar por uma coleção e pode remover elementos da coleção durante a iteração.

b) Um elemento em uma List pode ser acessado utilizando o(a) ________ do elemento.

c) Supondo que myArray contém referências aos objetos Double, ________ ocorre quando a instrução "myArray[0] = 1.25;" executa.

d) As classes Java ________ e ________ fornecem as capacidades de estruturas de dados no estilo array que podem redimensionar a si mesmas dinamicamente.

e) Se você não especificar um incremento de capacidade, o sistema irá ________ o tamanho do Vector toda vez que a capacidade adicional for necessária.

f) Você pode utilizar um(a) ________ para criar uma coleção que oferece acesso de leitura para outras pessoas ao mesmo tempo em que permite que você tenha acesso de gravação e leitura.

g) Supondo que myArray contém referências aos objetos Double, ________ ocorre quando a instrução "double number = myArray[0];" executa.

h) O algoritmo Collections ________ determina se duas coleções têm elementos em comum.


16.2 Determine se cada sentença é verdadeira ou falsa. Se falsa, explique por quê.

a) Os valores de tipos primitivos podem ser armazenados diretamente em uma coleção.

b) Uma Set pode conter valores duplicados.

c) Um Map pode conter chaves duplicadas.

d) Uma LinkedList pode conter valores duplicados.

e) Collections é uma interface.

f) Iterators podem remover elementos.

g) Com hashing, enquanto o fator de carga aumenta, a chance de colisões diminui.

h) Uma PriorityQueue permite elementos null.


## Respostas dos exercícios de revisão
16.1 a) Iterator. b) índice. c) autoboxing. d) ArrayList, Vector. e) dobrar.   
f) empacotador não modificável. g) auto-unboxing. h) disjoint.  


16.2 a) Falso. O autoboxing ocorre ao adicionar um tipo primitivo a uma coleção, o que significa que o tipo primitivo é convertido em sua classe empacotadora de tipo correspondente.  
b) Falso. Um Set não pode conter valores duplicados.  
c) Falso. Um Map não pode conter chaves duplicadas.  
d) Verdadeiro.  
e) Falso. Collections é uma class; e Collection é uma interface.  
f) Verdadeiro.  
g) Falso. À medida que o fator de carga aumenta, menos slots estão disponíveis em relação ao número total de slots, assim a probabilidade de uma colisão aumenta.  
h) Falso. A tentativa de inserir um elemento null causa uma NullPointerException.  


## Questões

16.3 Defina cada um dos seguintes termos:

a) Collection

b) Collections

c) Comparator

d) List

e) fator de carga

f) colisão

g) relação de troca espaço/tempo em hashing

h) HashMap


16.4 Explique brevemente a operação de cada um dos seguintes métodos da classe Vector:

a) add

b) set

c) remove

d) removeAllElements

e) removeElementAt

f) firstElement

g) lastElement

h) contains

i) indexOf

j) size

k) capacity


16.5 Explique por que inserir elementos adicionais em um objeto Vector cujo tamanho atual é menor que sua capacidade é uma operação relativamente rápida e por que inserir elementos adicionais em um objeto Vector cujo tamanho atual está dentro da capacidade é uma operação relativamente lenta.

16.6 Estendendo a classe Vector, os projetistas do Java foram capazes de criar a classe Stack rapidamente. Quais são os aspectos negativos dessa utilização de herança, particularmente para a classe Stack?


16.7 Responda resumidamente às seguintes perguntas:

a) Qual é a principal diferença entre um Set e um Map?

b) O que acontece quando você adiciona um valor de tipo primitivo (por exemplo, double) a uma coleção?

c) Você pode imprimir todos os elementos em uma coleção sem utilizar um Iterator? Se puder, como você os imprime?


16.8 Explique a principal operação de cada um dos seguintes métodos relacionados com Iterator:

a) iterator

b) hasNext

c) next


16.9 Explique brevemente a operação de cada um dos seguintes métodos da classe HashMap:

a) put

b) get

c) isEmpty

d) containsKey

e) keySet


16.10 Determine se cada uma das sentenças é verdadeira ou falsa. Se falsa, explique por quê.

a) Os elementos em uma Collection devem ser classificados em ordem crescente antes que uma binarySearch possa ser realizada.

b) O método first obtém o primeiro elemento em uma TreeSet.

c) Uma List criada com o método Arrays asList é redimensionável.


16.11 Explique a operação de cada um dos seguintes métodos da classe Properties:

a) load

b) store

c) getProperty

d) list


16.12 Reescreva as linhas 16 a 25 na Figura 16.3 para que sejam mais concisas utilizando o método asList e o construtor LinkedList, que aceita um argumento Collection.

16.13 (Eliminação de duplicatas) Escreva um programa que lê em uma série nomes e elimina duplicatas armazenando-os em um Set. Permita que o usuário procure um primeiro nome.

16.14 (Contando letras) Modifique o programa da Figura 16.18 para contar o número de ocorrências de cada letra em vez do número de cada palavra. Por exemplo, a string "HELLO THERE" contém dois Hs, três Es, dois Ls, um O, um T e um R. Exiba os resultados.

16.15 (Seletor de cor) Utilize uma HashMap para criar uma classe reutilizável a fim de escolher uma das 13 cores predefinidas na classe Color. 

Os nomes das cores devem ser utilizados como chaves; e os objetos Color predefinidos devem ser utilizados como valores. Coloque essa classe em um pacote que pode ser importado em qualquer programa Java. Utilize sua nova classe em um aplicativo que permite ao usuário selecionar uma cor e desenhar uma forma nessa cor.


16.16 (Contando palavras duplicadas) Escreva um programa que determina e imprime o número de palavras duplicadas em uma frase. Trate da mesma maneira letras minúsculas e maiúsculas. Ignore a pontuação.


16.17 (Inserção de elementos de uma LinkedList em uma ordem classificada) Escreva um programa que insere 25 inteiros aleatórios de 0 a 100 em ordem em um objeto LinkedList. O programa deve classificar os elementos e, então, calcular a soma dos elementos e a média de ponto flutuante deles.


16.18 (Copiando e invertendo LinkedList) Escreva um programa que cria um objeto LinkedList de 10 caracteres e, então, cria um segundo objeto LinkedList contendo uma cópia da primeira lista, mas na ordem inversa.


16.19 (Números primos e fatores primos) Escreva um programa que recebe um número inteiro de entrada de um usuário e determina se ele é primo. Se o número não for primo, exiba seus fatores primos únicos. Lembre-se de que os fatores de um número primo são somente 1 e o próprio número primo. Cada número que não é primo tem uma fatoração em primos única. Por exemplo, considere o número 54. Os fatores primos de 54 são 2, 3, 3 e 3. Quando os valores são multiplicados, o resultado é 54. Para o número 54, a saída dos fatores primos deve ser 2 e 3. Utilize Sets como parte de sua solução.


16.20 (Classificando palavras com um TreeSet) Escreva um programa que utiliza um método String split para tokenizar uma linha de entrada de texto fornecida pelo usuário e coloca cada token em um TreeSet. Imprima os elementos do TreeSet. 

[Observação: isso deve fazer com que os elementos sejam impressos na ordem de classificação ascendente.]


16.21 (Alterando a ordem de classificação de uma PriorityQueue) A saída da Figura 16.15 mostra que PriorityQueue ordena os elementos Double em ordem crescente. Reescreva a Figura 16.15 de modo que ela ordene os elementos Double em ordem decrescente (isto é, 9.8 deve ser o elemento de maior prioridade em vez de 3.2).


