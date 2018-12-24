## Exercícios de revisão

23.1 Preencha as lacunas em cada uma das seguintes afirmações:

a) Uma thread entra no estado terminado quando ________.

b) Para pausar um número designado de milissegundos e retomar a execução, uma thread deve chamar o método ________ da classe ________.

c) Uma thread executável pode entrar no estado ________ por um intervalo especificado de tempo.

d) No nível do sistema operacional, o estado executável realmente inclui dois estados separados, ________ e ________.

e) Runnables são executadas utilizando uma classe que implementa a interface ________.

f) O método ExecutorService ________ termina cada thread em uma interface ExecutorService logo que terminar de executar sua Runnable atual, se houver alguma.

g) Em um relacionamento ________, o ________ gera dados e armazena-os em um objeto compartilhado, e o ________ lê os dados do objeto compartilhado.

h) A palavra-chave ________ indica que somente uma thread por vez deve executar em um objeto.


23.2 (Seções opcionais avançadas) Preencha os espaços em branco em cada uma das seguintes instruções:

a) O método ________ da classe Condition move uma única thread no estado de espera de um objeto para o estado executável.

b) O método ________ da classe Condition move toda thread no estado de espera de um objeto para o estado executável.

c) Uma thread pode chamar o método ________ em um objeto Condition para liberar o Lock associado e colocar essa thread no estado ________.

d) A classe ________ implementa a interface BlockingQueue que utiliza um array.

e) O método ________ static da classe Instant começa a data/hora atual.

f) O método Duration ________ retorna a Duration como valor long em milissegundos.

g) O método NumberFormat static ________ retorna um NumberFormat que é usado para formatar um número como uma porcentagem.

h) O método NumberFormat ________ retorna uma representação String de seu argumento no formato numérico especificado.

i) O método Arrays static ________ preenche um array com os valores produzidos por uma função de gerador.

j) O método Arrays static ________ aplica uma BinaryOperator ao elemento atual e os elementos anteriores do array e armazena

o resultado no elemento atual.

k) Para obter um fluxo paralelo, basta invocar o método ________ em um fluxo existente.

l) Entre seus muitos recursos, um CompletableFuture permite executar assincronamente ________ que realiza tarefas ou ________ que retornam valores.


23.3 Determine se cada um dos seguintes itens é verdadeiro ou falso. Se falso, explique por quê.

a) Uma thread não é executável se tiver terminado.

b) Alguns sistemas operacionais utilizam fracionamento de tempo com threads. Portanto, eles podem permitir que as threads façam preempção de threads da mesma prioridade.

c) Quando o quantum da thread expira, a thread retorna ao estado de execução enquanto o sistema operacional a atribui a um processador.

d) Em um sistema de processador único sem divisão do tempo, cada thread em um conjunto de threads com prioridade igual (sem nenhuma outra thread presente) é executada até a conclusão antes que outras threads com prioridade igual tenham a oportunidade de executar.


23.4 (Seções opcionais avançadas) Determine se cada uma das seguintes instruções é verdadeira ou falsa. Se falsa, explique por quê.

a) Para determinar a diferença entre dois Instants, use o método static difference da classe Duration que retorna um objeto Duration contendo a diferença de data/hora.

b) Fluxos são fáceis de paralelizar, permitindo que os programas se beneficiem de melhor desempenho em sistemas multiprocessados.

c) A interface Supplier, como a interface Callable, é uma interface funcional com um único método que não recebe argumentos e retorna um resultado.

d) O método CompletableFuture static runAsync executa assincronamente uma tarefa Supplier que retorna um valor.

e) O método CompletableFuture static supplyAsync executa assincronamente uma tarefa Runnable que não retorna um resultado.


## Respostas dos exercícios de revisão

23.1 a) seu método run termina. b) sleep, Thread. c) espera sincronizada. d) pronto, em execução. e) Executor. f) shutdown.    
g) produtor/consumidor, produtor, consumidor. h) synchronized.    

23.2 a) signal. b) signalAll. c) await, em espera. d) ArrayBlockingQueue. e) now. f) toMillis. g) getPercentInstance.    
h) format. i) parallelSetAll. j) parallelPrefix. k) parallel. l) Runnables, Suppliers.    

23.3 a) Verdadeiro. b) Falso. Fracionamento de tempo permite uma thread executar até que sua fração de tempo (ou quantum) expire. Então outras threads de igual prioridade podem executar. c) Falsa. Quando o quantum de uma thread expira, a thread retorna ao estado pronto e o sistema operacional atribui ao processador outra thread. d) Verdadeira.

