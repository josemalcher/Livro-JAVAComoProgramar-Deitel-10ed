Exercícios de revisão

9.1 Preencha as lacunas em cada uma das seguintes afirmações:

a) ________ é uma forma de reutilização de software em que novas classes adquirem os membros de classes existentes e as aprimoram com novas capacidades.

b) Os membros ________ de uma superclasse podem ser acessados na declaração de superclasse e nas declarações de subclasse.

c) Em um relacionamento ________, um objeto de uma subclasse também pode ser tratado como um objeto de sua superclasse.

d) Em um relacionamento ________, um objeto de classe tem referências a objetos de outras classes como membros.

e) Na herança simples, há uma classe em um relacionamento ________ com suas subclasses.

f) Os membros de uma superclasse ________ são acessíveis em qualquer lugar no qual o programa tem uma referência para um objeto daquela superclasse ou para um objeto de uma de suas subclasses.

g) Quando um objeto de uma subclasse é instanciado, um ________ é chamado de uma superclasse implícita ou explicitamente.

h) Os construtores de subclasse podem chamar construtores de superclasse via a palavra-chave ________.


9.2 Determine se cada uma das seguintes afirmações é verdadeira ou falsa. Se uma instrução for falsa, explique por quê.

a) Os construtores de superclasse não são herdados por subclasses.

b) Um relacionamento tem um é implementado via herança.

c) Uma classe Car tem um relacionamento é um com as classes SteeringWheel e Brakes.

d) Quando uma subclasse redefinir um método de superclasse utilizando a mesma assinatura, diz-se que a subclasse sobrecarrega esse método de superclasse.


## Respostas dos exercícios de revisão

9.1 a) Herança. b) public e protected. c) é um ou herança. d) tem um ou composição. e) hierárquico. f) public. g) construtor. h) super.

9.2 a) Verdadeira. 

b) Falsa. Um relacionamento tem um é implementado via composição. Um relacionamento é um é implementado via herança. 

c) Falsa. Esse é um exemplo de um relacionamento tem um. A classe Car tem um relacionamento é um com a classe Vehicle. 

d) Falsa. Isso é conhecido como sobrescrição, não sobrecarga — um método sobrecarregado tem o mesmo nome, mas uma assinatura diferente.


## Questões

9.3 (Uso de composição em vez de herança) Muitos programas escritos com herança podem ser escritos com composição, e vice-versa. Reescreva a classe BasePlusCommissionEmployee (Figura 9.11) da hierarquia CommissionEmployee–BasePlusCommissionEmployee para utilizar composição em vez de herança.

9.4 (Reutilização de software) Discuta de que maneira a herança promove a reutilização de software, economiza tempo durante o desenvolvimento de programa e ajuda a evitar erros.

9.5 (Hierarquia de herança Student) Desenhe uma hierarquia de herança para os estudantes em uma universidade semelhante à hierarquia mostrada na Figura 9.2. Use Student como a superclasse da hierarquia, então estenda Student com as classes UndergraduateStudent e GraduateStudent. Continue a estender a hierarquia o mais profundamente (isto é, com muitos níveis) possível. Por exemplo, Freshman, Sophomore, Junior e Senior poderiam estender UndergraduateStudent, e DoctoralStudent e MastersStudent poderiam ser subclasses de GraduateStudent. Depois de desenhar a hierarquia, discuta os relacionamentos entre as classes. [Observação: você não precisa escrever nenhum código para este exercício.]

9.6 (Hierarquia de herança Shape) O mundo das formas é muito mais rico do que aquelas incluídas na hierarquia de herança da Figura

9.3. Anote todas as formas que você puder imaginar — bidimensionais e tridimensionais — e transforme-as em uma hierarquia Shape mais completa com o maior número possível de níveis. Sua hierarquia deve ter a classe Shape na parte superior. As classes TwoDimensionalShape e ThreeDimensionalShape devem ampliar Shape. Acrescente subclasses adicionais, como Quadrilateral e Sphere, em suas localizações corretas na hierarquia conforme necessário.

9.7 (protected versus private) Alguns programadores preferem não utilizar acesso protected, porque acreditam que ele quebra o encapsulamento da superclasse. Discuta os méritos relativos de usar acesso protected versus acesso private em superclasses.

