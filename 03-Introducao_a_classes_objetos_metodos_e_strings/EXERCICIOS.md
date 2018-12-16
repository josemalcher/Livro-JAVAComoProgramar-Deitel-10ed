## Exercícios de revisão

3.1 Preencha as lacunas em cada uma das seguintes sentenças:

a) Toda declaração de classe que inicia com a palavra-chave ________ deve ser armazenada em um arquivo que tem exatamente o mesmo nome que a classe e terminar com a extensão de nome do arquivo .java.

b) A palavra-chave ________ em uma declaração de classe é imediatamente seguida pelo nome da classe.

c) A palavra-chave ________ solicita memória do sistema para armazenar um objeto, e então chama o construtor da classe correspondente para inicializar esse objeto.

d) Todo parâmetro deve especificar um(a) ________ e um(a) ________.

e) Por padrão, as classes que são compiladas no mesmo diretório são consideradas como estando no mesmo pacote, conhecido como ________.

f) O Java fornece dois tipos primitivos para armazenar números de ponto flutuante na memória: ________ e ________.

g) As variáveis de tipo double representam números de ponto flutuante de ________.

h) O método scanner ________ retorna um valor double.

i) A palavra-chave public é um ________ de acesso.

j) O tipo de retorno ________ indica que um método não retornará um valor.

k) O método Scanner ________ lê os caracteres até encontrar um caractere de nova linha, então retorna esses caracteres como uma String.

l) A classe String está no pacote ________.

m) Um(a) ________ não é requerido(a) se você sempre referenciar uma classe por meio do seu nome completamente qualificado.

n) Um(a) ________ é um número com um ponto de fração decimal, como 7,33, 0,0975 ou 1000,12345.

o) As variáveis de tipo float representam ________ números de ponto flutuante de dupla precisão.

p) O especificador de formato ________ é utilizado para gerar saída de valores de tipo float ou double.

q) Os tipos no Java são divididos em duas categorias — tipo ________ e tipo ________.


3.2 Determine se cada uma das seguintes sentenças é verdadeira ou falsa. Se falsa, explique por quê.

a) Por convenção, os nomes de método são iniciados com letra maiúscula, e todas as palavras subsequentes a ele também começam com letra maiúscula.

b) Uma declaração import não é necessária quando uma classe em um pacote utiliza outra no mesmo pacote.

c) Parênteses vazios que se seguem a um nome de método em uma declaração indicam que ele não requer nenhum parâmetro para realizar sua tarefa.

d) Uma variável de tipo primitivo pode ser utilizada para invocar um método.

e) As variáveis declaradas no corpo de um método particular são conhecidas como variáveis de instância e podem ser utilizadas em todos os métodos da classe.

f) O corpo de todos os métodos é delimitado pelas chaves esquerda e direita ({ e }).

g) As variáveis locais de tipo primitivo são inicializadas por padrão.

h) As variáveis de instância de tipo por referência são inicializadas por padrão com o valor null.

i) Qualquer classe que contém public static void main(String[] args) pode ser usada para executar um aplicativo.

j) O número de argumentos na chamada de método deve corresponder ao de itens na lista de parâmetros da declaração desse método.

k) Os valores de ponto flutuante que aparecem no código-fonte são conhecidos como literais de ponto flutuante e são tipos float por padrão.


3.3 Qual é a diferença entre uma variável local e uma variável de instância?

3.4 Explique o propósito de um parâmetro de método. Qual a diferença entre um parâmetro e um argumento?

---

## Respostas dos exercícios de revisão

3.1 a) public. b) class. c) new. d) tipo, nome. e) pacote padrão. f) float, double. g) precisão dupla. h) nextDouble. i) modificador. j) void. k) nextLine. l) java.lang. m) declaração import. n) número de ponto flutuante. o) simples. p) %f. q) primitivo, referência.

3.2 a) Falsa. Por convenção, os nomes de método são iniciados com letra minúscula e todas as palavras subsequentes começam com letra maiúscula. b) Verdadeira. c) Verdadeira. d) Falsa. Uma variável de tipo primitivo não pode ser utilizada para invocar um método — uma referência a um objeto é necessária para que os métodos do objeto possam ser invocados. e) Falsa. Essas variáveis são chamadas variáveis locais e só podem ser utilizadas no método em que são declaradas. f) Verdadeira. g) Falsa. As variáveis de instância de tipo primitivo são inicializadas por padrão. Deve-se atribuir um valor explicitamente a cada variável local. h) Verdadeira. i) Verdadeira. j) Verdadeira. k) Falsa. Esses literais são de tipo double por padrão.