23.4 a) Falso. O método Duration para calcular a diferença entre dois Instants é chamado between. b) Verdadeiro. c) Verdadeiro. d) Falso. O método que executa assincronamente um Supplier é supplyAsync. e) Falso. O método que executa assincronamente um Runnable é runAsync.


## Questões

23.5 (Verdadeiro ou falso) Declare se cada uma das seguintes instruções é verdadeira ou falsa. Se falsa, explique por quê.

a) O método sleep não consome tempo de processador enquanto uma thread dorme.

b) Os componentes Swing são seguros para thread.

c) (Avançado) Declarar um método synchronized garante que o impasse não ocorra.

d) (Avançado) Uma vez que um ReentrantLock foi obtido por uma thread, o objeto ReentrantLock não permitirá que outra thread obtenha o bloqueio até que a primeira thread o libere.


23.6 (Termos de multithreading) Defina cada um dos seguintes termos.

a) thread

b) multithreading

c) estado executável

d) estado de espera sincronizada

e) agendamento preemptivo

f) interface Runnable

g) relacionamento produtor/consumidor

h) quantum


23.7 (Avançado: termos de Multithreading) Discuta cada um dos seguintes termos no contexto de mecanismos de thread do Java:

a) synchronized

b) wait

c) notify

d) notifyAll

e) Lock

f) Condition


23.8 (Estado bloqueado) Liste as razões para entrar no estado bloqueado. Para cada uma delas, descreva como o programa normalmente deixará o estado bloqueado e entrará no estado executável.


23.9 (Impasse e adiamento indefinido) Dois problemas que podem ocorrer em sistemas que permitem que as threads esperem são os impasses, em que uma ou mais threads esperarão eternamente por um evento que não pode ocorrer, e o adiamento indefinido, em que uma ou mais threads serão retardadas por um tempo imprevisivelmente longo. Dê um exemplo de como cada um desses problemas podem ocorrer em programas Java de múltiplas threads.


23.10 (Rebatendo a bola) Escreva um programa que faz uma bola azul rebater dentro de um JPanel. A bola deve começar a se mover com um evento mousePressed. Quando a bola atingir a borda do JPanel, ela deve rebater fora da borda e continuar na direção oposta. A bola deve ser atualizada com uma interface Runnable.


23.11 (Rebatendo bolas) Modifique o programa na Questão 23.10 para adicionar uma nova bola toda vez que o usuário clicar no mouse. Ofereça um mínimo de 20 bolas. Escolha a cor para cada nova bola aleatoriamente.

23.12 (Bolas rebatendo com sombras) Modifique o programa na Questão 23.11 para adicionar sombras. À medida que uma bola se mover, desenhe uma oval sólida preta na parte inferior do JPanel. Você pode considerar adicionar um efeito 3-D, aumentando ou diminuindo o tamanho de cada bola quando ela atingir a borda do JPanel.


23.13 (Avançado: buffer circular com Locks e Conditions) Reimplemente o exemplo na Seção 23.8 utilizando os conceitos Lock e Condition apresentados na Seção 23.9.

23.14 (Buffer limitado: um exemplo do mundo real) Descreva como a alça de acesso de uma rodovia para uma estrada local é um bom exemplo de um relacionamento produtor/consumidor com um buffer limitado. Em particular, discuta como os projetistas podem escolher o tamanho da alça de acesso.


## Fluxos paralelos

Para os exercícios 23.15 a 23.17, talvez você precise criar conjuntos de dados maiores para ver uma diferença significativa de desempenho.

23.15 (Resumindo as palavras em um arquivo) Reimplemente a Figura 17.17 usando fluxos paralelos. Use as técnicas de cronometragem da API Date/Time que você aprendeu na Seção 23.12 para comparar o tempo necessário para as versões sequenciais e paralelas do programa.

23.16 (Resumindo os caracteres em um arquivo) Reimplemente o Exercício 17.9 usando fluxos paralelos. Use as técnicas de cronometragem da API Date/Time que você aprendeu na Seção 23.12 para comparar o tempo necessário para as versões sequenciais e paralelas do programa.

23.17 (Resumindo os tipos de arquivo em um diretório) Reimplemente o Exercício 17.10 usando fluxos paralelos. Use as técnicas de cronometragem da API Date/Time que você aprendeu na Seção 23.12 para comparar o tempo necessário para as versões sequenciais e paralelas do programa.


