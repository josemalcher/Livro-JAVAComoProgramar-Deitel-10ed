## Exercícios de revisão

10.1 Preencha as lacunas em cada uma das seguintes afirmações:

a) Se uma classe contiver pelo menos um método abstrato, ela será uma classe ________.

b) As classes a partir das quais os objetos podem ser instanciados são chamadas ________.

c) ________ envolve a utilização de uma variável de superclasse para invocar métodos nos objetos de superclasse e de subclasse, permitindo que você “programe no geral”.

d) Os métodos que não são métodos de interface e que não fornecem implementações devem ser declarados com a palavra-chave ________.

e) Fazer uma coerção em uma referência armazenada em uma variável da superclasse para um tipo de subclasse é chamado ________.


10.2 Determine se cada uma das instruções a seguir é verdadeira ou falsa. Se falsa, explique por quê.

a) Todos os métodos em uma classe abstract devem ser declarados como métodos abstract.

b) Não é permitido invocar um método “somente de subclasse” por meio de uma variável de subclasse.

c) Se uma superclasse declarar um método como abstract, uma subclasse deverá implementar esse método.

d) Um objeto de uma classe que implementa uma interface pode ser pensado como um objeto desse tipo de interface.


10.3 (Interfaces Java SE 8) Preencha os espaços em branco em cada uma das seguintes instruções:

a) No Java SE 8, uma interface pode declarar ________, isto é, métodos public com implementações concretas que especificam como uma operação deve ser realizada.

b) A partir do Java SE 8, as interfaces agora podem incluir métodos auxiliares ________.

c) A partir do Java SE 8, qualquer interface que contém um único método é conhecida como ________.


## Respostas dos exercícios de revisão

10.1 a) abstrata. b) concretas. c) Polimorfismo. d) abstract. e) downcasting.

10.2 a) Falso. Uma classe abstrata pode incluir métodos com implementações e métodos abstract. b) Falsa. Tentar invocar um método somente de subclasse com uma variável de superclasse não é permitido. c) Falsa. Somente uma subclasse concreta deve implementar o método. d) Verdadeira.

10.3 a) métodos default. b) static. c) interface funcional.

## Questões

10.4 Como o polimorfismo permite programar “no geral” em vez de “no específico”? Discuta as vantagens cruciais da programação “no geral”.

10.5 O que são métodos abstratos? Descreva as circunstâncias em que um método abstrato seria apropriado.

10.6 Como o polimorfismo promove extensibilidade?

10.7 Discuta três maneiras como você pode atribuir referências de superclasse e de subclasse a variáveis de superclasse e a tipos de subclasse.

10.8 Compare e contraste classes abstratas e interfaces. Por que você utilizaria uma classe abstrata? Por que você utilizaria uma interface?

10.9 (Interfaces Java SE 8) Explique como métodos default permitem adicionar novos métodos a uma interface existente sem violar as classes que implementaram a interface original.

10.10 (Interfaces Java SE 8) O que é uma interface funcional?

10.11 (Interfaces Java SE 8) Por que é útil ser capaz de adicionar métodos static a interfaces?

10.12 (Modificação do sistema de folha de pagamento) Modifique o sistema de folha de pagamento das figuras 10.4 a 10.9 para incluir a variável de instância private birthDate na classe Employee. Utilize a classe Date da Figura 8.7 para representar o aniversário de um funcionário. Adicione métodos get à classe Date. Suponha que a folha de pagamento seja processada uma vez por mês. Crie um array de variáveis Employee para armazenar referências aos vários objetos de funcionário. Em um loop, calcule a folha de pagamento para cada Employee (polimorficamente) e adicione um bônus de US$ 100.00 à quantia da folha de pagamento do funcionário se o mês atual for aquele em que ocorre o aniversário do Employee.

10.13 (Projeto: hierarquia Shape) Implemente a hierarquia Shape mostrada na Figura 9.3. Cada TwoDimensionalShape deve conter o método getArea para calcular a área da forma bidimensional. Cada ThreeDimensionalShape deve ter métodos getArea e getVolume para calcular a área do volume e superfície, respectivamente, da forma tridimensional. Crie um programa que utiliza um array de referências Shape para objetos de cada classe concreta na hierarquia. O programa deve imprimir uma descrição de texto do objeto ao qual cada elemento no array se refere. Além disso, no loop que processa todas as formas no array, determine se cada forma é uma TwoDimensionalShape ou uma ThreeDimensionalShape. Se for uma TwoDimensionalShape, exiba sua área. Se for uma ThreeDimensionalShape, exiba sua área e volume.