3.3 Uma variável local é declarada no corpo de um método e só pode ser utilizada do ponto em que isso acontece até o fim da declaração do método. Uma variável de instância é declarada em uma classe, mas não no corpo de qualquer um dos métodos dessa classe. Além disso, as variáveis de instância são acessíveis a todos os métodos da classe. (Veremos uma exceção disso no Capítulo 8.)

3.4 Um parâmetro representa informações adicionais que um método requer para realizar sua tarefa. Cada parâmetro requerido por um método é especificado na declaração do método. Um argumento é o valor real de um parâmetro de método. Quando um método é chamado, os valores de argumento são passados para os parâmetros correspondentes desse método para que ele possa realizar sua tarefa.


## Questões


3.5 (Palavra-chave new) Qual é o objetivo da palavra-chave new? Explique o que acontece quando você a utiliza.

3.6 (Construtores padrão) O que é um construtor padrão? Como as variáveis de instância de um objeto são inicializadas se uma classe tiver somente um construtor padrão?

3.7 (Variáveis de instância) Explique o propósito de uma variável de instância.

3.8 (Usando classes sem importá-las) A maioria das classes precisa ser importada antes de ser usada em um aplicativo. Por que cada aplicativo pode utilizar as classes System e String sem importá-las antes?

3.9 (Usando uma classe sem importá-la) Explique como um programa pode usar a classe Scanner sem importá-la.

3.10 (Métodos set e get) Explique por que uma classe pode fornecer um método set e um método get para uma variável de instância.

3.11 (Classe Account modificada) Modifique a classe Account (Figura 3.8) para fornecer um método chamado withdraw que retira dinheiro de uma Account. Assegure que o valor de débito não exceda o saldo de Account. Se exceder, o saldo deve ser deixado inalterado e o método deve imprimir uma mensagem que indica "Withdrawal amount exceeded account balance" [Valor de débito excedeu o saldo da conta]. Modifique a classe AccountTest (Figura 3.9) para testar o método withdraw.

3.12 (Classe Invoice) Crie uma classe chamada Invoice para que uma loja de suprimentos de informática a utilize para representar uma fatura de um item vendido nela. Uma Invoice (fatura) deve incluir quatro partes das informações como variáveis de instância — o número (tipo String), a descrição (tipo String), a quantidade comprada de um item (tipo int) e o preço por item (double). Sua classe deve ter um construtor que inicializa as quatro variáveis de instância. Forneça um método set e um get para cada variável de instância.

Além disso, forneça um método chamado getInvoiceAmount que calcula o valor de fatura (isto é, multiplica a quantidade pelo preço por item) e depois retorna esse valor como double. Se a quantidade não for positiva, ela deve ser configurada como 0. Se o preço por item não for positivo, ele deve ser configurado como 0.0. Escreva um aplicativo de teste chamado InvoiceTest que demonstra as capacidades da classe Invoice.

3.13 (Classe Employee) Crie uma classe chamada Employee que inclua três variáveis de instância — um primeiro nome (tipo String), um sobrenome (tipo String) e um salário mensal (double). Forneça um construtor que inicializa as três variáveis de instância. Forneça um método set e um get para cada variável de instância. Se o salário mensal não for positivo, não configure seu valor. Escreva um aplicativo de teste chamado EmployeeTest que demonstre as capacidades da classe Employee. Crie dois objetos Employee e exiba o salário anual de cada objeto. Então dê a cada Employee um aumento de 10% e exiba novamente o salário anual de cada Employee.

3.14 (Classe Date) Crie uma classe chamada Date que inclua três variáveis de instância — mês (tipo int), dia (tipo int) e ano (tipo int). Forneça um construtor que inicializa as três variáveis de instância supondo que os valores fornecidos estejam corretos. Ofereça um método set e um get para cada variável de instância. Apresente um método displayDate que exiba mês, dia e ano separados por barras normais (/). Escreva um aplicativo de teste chamado DateTest que demonstre as capacidades da classe Date.

3.15 (Removendo código duplicado no método main) Na classe AccountTest da Figura 3.9, o método main contém seis instruções (linhas 13 e 14, 15 e 16, 28 e 29, 30 e 31, 40 e 41 e 42 e 43) e cada uma exibe name e balance do objeto Account. Estude essas instruções e você perceberá que elas só diferem no objeto Account sendo manipulado — account1 ou account2. Neste exercício, você definirá um novo método displayAccount que contém uma cópia dessa instrução de saída. O parâmetro do método será um objeto Account e o método irá gerar name e balance dele. Então você substituirá as seis instruções duplicadas em main por chamadas para displayAccount passando como argumento o objeto específico Account para saída.

