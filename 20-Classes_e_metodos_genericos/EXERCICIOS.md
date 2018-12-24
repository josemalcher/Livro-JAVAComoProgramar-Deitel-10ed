## Exercícios de revisão

20.1 Determine se cada um dos seguintes itens é verdadeiro ou falso. Se falso, explique por quê.

a) Um método genérico não pode ter o mesmo nome que um método não genérico.

b) Todas as declarações de métodos genéricos têm uma seção de parâmetro de tipo que precede imediatamente o nome de método.

c) Um método genérico pode ser sobrecarregado por um outro com o mesmo nome do método, mas diferentes parâmetros de método.

d) Um parâmetro de tipo pode ser declarado somente uma vez na seção de parâmetro de tipo, mas pode aparecer mais de uma vez na lista de parâmetros do método.

e) Os nomes dos parâmetros de tipo entre diferentes métodos genéricos devem ser únicos.

f) O escopo de um parâmetro de tipo da classe genérico é a classe inteira, exceto seus membros static.


20.2 Preencha as lacunas em cada um dos seguintes itens:

a) ________ e ________ permitem especificar, com uma única declaração de método, um conjunto de métodos relacionados ou, com uma única declaração de classe, um conjunto de tipos relacionados, respectivamente.

b) Uma seção de parâmetro de tipo é delimitada por ________.

c) ________ de um método genérico podem ser usados para especificar os tipos de argumento do método, especificar o tipo de retorno do método e declarar variáveis dentro do método.

d) A instrução “Stack objectStack = new Stack();” indica que objectStack armazena ________.

e) Na declaração de uma classe genérica, o nome da classe é seguido por um(a) ________.

f) A sintaxe ________ especifica que o limite superior de um curinga é o tipo T.


## Respostas dos exercícios de revisão

20.1 a) Falso. Métodos genéricos e não genéricos podem ter o mesmo nome de método. Um método genérico pode sobrecarregar um outro com o mesmo nome do método, mas diferentes parâmetros de método. Um método genérico também pode ser sobrecarregado fornecendo métodos não genéricos com o mesmo nome de método e número de argumentos. b) Falso. Todas as declarações de métodos genéricos têm uma seção de parâmetro de tipo que imediatamente precede o tipo de retorno do método. c) Verdadeiro. d) Verdadeiro. e) Falso. Nomes de parâmetro de tipo entre diferentes métodos genéricos não precisam ser únicos. f) Verdadeiro.

20.2 a) Métodos genéricos, classes genéricas. b) colchetes angulares (< e >). c) Parâmetros de tipo. d) um tipo bruto. e) seção de parâmetro de tipo. f) ? extends T.


## Questões

20.3 (Explique a notação) Explique o uso da seguinte notação em um programa Java:

public class Array<T> { }


20.4 (Método genérico SelectionSort) Escreva um método selectionSort genérico com base no programa de classificação da Figura 19.4. Escreva um programa de teste que insere, classifica e gera uma saída de um array Integer e um array Float. [Dica: use <T extends Comparable<T>> na seção de parâmetros de tipo para o método selectionSort, de modo que você possa usar o método compareTo para comparar os objetos do tipo que T representa.]


20.5 (Método genérico sobrecarregado printArray) Sobrecarregue o método genérico printArray da Figura 20.3 para que ele receba dois argumentos do tipo inteiro adicionais, lowSubscript e highSubscript. Uma chamada a esse método imprime somente a parte especificada do array. Valide lowSubscript e highSubscript. Se um deles estiver fora do intervalo, o método printArray sobrecarregado deve lançar uma InvalidSubscriptException; caso contrário, printArray deve retornar o número de elementos impressos. Então, modifique main para praticar as duas versões do printArray nos arrays integerArray, doubleArray e characterArray. Teste todas as capacidades das duas versões de printArray.

20.6 (Sobrecarregando um método genérico com um método não genérico) Sobrecarregue o método genérico printArray da Figura

20.3 com uma versão não genérica que imprime especificamente um array de Strings em um formato tabular perfeito, como mostrado na saída do exemplo a seguir:

```
Array stringArray contains:
one two three four
five six seven eight

```


20.7 (Método genérico isEqualTo) Escreva uma versão genérica simples do método isEqualTo que compara seus dois argumentos com o método equals e retorna true se forem iguais e false caso contrário. Utilize esse método genérico em um programa que chama isEqualTo com uma variedade de tipos predefinidos, como Object ou Integer. Qual resultado você obtém ao tentar executar esse programa?

20.8 (Classe genérica Pair) Escreva uma classe genérica Pair que tem dois parâmetros de tipo — F e S —, cada um representando o tipo do primeiro e segundo elemento do par, respectivamente. Adicione os métodos get e set ao primeiro e ao segundo elemento do par. [Dica: o cabeçalho da classe deve ser public class Pair< F, S >.] 

20.9 (Sobrecarregando métodos genéricos) Como métodos genéricos podem ser sobrecarregados?

20.10 (Solução de sobrecarga) O compilador realiza um processo de correspondência para determinar qual método chamar quando um método é invocado. Sob quais circunstâncias uma tentativa de fazer uma correspondência resulta em um erro em tempo de compilação?

20.11 (O que essa instrução faz?) Explique por que um programa Java utilizaria a instrução

ArrayList<Employee> workerList = new ArrayList<>();