10.14 (Modificação do sistema de folha de pagamento) Modifique o sistema de folha de pagamento das figuras 10.4 a 10.9 para incluir uma subclasse PieceWorker adicional de Employee que representa um funcionário cujo pagamento está baseado no número de peças de mercadorias produzido. A classe PieceWorker deve conter variáveis de instância wage private (para armazenar o salário do funcionário por peça) e pieces (para armazenar o número de peças produzido). Forneça uma implementação concreta do método earnings na classe PieceWorker que calcula os vencimentos do funcionário multiplicando o número de peças produzido pelo salário por peças.

Crie um array de variáveis Employee para armazenar referências a objetos de cada classe concreta na nova hierarquia Employee. Para cada Employee, exiba sua representação de String e vencimentos.


10.15 (Modificação do sistema de contas a pagar) Neste exercício, modificamos o aplicativo de contas a pagar das figuras 10.11 a 10.15 a fim de incluir a funcionalidade completa do aplicativo de folha de pagamento das figuras 10.4 a 10.9. O aplicativo ainda deve processar dois objetos Invoice, mas agora deve processar um objeto de cada uma das quatro subclasses Employee. Se o objeto atualmente processado for uma BasePlusCommissionEmployee, o aplicativo deverá aumentar o salário-base de BasePlusCommissionEmployee em 10%. Por fim, o aplicativo deve gerar a saída da quantia de pagamento para cada objeto. Complete os seguintes passos para criar o novo aplicativo:

a) Modifique as classes HourlyEmployee (Figura 10.6) e CommissionEmployee (Figura 10.7) para colocá-las na hierarquia Payable como subclasses da versão de Employee (Figura 10.13) que implementa Payable. 

[Dica: altere o nome do método earnings para getPaymentAmount em cada subclasse, de modo que a classe satisfaça seu contrato herdado com a interface Payable.]

b) Modifique a classe BasePlusCommissionEmployee (Figura 10.8) para que ela estenda a versão da classe CommissionEmployee criada na parte (a).

c) Modifique PayableInterfaceTest (Figura 10.15) para processar polimorficamente duas Invoice, uma SalariedEmployee, uma HourlyEmployee, uma CommissionEmployee e uma BasePlusCommissionEmployee. Primeiro gere uma representação String de cada objeto Payable. Em seguida, se um objeto for uma BasePlusCommissionEmployee, aumente seu salário-base em 10%. Por fim, gere a saída da quantia de pagamento para cada objeto Payable.

10.16 (Modificação no sistema Contas a Pagar) É possível incluir a funcionalidade do aplicativo de folha de pagamento (figuras 10.4 a 10.9) no aplicativo contas a pagar sem modificar as subclasses Employee SalariedEmployee, HourlyEmployee, CommissionEmployee ou BasePlusCommissionEmployee. Para fazer isso, modifique a classe Employee (Figura 10.4) para implementar a interface Payable e declare o método getPaymentAmount para invocar o método earnings. O método getPaymentAmount passaria então a ser herdado pelas subclasses na hierarquia Employee. Quando getPaymentAmount é chamado para um objeto de subclasse particular, ele invoca polimorficamente o método de earnings adequado para a subclasse. Reimplemente a Questão 10.15 usando a hierarquia Employee original a partir do aplicativo de folha de pagamento das figuras 10.4 a 10.9. Modifique a classe Employee como descrito nesta questão, e não modifique nenhuma das subclasses da classe Employee.



## Fazendo a diferença

10.17 (Interface CarbonFootprint: polimorfismo) Usando as interfaces, como aprendeu neste capítulo, você pode especificar comportamentos semelhantes para as classes possivelmente díspares. Governos e empresas em todo o mundo estão cada vez mais preocupados com as pegadas de carbono (liberações anuais de dióxido de carbono na atmosfera) a partir de edifícios que queimam vários tipos de combustíveis para aquecimento, veículos que queimam combustíveis para obter energia etc. 

Muitos cientistas culpam esses gases do efeito estufa pelo fenômeno chamado de aquecimento global. Crie três classes pequenas não relacionadas por meio de herança — as classes Building, Car e Bicycle. Dê a cada classe alguns atributos e comportamentos adequados únicos que ela não tem em comum com outras classes. Escreva uma interface de CarbonFootprint com um método getCarbonFootprint. Faça com que cada uma das suas classes implemente essa interface para que o método getCarbonFootprint calcule uma pegada de carbono adequada para essa classe (confira alguns sites que explicam como calcular pegadas de carbono). Escreva um aplicativo que cria objetos de cada uma das três classes, insere referências a esses objetos em ArrayList<CarbonFootprint>, então itera pelo ArrayList polimorficamente invocando o método getCarbonFootprint de cada objeto. 

Para cada objeto, imprima algumas informações de identificação e a pegada de carbono do objeto.