Modifique a classe AccountTest da Figura 3.9 para declarar o seguinte método displayAccount após a chave direita de fechamento de main e antes da chave direita de fechamento da classe AccountTest:

```
public static void displayAccount(Account accountToDisplay)
{
    // coloque aqui a instrução que exibe
    // o name e o balance de accountToDisplay
}
```

Substitua o comentário no corpo do método por uma instrução que exiba name e balance de accountToDisplay. 

Lembre-se de que main é um método static, assim pode ser chamado sem antes criar um objeto da classe em que é declarado. Também declaramos o método displayAccount como um método static. Quando main tem de chamar outro método na mesma classe sem antes criar um objeto dela, o outro método também deve ser declarado static.

Depois de concluir a declaração de displayAccount, modifique main para substituir as instruções que exibem name e balance de cada Account pelas chamadas para displayAccount — cada uma recebendo como seu argumento o objeto account1 ou account2, como apropriado. Então, teste a classe AccountTest atualizada para garantir que ela produz a mesma saída como mostrado na Figura 3.9.


## Fazendo a diferença

3.16 (Calculadora de frequência cardíaca alvo) Ao fazer exercícios físicos, você pode utilizar um monitor de frequência cardíaca para ver se sua frequência permanece dentro de um intervalo seguro sugerido pelos seus treinadores e médicos. Segundo a American Heart Association (AHA) (www.americanheart.org/presenter.jhtml?identifier=4736), a fórmula para calcular a frequência cardíaca máxima por minuto é 220 menos a idade em anos. Sua frequência cardíaca alvo é um intervalo entre 50-85% da sua frequência cardíaca máxima. 

[Observação: essas fórmulas são estimativas fornecidas pela AHA. As frequências cardíacas máximas e alvo podem variar com base na saúde, capacidade física e sexo da pessoa. Sempre consulte um médico ou profissional de saúde qualificado antes de começar ou modificar um programa de exercícios físicos.] 

Crie uma classe chamada HeartRates. Os atributos da classe devem incluir o nome, sobrenome e data de nascimento da pessoa (consistindo em atributos separados para mês, dia e ano de nascimento). Sua classe deve ter um construtor que receba esses dados como parâmetros. Para cada atributo forneça métodos set e get. 

A classe também deve incluir um método que calcule e retorne a idade (em anos), um que calcule e retorne a frequência cardíaca máxima e um que calcule e retorne a frequência cardíaca alvo da pessoa. Escreva um aplicativo Java que solicite as informações da pessoa, instancie um objeto da classe HeartRates e imprima as informações a partir desse objeto — incluindo nome, sobrenome e data de nascimento da pessoa — calcule e imprima a idade da pessoa (em anos), seu intervalo de frequência cardíaca máxima e sua frequência cardíaca alvo.


3.17 (Computadorização dos registros de saúde) Uma questão relacionada à assistência médica discutida ultimamente nos veículos de comunicação é a computadorização dos registros de saúde. Essa possibilidade está sendo abordada de maneira cautelosa por causa de preocupações quanto à privacidade e à segurança de dados sigilosos, entre outros motivos. 

[Iremos discutir essas preocupações em exercícios posteriores.] A computadorização dos registros de saúde pode facilitar que pacientes compartilhem seus perfis e históricos de saúde entre vários profissionais de saúde. Isso talvez aprimore a qualidade da assistência médica, ajude a evitar conflitos e prescrições erradas de medicamentos, reduza custos em ambulatórios e salve vidas. Neste exercício, você projetará uma classe HealthProfile “inicial” para uma pessoa. Os atributos da classe devem incluir nome, sobrenome, sexo, data de nascimento (consistindo em atributos separados para mês, dia e ano de nascimento), altura (em metros) e peso (em quilogramas) da pessoa. Sua classe deve ter um construtor que receba esses dados.

Para cada atributo, forneça métodos set e get. A classe também deve incluir métodos que calculem e retornem a idade do usuário em anos, intervalo de frequência cardíaca máxima e frequência cardíaca alvo (veja o Exercício 3.16), além de índice de massa corporal (IMC; veja o Exercício 2.33). Escreva um aplicativo Java que solicite as informações da pessoa, instancie um objeto da classe HealthProfile para ela e imprima as informações a partir desse objeto — incluindo nome, sobrenome, sexo, data de nascimento, altura e peso da pessoa ––, e então calcule e imprima a idade em anos, IMC, intervalo de frequência cardíaca máxima e frequência cardíaca alvo. Ele também deve exibir o gráfico de valores IMC do Exercício 2.33.










