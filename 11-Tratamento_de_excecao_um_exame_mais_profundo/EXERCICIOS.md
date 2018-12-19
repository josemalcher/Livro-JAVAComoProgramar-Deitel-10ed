## Exercícios de revisão

11.1 Liste cinco exemplos de exceções comuns.

11.2 Por que as exceções são particularmente adequadas para lidar com erros produzidos por métodos de classes na Java API?

11.3 O que é um “vazamento de recurso”?

11.4 Se nenhuma exceção é lançada em um bloco try, onde o controle prossegue quando o bloco try completa a execução?

11.5 Dê uma vantagem fundamental de utilizar catch(Exception nomeDaExceção).

11.6 Um aplicativo convencional deve capturar objetos Error? Explique.

11.7 O que acontece se nenhuma rotina de tratamento catch corresponder ao tipo de um objeto lançado?

11.8 O que acontece se vários blocos catch correspondem ao tipo do objeto lançado?

11.9 Por que um programador especificaria um tipo de superclasse como o tipo em um bloco catch?

11.10 Qual é a razão chave para utilizar blocos finally?

11.11 O que acontece quando um bloco catch lança uma Exception?

11.12 O que a instrução throw referênciaDaExceção faz em um bloco catch?

11.13 O que acontece com uma referência local em um bloco try quando esse bloco lança uma Exception?


## Respostas dos exercícios de revisão

11.1 Esgotamento de memória, índice de array fora dos limites, estouro aritmético, divisão por zero, parâmetros de método inválidos.

11.2 É improvável que os métodos de classes na Java API possam realizar processamento de erro que atenda às necessidades particulares de todos os usuários.

11.3 Um “vazamento de recurso” ocorre quando um programa em execução não libera adequadamente um recurso quando ele não é mais necessário.

11.4 Os blocos catch para essa instrução try são pulados e o programa retoma a execução depois do último bloco catch. Se houver um bloco finally, ele será executado primeiro; então o programa retomará a execução depois do bloco finally.

11.5 A forma catch(Exception nomeDaExceção) captura qualquer tipo de exceção lançada em um bloco try. Uma vantagem é que nenhuma Exception lançada pode passar sem ser capturada. Você pode tratar a exceção ou relançá-la.

11.6 Errors são problemas normalmente sérios com o sistema Java subjacente; a maioria dos programas não quer capturar Errors porque não serão capazes de se recuperar deles.

11.7 Isso faz com que a pesquisa por uma correspondência continue na próxima instrução try circundante. Se houver um bloco finally, ele será executado antes de a exceção ir para a próxima instrução try circundante. Se não houver nenhuma instrução try circundante para a qual existem blocos catch correspondentes, e as exceções forem declaradas (ou não verificadas), um rastreamento de pilha é impresso e a thread atual termina antes. Se as exceções são verificadas, mas não capturadas ou declaradas, ocorrem erros de compilação.

11.8 O primeiro bloco catch correspondente depois do bloco try é executado.

11.9 Isso permite que um programa capture tipos de exceções relacionadas e os processe de maneira uniforme. Entretanto, costuma ser útil processar os tipos de subclasse individualmente para obter um tratamento de exceção mais preciso.

11.10 O bloco finally é o meio preferido de liberar recursos para impedir vazamentos de recurso.

11.11 Primeiro, o controle passa para o bloco finally se houver algum. Em seguida, a exceção será processada por um bloco catch (se houver algum) associado com um bloco try envolvente (se houver algum).

11.12 Ele relança a exceção para o processamento por uma rotina de tratamento de exceção de uma instrução try envolvente, depois de o bloco finally da instrução try atual executar.

11.13 A referência sai de escopo. Se o objeto referenciado torna-se inacessível, o objeto pode passar por coleta de lixo. Questões

11.14 (Condições excepcionais) Liste as várias condições excepcionais que ocorreram em programas por todo este livro até agora. Liste o maior número de condições excepcionais adicionais que você puder. Para cada uma delas, descreva brevemente como um programa normalmente trataria a exceção usando as técnicas de tratamento de exceção discutidas neste capítulo. Exceções típicas incluem divisão por zero e índice de array fora dos limites.

11.15 (Exceções e falha de construtor) Até este capítulo, descobrimos que lidar com erros detectados por construtores é um pouco complicado. Explique por que o tratamento de exceção é um meio eficaz de lidar com falha de construtor.

11.16 (Capturando exceções com superclasses) Utilize herança para criar uma superclasse de exceção (chamada ExceptionA) e subclasses de exceção ExceptionB e ExceptionC, em que ExceptionB herda de ExceptionA e ExceptionC herda de ExceptionB. Escreva um programa para demonstrar que o bloco catch para tipo ExceptionA captura exceções de tipos ExceptionB e ExceptionC.

11.17 (Capturando exceções com a classe Exception) Escreva um programa que demonstra como várias exceções são capturadas com 

```
catch (Exception exception)
```

Desta vez, defina as classes ExceptionA (que herda da classe Exception) e ExceptionB (que herda da classe ExceptionA). Em seu programa, crie blocos try que lançam exceções de tipos ExceptionA, ExceptionB, NullPointerException e IOException.

Todas as exceções devem ser capturadas com blocos catch para especificar o tipo Exception.


11.18 (Ordenando blocos catch) Escreva um programa que demonstre que a ordem dos blocos catch é importante. Se você tentar capturar um tipo de exceção de superclasse antes de um tipo de subclasse, o compilador deve gerar erros.

11.19 (Falha de construtor) Escreva um programa que mostra um construtor que passa informações sobre a falha do construtor para uma rotina de exceção. Defina a classe SomeClass, que lança um Exception no construtor. O seu programa deve tentar criar um objeto do tipo SomeClass e capturar a exceção que é lançada do construtor.

11.20 (Relançando exceções) Escreva um programa que ilustra o relançamento de uma exceção. Defina os métodos someMethod e someMethod2. O método someMethod2 deve lançar inicialmente uma exceção. O método someMethod deve chamar someMethod2, capturar a exceção e relançá-la. Chame someMethod a partir do método main e capture a exceção relançada. Imprima o rastreamento de pilha dessa exceção.

11.21 (Capturando exceções com escopos externos) Escreva um programa que mostra que um método com seu próprio bloco try não precisa capturar todo possível erro gerado dentro do try. Algumas exceções podem escorregar para, e serem tratadas em, outros escopos.