9.8 (Hierarquia de herança Quadrilateral) Escreva uma hierarquia de herança para as classes Quadrilateral, Trapezoid, Parallelogram, Rectangle e Square. Utilize Quadrilateral como a superclasse da hierarquia. Crie e use uma classe Point para representar os pontos em cada forma. Faça a hierarquia o mais profunda possível (isto é, com muitos níveis). Especifique as variáveis de instância e os métodos para cada classe. As variáveis de instância private de Quadrilateral devem ser os pares de coordenadas x-y para os quatro pontos que delimitam o Quadrilateral. Escreva um programa que instancia objetos de suas classes e gera saída da área de cada objeto (exceto Quadrilateral).


9.9 (O que cada trecho de código faz?)

a) Suponha que a seguinte chamada de método esteja localizada em um método earnings sobrescrito em uma subclasse:

```
super.earnings()

```

b) Suponha que a seguinte linha de código apareça antes de uma declaração de método:

```
@Override
```

c) Suponha que a seguinte linha de código apareça como a primeira instrução no corpo de um construtor:

```
super(firstArgument, secondArgument);
```

9.10 (Escreva uma linha do código) Escreva uma linha do código que realiza cada uma das seguintes tarefas:

a) Especifique que a classe PieceWorker é herdada da classe Employee.

b) Chame o método toString da superclasse Employee a partir do método toString da subclasse PieceWorker.

c) Chame o construtor da superclasse Employee a partir do construtor da subclasse PieceWorker — suponha que o construtor da superclasse receba três Strings que representam o primeiro nome, o sobrenome e o número de seguro social.


9.11 (Usando super no corpo de um construtor) Explique por que você usaria super na primeira instrução do corpo de um construtor de uma subclasse.

9.12 (Usando super no corpo de um método de instância) Explique por que você usaria super no corpo de um método de instância de uma subclasse.

9.13 (Chamando métodos get no corpo de uma classe) Nas figuras 9.10 e 9.11, os métodos earnings e toString chamam vários métodos get dentro da mesma classe. Explique os benefícios de chamar esses métodos get dentro das classes.


9.14 (Hierarquia Employee) Neste capítulo, você estudou uma hierarquia de herança em que a classe BasePlusCommissionEmployee é herdada da classe CommissionEmployee. Mas nem todos os tipos de empregados são CommissionEmployees. Neste exercício, você criará uma superclasse Employee mais geral para calcular os atributos e comportamentos na classe CommissionEmployee que são comuns a todos os Employees. Os atributos e comportamentos comuns a todos os Employees são firstName, lastName, socialSecurityNumber, getFirstName, getLastName, getSocialSecurityNumber e uma parte do método toString. 

Crie uma nova superclasse Employee que contenha esses métodos e variáveis de instância, além de um construtor. Então, reescreva a classe CommissionEmployee da Seção 9.4.5 como uma subclasse de Employee. A classe CommissionEmployee só deve conter os métodos e as variáveis de instância que não são declarados na superclasse Employee. O construtor da classe CommissionEmployee deve chamar o construtor da classe Employee, e o método toString de CommissionEmployee deve invocar o método toString de Employee.

Depois de concluir essas modificações, execute os aplicativos CommissionEmployeeTest e BasePlusCommissionEmployeeTest com essas novas classes para garantir que os aplicativos continuem a exibir os mesmos resultados para um objeto CommissionEmployee e um objeto BasePlusCommissionEmployee, respectivamente.


9.15 (Criando uma nova subclasse de Employee) Outros tipos de Employees podem incluir SalariedEmployees, que recebem um salário semanal fixo; PieceWorkers, que são pagos pelo número de peças que produzem; ou HourlyEmployees, que recebem um valor 50% maior para as horas extras.

Crie uma classe HourlyEmployee, que é herdada da classe Employee (Exercício 9.14), e tem variáveis de instância hours (um double), que representa as horas trabalhadas, e wage (um double), que representa os salários por hora, além de um construtor que recebe como argumentos primeiro nome, sobrenome, número de seguro social, salário por hora e número de horas trabalhadas, métodos set e get para manipular hours e wage, um método earnings para calcular os rendimentos de um HourlyEmployee com base nas horas trabalhadas e um método toString que retorna a representação String de HourlyEmployee. 

O método setWage deve assegurar que wage não seja negativo, e setHours, que o valor das horas esteja entre 0 e 168 (o número total de horas em uma semana). Use a classe HourlyEmployee em um programa de teste, semelhante ao da Figura 9.5.


