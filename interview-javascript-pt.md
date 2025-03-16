### Sumário - Node JS

| No. | Perguntas |
| --- | --------- |
|   | **Node JS** |
| 1 | [O que é NodeJS?](#o-que-é-nodejs)|                                                                                                    
| 2 | [Como você pode evitar callback hells?](#como-você-pode-evitar-callback-hells)|                         
| 3 | [Quando processos em segundo plano ou worker são úteis?](#quando-processos-em-segundo-plano-ou-worker-são-úteis)|        
| 4 | [Por que o NodeJS é Single threaded?](#por-que-o-nodejs-é-single-threaded)|                                                                          
| 5 | [Cite os tipos de funções de API no Node?](#cite-os-tipos-de-funções-de-api-no-node)|                                                          
| 6 | [Explique o encadeamento (chaining) no Nodejs?](#explique-o-encadeamento-chaining-no-nodejs)|                                                                                
| 7 | [O que são streams no Nodejs? Explique os diferentes tipos de streams presentes no Nodejs?](#o-que-são-streams-no-nodejs-explique-os-diferentes-tipos-de-streams-presentes-no-nodejs) |
| 8 | [O que é package json?](#o-que-é-package-json)|                                                                                                       
| 9 | [Explique o propósito do module exports?](#explique-o-propósito-do-module-exports)|                                                           
| 10| [Liste as principais implementações de segurança no Node.js?](#liste-as-principais-implementações-de-segurança-no-nodejs)|                         
| 11| [Explique o conceito do módulo URL?](#explique-o-conceito-do-módulo-url)|                                        
| 12| [Explique o conceito de middleware no Nodejs?](#explique-o-conceito-de-middleware-no-nodejs)|                                            
| 13| [Explique o libuv?](#explique-o-libuv)|
| 14| [Liste os dois argumentos que async queue recebe como entrada?](#liste-os-dois-argumentos-que-async-queue-recebe-como-entrada) |
| 15| [Diferencie entre os métodos spawn e fork no Nodejs?](#diferencie-entre-os-métodos-spawn-e-fork-no-nodejs) |
| 16| [Explique o propósito do pacote ExpressJS?](#explique-o-propósito-do-pacote-expressjs) |
| 17| [Explique o uso da classe buffer no Nodejs?](#explique-o-uso-da-classe-buffer-no-nodejs) |
| 18| [Como o Nodejs lida com as threads filhas?](#como-o-nodejs-lida-com-as-threads-filhas) |
| 19| [Explique stream no Nodejs junto com seus vários tipos?](#explique-stream-no-nodejs-junto-com-seus-vários-tipos) |
| 20| [Descreva os códigos de saída do Nodejs?](#descreva-os-códigos-de-saída-do-nodejs) |
| 21| [A criptografia é suportada no Nodejs?](#a-criptografia-é-suportada-no-nodejs) |
| 22| [Explique o motivo pelo qual o aplicativo Express e a pasta do servidor devem ser mantidos separados?](#explique-o-motivo-pelo-qual-o-aplicativo-express-e-a-pasta-do-servidor-devem-ser-mantidos-separados) |
| 23| [Qual é o papel do módulo asset no nodejs?](#qual-é-o-papel-do-módulo-asset-no-nodejs) |
| 24| [Qual é o papel do módulo async_hooks no nodejs?](#qual-é-o-papel-do-módulo-async_hooks-no-nodejs) |
| 25| [O que são objetos buffer no nodejs?](#o-que-são-objetos-buffer-no-nodejs) |
| 26| [Quais são as diferentes maneiras de implementar Addons no NodeJS?](#quais-são-as-diferentes-maneiras-de-implementar-addons-no-nodejs) |
| 27| [Como podemos criar processos filhos de forma assíncrona sem bloquear o event loop do Nodejs?](#como-podemos-criar-processos-filhos-de-forma-assíncrona-sem-bloquear-o-event-loop-do-nodejs) |
| 28| [Como podemos aproveitar um sistema multi-core no Nodejs, já que o nodejs trabalha em thread única?](#como-podemos-aproveitar-um-sistema-multi-core-no-nodejs-já-que-o-nodejs-trabalha-em-thread-única) |
| 29| [Qual é o tipo de dados do console?](#qual-é-o-tipo-de-dados-do-console) |
| 30| [Quais são os diferentes métodos de console disponíveis?](#quais-são-os-diferentes-métodos-de-console-disponíveis) |
| 31| [O node js pode realizar funções criptográficas?](#o-node-js-pode-realizar-funções-criptográficas) |
| 32| [Como podemos ler ou escrever arquivos no node js?](#como-podemos-ler-ou-escrever-arquivos-no-node-js) |
| 33| [Quais são os objetos globais no Node JS?](#quais-são-os-objetos-globais-no-node-js) |
| 34| [Como podemos realizar API de rede assíncrona no Node JS?](#como-podemos-realizar-api-de-rede-assíncrona-no-node-js) |
| 35| [Quais são as utilidades do módulo OS no NodeJS?](#quais-são-as-utilidades-do-módulo-os-no-nodejs) |
| 36| [Quais são as áreas onde é adequado usar NodeJS?](#quais-são-as-áreas-onde-é-adequado-usar-nodejs) |
| 37| [Quais são as áreas onde não é adequado usar NodeJS?](#quais-são-as-áreas-onde-não-é-adequado-usar-nodejs) |
| 38| [Quais são as principais características do NodeJs?](#quais-são-as-principais-características-do-nodejs) |
| 39| [Explique REPL no NodeJs?](#explique-repl-no-nodejs) |
| 40| [Você pode escrever operações CRUD no Node js sem usar frameworks?](#você-pode-escrever-operações-crud-no-node-js-sem-usar-frameworks) |
| 41| [Você pode criar um servidor HTTP no Nodejs? Explique o código usado para isso?](#você-pode-criar-um-servidor-http-no-nodejs-explique-o-código-usado-para-isso) |
| 42| [Qual é a diferença entre Nodejs AJAX e JQuery?](#qual-é-a-diferença-entre-nodejs-ajax-e-jquery) |
| 43| [O que é EventEmitter no NodeJs?](#o-que-é-eventemitter-no-nodejs) |
| 44| [O que é um módulo Child_process no NodeJs?](#o-que-é-um-módulo-child_process-no-nodejs) |

## Node Js

1. ### O que é NodeJS?

Node.js é um ambiente de tempo de execução JavaScript de código aberto e multiplataforma que executa código JavaScript fora de um navegador**. O Node JS foi criado por [Ryan Dahl](https://github.com/ry), Ryan Dahl é um engenheiro de software e o desenvolvedor original do tempo de execução JavaScript do Node.js.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

2. ### Como você pode evitar callback hells?

Existem muitas maneiras de resolver o problema de callback hells: <br /> 1. modularização: divida os callbacks em funções independentes, <br /> 2. use uma biblioteca de fluxo de controle, como async. <br /> 3. use geradores com Promises, <br /> 4. use async/await (observe que ele só está disponível na versão v7 mais recente e não na versão LTS

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

3. ### Quando os processos de segundo plano ou de trabalho são úteis?

Os processos de trabalho são extremamente úteis se você quiser fazer processamento de dados em segundo plano, como enviar e-mails ou processar imagens.
<br/>
Existem muitas opções para isso, como RabbitMQ ou Kafka.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

4. ### Por que o NodeJS é single threaded?

O Node.js é single threaded para processamento assíncrono. Ao fazer processamento assíncrono em um único thread sob cargas típicas da web, mais desempenho e escalabilidade podem ser alcançados em oposição ao típico implementação baseada em thread.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

5. ### Nomeie os tipos de funções de API no Node?

Existem dois tipos de funções no Node.js. <br/>
1. Funções de bloqueio - Em uma operação de bloqueio, todo o outro código é bloqueado de execução até que um evento de E/S que está sendo aguardado ocorra. Funções de bloqueio são executadas de forma síncrona. <br/>2. Funções não bloqueantes - Em uma operação não bloqueante, várias chamadas de E/S podem ser realizadas sem que a execução do programa seja interrompida. Funções não bloqueantes são executadas de forma assíncrona.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

6. ### Explique o encadeamento no Nodejs?

O encadeamento é um mecanismo pelo qual a saída de um fluxo é conectada a outro fluxo, criando uma cadeia de várias operações de fluxo.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

7. ### O que são fluxos no Nodejs Explique os diferentes tipos de fluxos presentes no Nodejs?

Os fluxos são objetos que permitem a leitura de dados da origem e a gravação de dados no destino como um processo contínuo.<br/>
Existem quatro tipos de fluxos.<br/>
<Readable> para facilitar a operação de leitura.<br/>
<Writable> para facilitar a operação de gravação.<br/>
<Duplex> para facilitar as operações de leitura e gravação.<br/>
<Transform> é uma forma de fluxo Duplex que realiza cálculos com base na entrada disponível.<br/>

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

8. ### O que é o pacote json?

O arquivo package.json no Node.js é o coração de todo o aplicativo. É basicamente o arquivo manifesto que contém os metadados do projeto onde definimos as propriedades de um pacote.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

9. ### Explique o propósito das exportações de módulos?

Um módulo em Node.js é usado para encapsular todos os códigos relacionados em uma única unidade de código que pode ser interpretada deslocando todas as funções relacionadas em um único arquivo

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

10. ### Liste as principais implementações de segurança dentro do Nodejs?

As principais implementações de segurança no Node.js são: Autenticações, Tratamento de erros

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

11. ### Explique o conceito de módulo de URL?

O módulo URL divide um endereço da web em partes legíveis

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

12. ### Explique o conceito de middleware no Nodejs?

Em geral, o middleware é uma função que recebe os objetos Request e Response. Em outras palavras, no ciclo de solicitação-resposta de um aplicativo, essas funções têm acesso a vários objetos de solicitação e resposta junto com a próxima função do ciclo. A próxima função do middleware é representada com a ajuda de uma variável, geralmente chamada next. As tarefas mais comumente executadas pelas funções do middleware são <br/>

Executar qualquer tipo de código<br/>
Atualizar ou modificar a solicitação e os objetos de resposta<br/>
Concluir o ciclo de solicitação-resposta<br/>
Invocar o próximo middleware na pilha

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

13. ### Explique a libuv?

Libuv é uma biblioteca de suporte multiplataforma do Node.js que é usada principalmente para E/S assíncronas. Foi desenvolvida principalmente para Node.js, com o tempo é popularmente praticada com outros sistemas como Luvit, pyuv, Julia, etc. Libuv é basicamente uma abstração em torno de libev/IOCP dependendo da plataforma, fornecendo aos usuários uma API baseada em libev. Alguns dos recursos importantes do libuv são: <br/>

Loop de eventos com todos os recursos suportados<br/>
Eventos do sistema de arquivos<br/>
Operações assíncronas de arquivo e sistema de arquivo<br/>
Assíncrono sockets TCP e UDP horonous<br/>
Processos filhos

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

14. ### Liste os dois argumentos que async.queue recebe como entrada?

Abaixo estão os dois argumentos que async.queue recebe como entrada - Tarefa Função e Valor de Simultaneidade

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

15. ### Diferenciar entre métodos spawn e fork no Nodejs?

No Node.js, o spawn() é usado para iniciar um novo processo com o conjunto de comandos fornecido. Este método não cria uma nova instância V8 e apenas uma cópia do módulo node está ativa no processador. Quando seu processo filho retorna uma grande quantidade de dados para o Node, você pode invocar este método.

**[ Voltar ao topo ⬆ ](#tabela-de-conteúdos---node-js)**

16. ### Explique o propósito do pacote ExpressJS?

Express.js é uma estrutura construída sobre o Node.js que facilita o gerenciamento do fluxo de dados entre o servidor e as rotas nos aplicativos do lado do servidor. É uma estrutura leve e flexível que fornece uma ampla gama de recursos necessários para o desenvolvimento de aplicativos da web e móveis. O Express.js é desenvolvido no módulo de middleware do Node.js chamado connect. O módulo connect também faz uso do módulo http para se comunicar com o Node.js. Portanto, se você estiver trabalhando com qualquer um dos módulos de middleware baseados em connect, poderá integrar facilmente com o Express.js.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

17. ### Explique o uso de uma classe de buffer no Nodejs?

A classe de buffer no Node.js é usada para armazenar dados brutos de maneira semelhante a uma matriz de inteiros. Mas corresponde a uma alocação de memória bruta que está localizada fora do heap V8. É uma classe global que é facilmente acessível e pode ser acessada em um aplicativo sem importar um módulo de buffer. A classe Buffer é usada porque o JavaScript puro não é compatível com dados binários. Então, ao lidar com fluxos TCP ou o sistema de arquivos, é necessário lidar com fluxos de octetos.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

18. ### Como o Nodejs lida com os threads filhos?

Em geral, o Node.js é um processo de thread única e não expõe os threads filhos ou métodos de gerenciamento de threads. Mas você ainda pode usar os threads filhos usando spawn() para algumas tarefas de E/S assíncronas específicas que são executadas em segundo plano e geralmente não executam nenhum código JS ou atrapalham o loop de eventos principal no aplicativo. Se você ainda quiser usar o conceito de threading em seu aplicativo, você tem que incluir um módulo chamado ChildProcess explicitamente.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

19. ### Explique o fluxo no Nodejs junto com seus vários tipos?

Os fluxos no Node.js são a coleção de dados semelhantes a matrizes e strings. Eles são objetos usando os quais você pode ler dados de uma fonte ou gravar dados em um destino de forma contínua. Eles podem não estar disponíveis imediatamente e não precisam caber na memória. Esses fluxos são especialmente úteis para ler e processar um grande conjunto de dados. No Node.js, há quatro tipos fundamentais de fluxos:<br/>
Legível: Usado para ler grandes blocos de dados da fonte.<br/>
Gravável: Usado para gravar grandes blocos de dados no destino.<br/>
Duplex: Usado para ambas as funções; ler e gravar.<br/>
Transformar: É um fluxo duplex usado para modificar os dados.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

20. ### Descreva os códigos de saída do Nodejs?

No Node.js, os códigos de saída são um conjunto de códigos específicos que são usados ​​para finalizar um processo específico. Esses processos podem incluir o objeto global também. Abaixo estão alguns dos códigos de saída usados ​​no Node.js:<br/>
*Exceção fatal não capturada<br/>
*Não utilizado<br/>
*Erro fatal<br/>
*Falha de tempo de execução do manipulador de exceção interna<br/>
*Falha de avaliação interna do JavaScript<br/>

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

21. ### A criptografia é suportada no Nodejs?

Sim, o Node.js suporta criptografia por meio de um módulo chamado Crypto. Este módulo fornece várias funcionalidades criptográficas como cifrar, decifrar, assinar e verificar funções, um conjunto de wrappers para hash HMAC de SSL aberto etc.<br/>

```
const crypto = require'crypto');
const secret = 'akerude';
const hash = crypto.createHmac('swaEdu', secret).update('Welcome to Edureka').digest('hex');
console.log(hash);

```

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

22. ### Explique o motivo pelo qual o aplicativo Express e a pasta do servidor devem ser mantidos separados?

Express ‘app’ e ‘server’ devem ser mantidos separados, pois ao fazer isso, você estará separando a declaração da API da configuração relacionada à rede, o que se beneficia das maneiras listadas abaixo:<br/>
*Permite testar a API em andamento sem precisar executar as chamadas de rede<br/>
*Execução de teste mais rápida<br/>
*Obter métricas de cobertura mais amplas do código<br/>
*Permite implantar a mesma API em condições de rede flexíveis e diferentes<br/>
*Melhor separação de preocupações e código mais limpo

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

23. ### Qual é a função do módulo asset no nodejs?

O módulo assert fornece um conjunto de funções de asserção para verificar invariantes

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

24. ### Qual é a função do módulo async_hooks no nodejs?

O módulo async_hooks fornece uma API para rastrear recursos assíncronos. Ele pode ser acessado usando:
```
const async_hooks = require('async_hooks');
```

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

25. ### O que são objetos buffer no nodejs?

No Node.js, os objetos Buffer são usados ​​para representar dados binários na forma de uma sequência de bytes. Muitas APIs do Node.js, por exemplo, transmitem um d operações do sistema de arquivos, suportam Buffers, pois as interações com o sistema operacional ou outros processos geralmente sempre acontecem em termos de dados binários

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

26. ### Quais são as diferentes maneiras de implementar Addons no NodeJS?

Existem três opções para implementar Addons: <br/>N-API<br/> nan uso direto de V8 interno <br/> libuv <br/> bibliotecas Node.js

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

27. ### Como podemos gerar o processo filho de forma assíncrona sem bloquear o loop de eventos do Nodejs?

O método **child_process.spawn()** gera o processo filho de forma assíncrona, sem bloquear o loop de eventos do Node.js,O child_process. <br/>A função **spawnSync()** fornece funcionalidade equivalente de forma síncrona que bloqueia o loop de eventos até que o processo gerado saia ou seja encerrado

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

28. ### Como podemos aproveitar o sistema multi-core no Nodejs, já que o nodejs funciona em thread única?

Podemos usar o cluster node js para usar multicores no hardware. O módulo cluster permite a criação fácil de processos filhos que compartilham portas de servidor<br/>
```
const cluster = require('cluster');
const http = require('http');
const numCPUs = require('os').cpus().length;

if (cluster.isMaster) {
console.log(`Master ${process.pid} is running`);

// Bifurcar trabalhadores.
para (deixe i = 0; i < numCPUs; i++) {
cluster.fork();
}

cluster.on('exit', (worker, code, signal) => {
console.log(`worker ${worker.process.pid} died`);
});
}
else {
// Os workers podem compartilhar qualquer conexão TCP
// Neste caso, é um servidor HTTP
http.createServer((req, res) => {
res.writeHead(200);
res.end('hello world\n');
}).listen(8000);

console.log(`Worker ${process.pid} started`);
}

//Executar o Node.js agora compartilhará a porta 8000 entre os workers:

$ node server.js
Master 3596 está em execução
Worker 4324 iniciado
Worker 4520 iniciado
Worker 6056 iniciado
Worker 5644 iniciado
```

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

29. ### Qual é o tipo de dados do console?

O tipo de dados do console é um **objeto**

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

30. ### Quais são os diferentes métodos de console disponíveis?

Existem cerca de 21 métodos de console embutidos, também podemos construir nossos próprios protótipos usando a nova função de construtor de console<br/>
aqui estão alguns populares<br/>
1.**console.clear()** limpará apenas a saída na janela de visualização do terminal atual para o binário Node.js.<br/>
2.**console.error([data][, ...args])** Imprime em stderr com nova linha. Vários argumentos podem ser passados, com o primeiro usado como a mensagem primária e todos os adicionais usados ​​como substituição<br/>
3.**console.table(tabularData[, properties])** uma tabela com as colunas das propriedades de tabularData (ou usar propriedades) e linhas de tabularData e registrá-la.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

31. ### O node js pode executar funções criptográficas?

Sim, o módulo crypto fornece funcionalidade criptográfica que inclui um conjunto de wrappers para as funções hash, HMAC, cipher, decipher, sign e verify do OpenSSL.<br/>

Use require('crypto') para acessar este módulo.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

32. ### Como podemos ler ou escrever arquivos no node js?

O módulo fs fornece uma API para interagir com o sistema de arquivos de uma maneira modelada de perto em torno das funções POSIX padrão.
Para usar este módulo:<br/>

const fs = require('fs');<br/>
Existem alguns métodos como
<br/>fs.readFile(file, data[, options], callback)
<br/>fs.writeFile(file, data[, options], callback)

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

33. ### Quais são os objetos globais no Node JS?

__dirname<br/>
__filename<br/>
clearImmediate(objetoimediato)<br/>
clearInterval(objetointervalo)<br/>
clearTimeout(objetotempo limite)<br/>
console<br/>
exports<br/>
global<br/>
module<br/>
process<br/>
queueMicrotask(retorno de chamada)<br/>
require()<br/>
setImmediate(retorno de chamada[, ...args])<br/>
setInterval(retorno de chamada, atraso[, ...args])<br/>
setTimeout(retorno de chamada, atraso[, ...args])<br/>
TextDecoder<br/>
TextEncoder<br/>
URL<br/>
URLSearchParams<br/>
WebAssembly<br/>

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

34. ### Como podemos executar API de rede assíncrona no Node JS?

O módulo net fornece uma API de rede assíncrona para criar servidores TCP ou IPC baseados em fluxo (net.createServer()) e clientes (net.createConnection()).

Ele pode ser acessado usando:
<br/>

const net = require('net');

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

35. ### Quais são os utilitários do módulo OS no NodeJS?

O módulo os fornece métodos e propriedades de utilitários relacionados ao sistema operacional. Ele pode ser acessado usando:<br/>

const os = require('os');.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

36. ### Quais são as áreas onde é adequado usar o NodeJS?

Aplicativos vinculados a E/S<br/>
Aplicativos de streaming de dados<br/>
Aplicativos em tempo real com uso intensivo de dados (DIRT)<br/>
Aplicativos baseados em APIs JSON<br/>
Aplicativos de página única<br/>
.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

37. ### Quais são as áreas onde não é adequado usar o NodeJS?

não é adequado para aplicativos pesados ​​que envolvam mais uso de CPU

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

38. ### Quais são os principais recursos do NodeJS?

**Evento assíncrono orientado a E/S** ajuda no tratamento de solicitações simultâneas – Todas as APIs do Node.js são assíncronas. Esse recurso significa que se um Node receber uma solicitação para alguma operação de entrada/saída, ele executará essa operação em segundo plano e continuará com o processamento de outras solicitações. Portanto, ele não esperará pela resposta das solicitações anteriores.<br/>
**Rápido na execução do código** – O Node.js usa o mecanismo de tempo de execução V8 JavaScript, o mesmo usado pelo Google Chrome. O Node tem um wrapper sobre o mecanismo JavaScript que torna o mecanismo de tempo de execução muito mais rápido e, portanto, o processamento de solicitações dentro do Node.js também se torna mais rápido.<br/>
**Single Threaded, mas altamente escalável** – O Node.js usa um modelo de thread único para loop de eventos. A resposta desses eventos pode ou não chegar ao servidor imediatamente. No entanto, isso não bloqueia outras operações. Tornando o Node.js altamente escalável. Servidores tradicionais criam threads limitados para lidar com solicitações, enquanto o Node.js cria uma única thread que fornece serviço para um número muito maior dessas solicitações.<br/>
**A biblioteca Node.js usa JavaScript** – Este é outro aspecto importante do Node.js do ponto de vista do desenvolvedor. A maioria dos desenvolvedores já é bem versada em JavaScript. Portanto, o desenvolvimento em Node.js se torna mais fácil para um desenvolvedor que conhece JavaScript.<br/>
**Há uma comunidade ativa e vibrante para o framework Node.js** – A comunidade ativa sempre mantém o framework atualizado com as últimas tendências no desenvolvimento web.<br/>
**Sem buffer** – Os aplicativos Node.js nunca armazenam dados em buffer. Eles simplesmente produzem os dados em blocos.<br/>
.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

39. ### Explique REPL em NodeJs?

REPL significa “Read Eval Print Loop”. É um programa simples que aceita os comandos, os avalia e finalmente imprime os resultados. O REPL fornece um ambiente semelhante ao do shell Unix/Linux ou um console de janela, no qual podemos digitar o comando e o sistema, por sua vez, responde com a saída. O REPL executa as seguintes tarefas.<br/>

**READ** - Lê a entrada do usuário, analisa-a na estrutura de dados JavaScript e, em seguida, armazena-a na memória.<br/>
**EVAL** - Executa a estrutura de dados.<br/>
**PRINT** - Imprime o resultado obtido após avaliar o comando.<br/>
**LOOP** - Faz um loop no comando acima até que o usuário pressione Ctrl+C duas vezes.<br/>

.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**?

40. ### Você pode escrever operações CRUD em Node js sem usar frameworks?

Sim, podemos usar a biblioteca http interna para isso, aqui está um código simples para o mesmo:
```
var http = require('http');//criar um objeto de servidor:
http.createServer(function (req, res) {
res.writeHead(200, {'Content-Type': 'text/html'}); // cabeçalho httpvar url = req.url;
if(url ==='/about'){
res.write('<h1>página sobre nós<h1>'); //escrever uma resposta
res.end(); //terminar a resposta
}else if(url ==='/contact'){
res.write('<h1>página de contato<h1>'); //escrever uma resposta
res.end(); //terminar a resposta
}else{
res.write('<h1>Olá Mundo!<h1>'); //escrever uma resposta
res.end(); //terminar a resposta
}}).listen(3000, function(){
console.log("server start at port 3000"); //the server object listens on port 3000
});
```

.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

42. ### Qual é a diferença entre Nodejs AJAX e JQuery?

A única característica comum entre Node.js, AJAX e jQuery é que todos eles são a implementação avançada do JavaScript. No entanto, eles atendem a propósitos completamente diferentes.<br/>

**Node.Js** :<br/>

É uma plataforma do lado do servidor para desenvolver aplicativos cliente-servidor. Por exemplo, se tivermos que construir um sistema de gerenciamento de funcionários on-line, não faremos isso usando JS do lado do cliente. Mas o Node.js certamente pode fazer isso, pois ele roda em um servidor semelhante ao Apache, Django, não em um navegador.<br/>

**AJAX** (também conhecido como Javascript e XML assíncronos):<br/>

É uma técnica de script do lado do cliente, projetada principalmente para renderizar o conteúdo de uma página sem atualizá-la. Há um número de grandes empresas que utilizam AJAX, como Facebook e Stack Overflow, para exibir conteúdo dinâmico.<br/>

**JQuery**:<br/>

É um módulo JavaScript famoso que complementa AJAX, travessia de DOM, looping e assim por diante. Esta biblioteca fornece muitas funções úteis para ajudar no desenvolvimento de JavaScript. No entanto, não é obrigatório usá-lo, mas como ele também gerencia a compatibilidade entre navegadores, pode ajudá-lo a produzir aplicativos da web altamente sustentáveis.<br/>

.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

43. ### O que é EventEmitter no NodeJs?

O módulo Events no Node.js nos permite criar e manipular eventos personalizados. O módulo Event contém a classe “EventEmitter” que pode ser usada para gerar e manipular eventos personalizados. Ele pode ser acessado pelo código a seguir.<br/>
```
// Importar módulo events
var events = require('events');

// Criar um objeto eventEmitter
var eventEmitter = new events.EventEmitter();
```
<br/>
Quando uma instância EventEmitter encontra um erro, ela emite um evento “error”. Quando um novo listener é adicionado, ele dispara um evento “newListener” e quando um listener é removido, ele dispara um evento “removeListener”.

EventEmitter fornece várias propriedades como “on” e “emit”. A propriedade “on” é usada para vincular uma função ao evento e “emit” é usada para disparar um evento.
.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

44. ### O que é um módulo Child_process no NodeJs?

O Node.js suporta a criação de processos filhos para ajudar no processamento paralelo junto com o modelo orientado a eventos.<br/>

Os processos filhos sempre têm três fluxos <child.stdin>, child.stdout e child.stderr. O fluxo <stdio> do processo pai compartilha os fluxos do processo filho.<br/>

O Node.js fornece um módulo <child_process> que suporta os três métodos a seguir para criar um processo filho.<br/>

**exec** – o método <child_process.exec> executa um comando em um shell/console e armazena a saída em buffer.
**spawn** – <child_process.spawn> inicia um novo processo com um comando fornecido.
**fork** – <child_process.fork> é um caso especial do método spawn() para criar processos filhos.

**[ Voltar ao topo ⬆ ](#table-of-contents---node-js)**

### Índice - Express JS

| No. | Perguntas |
| --- | --------- |
| | **Express JS** |
| 1 | [O que é ExpressJS?](#o-que-e-expressjs)|
| 2 | [Quais são alguns dos recursos mais importantes do express?](#quais-são-alguns-dos-recursos-mais-importantes-do-express)|
| 3 | [Explique com um exemplo o funcionamento de um aplicativo express simples?](#explique-com-um-exemplo-o-funcionamento-de-um-aplicativo-express-simples)|
| 4 | [Mencione algumas propriedades do parâmetro de solicitação no express?](#mencione-algumas-propriedades-do-parâmetro-de-solicitação-no-express)|
| 5 | [Como obter os parâmetros de nome no express?](#como-obter-os-parâmetros-de-nome-no-express)|
| 6 | [Como recuperar os parâmetros da string de consulta get usando express? ?](#como-recuperar-os-parâmetros-da-string-de-consulta-get-usando-express)|
| 7 | [Como enviar uma resposta de volta usando express?](#como-enviar-uma-resposta-de-volta-usando-express)|
| 8 | [Como definir o status de resposta http usando express?](#como-definir-status-de-resposta-http-usando-express)|
| 9 | [Quais são os diferentes códigos de status http?](#quais-são-os-diferentes-códigos-de-status-http)|
| 10 | [Mencione algumas propriedades do parâmetro de solicitação no express?](#mencione-algumas-propriedades-do-parâmetro-de-solicitação-no-express)|
| 11 | [Como você pode alterar o valor do cabeçalho http de uma resposta?](#how-can-you-change-http-header-value-of-a-response)|
| 12 | [Como redirecionar para outras páginas do lado do servidor?](#how-to-redirect-to-other-pages-server-side)|
| 13 | [Como o roteamento funciona no express?](#how-does-routing-work-in-express)|
| 14 | [Quais são as tarefas que um middleware pode fazer?](#what-are-the-tasks-that-a-middleware-can-do)|
| 15 | [Quais são os diferentes tipos de middleware?](#what-are-the-different-types-of-middleware)|
| 16 | [Como servir ativos estáticos do express? ](#how-to-serve-static-assests-from-express)|
| 17 | [Como fornecer download de arquivo usando express?](#como-fornecer-download-de-arquivo-usando-express)|
| 18 | [Como usar o método Response.cookie() para manipular seus cookies?](#como-usar-o-método-response-cookie-()-para-manipular-seus-cookies)|
| 19 | [Como gerenciar sessões usando express?](#como-gerenciar-sessões-usando-express)|
| 20 | [Como fornecer download de arquivo usando express?](#como-fornecer-download-de-arquivo-usando-express)|
| 21 | [Como permitir CORs no Expressjs, explique com um exemplo?](#como-permitir-cors-no-expressjs--explique-com-um-exemplo)|

## Express Js

1. ### O que é ExpressJS?

Framework web rápido, imparcial e minimalista para Node.js, Express é um projeto da Node.js Foundation. É de código aberto e clique [aqui](https://github.com/expressjs/express/) para visualizar, é usado principalmente para construir serviços de rede (aplicativos web) e aplicativos, é construído sobre os recursos do node js para fornecer funcionalidade fácil de usar que satisfaça as necessidades de construção de aplicativos web. Ele tem muitos pacotes pré-construídos e também muitos frameworks são construídos sobre ele como <br/>
**Feathers**: Crie protótipos em minutos e aplicativos em tempo real prontos para produção em dias<br/>
**NestJs**: Um framework Node.js progressivo para construir aplicativos eficientes, escaláveis ​​e de nível empresarial do lado do servidor sobre TypeScript e JavaScript (ES6, ES7, ES8)<br/>
**Sails**: Framework MVC para Node.js para construir aplicativos práticos e prontos para produção.<br/>

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

2. ### Quais são alguns dos recursos mais importantes do express?

**Middlewares**: Configure middlewares para responder a solicitações HTTP/RESTful.<br/>
**Roteamento**: É possível definir uma tabela de roteamento para executar diferentes operações HTTP.<br/>
**Modelos**: Renderiza dinamicamente páginas HTML com base na passagem de argumentos para modelos.<br/>
**Alto desempenho**: O Express prepara uma camada fina, portanto, o desempenho é adequado.<br/>
**Suporte a banco de dados**: O Express oferece suporte a RDBMS e bancos de dados NoSQL.<br/>
**Suporte a MVC**: Organize o aplicativo da web em uma arquitetura MVC.
**Gerencia tudo, desde rotas** até a renderização da visualização e execução de requisições HTTP.<br/>

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

3. ### Explique com um exemplo o funcionamento de um aplicativo express simples?

Eu lhe dei o código, você explica, não espere que eu faça tudo

```
const express = require('express')
const port = 3000
const app = express()
app.get('/', function(req, res) {
res.send('Hello World!')
})
app.listen(port, function(){
console.log('listening on port',port)
})
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

4. ### Mencione algumas propriedades do parâmetro de requisição no express?

aqui está uma lista de alguns métodos req necessários para você saber
![métodos req](/img/express_req_methods.png)

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

5. ### Como obter os parâmetros de nome no express?

Esta propriedade é um objeto que contém propriedades mapeadas para a rota nomeada “parâmetros”. Por exemplo, se você tiver a rota /user/:name, então a propriedade “name” estará disponível como req.params.name. Este objeto tem como padrão {}.
```
// GET /user/tj
req.params.name
// => "tj"
```
**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

6. ### Como recuperar os parâmetros da string de consulta get usando express?

A sequência de consulta é a parte que vem depois do caminho da URL e começa com um ponto de interrogação ?.
```
?height=6&weight=60
//req.query.height - 6
//req.query.weight - 60
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

7. ### Como enviar uma resposta de volta usando express?

podemos usar qualquer um desses comandos
```
function(req, res) {
res.send('Hello World!')
}
function(req, res) {
res.end('Hello World!')
}
function(req, res) {
res.json({title:'Hello World!'})
}
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

8. ### Como definir o status de resposta http usando express?

podemos usar **res.status()** ou **res.sendStatus()**
```
res.status(404).send('Arquivo não encontrado')

//se sendStatus não precisarmos escrever o método send, eu pré-enviarei algumas mensagens internas ao usar isso

res.sendStatus(200)
// === res.status(200).send('OK')

res.sendStatus(403)
// === res.status(403).send('Proibido')

res.sendStatus(404)
// === res.status(404).send('Não encontrado')

res.sendStatus(500)
// === res.status(500).send('Erro interno do servidor')
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

9. ### Quais são os diferentes códigos de status http?

| Código | Mensagem | Descrição |
| ---- | ------- | ------------------------------|
| 100|Continuar|Apenas uma parte da solicitação foi recebida pelo servidor, mas, desde que não tenha sido rejeitada, o cliente deve continuar com a solicitação|
|101|Alternando protocolos|O servidor alterna o protocolo|
|200 |OK|A solicitação está OK.|
|201 |Criado|A solicitação foi concluída e um novo recurso foi criado |
|202 |Aceito|A solicitação foi aceita para processamento, mas o processamento não foi concluído|
|203 |Informações não autoritativas|As informações no cabeçalho da entidade são de uma cópia local ou de terceiros, não do servidor original.|
|204 |Sem conteúdo|Um código de status e um cabeçalho são fornecidos na resposta, mas não há corpo de entidade na resposta|
|205 |Redefinir conteúdo|O navegador deve limpar o formulário usado para esta transação para entrada adicional|
|206 |Conteúdo parcial|O servidor está retornando ng dados parciais do tamanho solicitado. Usado em resposta a uma solicitação especificando um cabeçalho Range. O servidor deve especificar o intervalo incluído na resposta com o cabeçalho Content-Range|
|300 |Múltiplas opções|Uma lista de links. O usuário pode selecionar um link e ir para esse local. Máximo de cinco endereços|
|301 |Movido permanentemente|A página solicitada foi movida para uma nova url |
|302 |Encontrado|A página solicitada foi movida temporariamente para uma nova url|
|303 |Ver outro|A página solicitada pode ser encontrada em uma url diferente|
|304 |Não modificado|Este é o código de resposta para um cabeçalho If-Modified-Since ou If-None-Match, onde a URL não foi modificada desde a data especificada|
|305 |Usar proxy|A URL solicitada deve ser acessada por meio do proxy mencionado no cabeçalho Location|
|306 |Não utilizado|Este código foi usado em uma versão anterior. Não é mais usado, mas o código está reservado|
|307 |Redirecionamento temporário|A página solicitada foi movida temporariamente para uma nova URL|
|400 |Solicitação incorreta|O servidor não entendeu a solicitação|
|401 | Não autorizado|A página solicitada precisa de um nome de usuário e uma senha|
|402 | Pagamento obrigatório|Você não pode usar este código ainda.|
|403 |Proibido|O acesso à página solicitada é proibido.|
|404 |Não encontrado|O servidor não consegue encontrar a página solicitada.|
|405 |Método não permitido|O método especificado na solicitação não é permitido|
|406 |Não aceitável|O servidor só pode gerar uma resposta que não seja aceita pelo cliente|
|407 | Autenticação de proxy obrigatória|Você deve autenticar com um servidor proxy antes que esta solicitação possa ser atendida|
|408 |Tempo limite da solicitação|A solicitação levou mais tempo do que o servidor estava preparado para esperar|
|409 |Conflito|A solicitação não pôde ser concluída devido a um conflito|
|410 |Desaparecido|A página solicitada não está mais disponível|
|411 |Comprimento necessário|O "Content-Length" não está definido. O servidor não aceitará a solicitação sem ele.|
|412 |Falha na pré-condição|A pré-condição fornecida na solicitação foi avaliada como falsa pelo servidor|
|413 |Entidade da solicitação muito grande|O servidor não aceitará a solicitação porque a entidade da solicitação é muito grande.|
|414 |URL da solicitação muito longa|O servidor não aceitará a solicitação porque a URL é muito longa. Ocorre quando você converte uma solicitação "post" em uma solicitação "get" com uma informação de consulta longa|
|415 |Tipo de mídia não suportado|O servidor não aceitará a solicitação porque o tipo de mídia não é suportado |
|416 |Intervalo solicitado não satisfatório|O intervalo de bytes solicitado não está disponível e está fora dos limites|
|417 |Expectativa falhou|A expectativa fornecida em um campo de cabeçalho de solicitação Expect não pôde ser atendida por este servidor.|
|500 |Erro interno do servidor|A solicitação não foi concluída. O servidor atendeu a uma condição inesperada.|
|501 | Não implementado|A solicitação não foi concluída. O servidor não oferece suporte à funcionalidade necessária.|
|502 | Gateway inválido|A solicitação não foi concluída. O servidor recebeu uma resposta inválida do servidor upstream.|
|503 |Serviço indisponível|A solicitação não foi concluída. O servidor está temporariamente sobrecarregado ou inativo.|
|504 |Tempo limite do gateway|O tempo limite do gateway expirou.|
|505 |Versão HTTP não suportada|O servidor não oferece suporte à versão "protocolo http"|

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

10. ### Mencione algumas propriedades do parâmetro de solicitação no express?

Você pode acessar todos os cabeçalhos HTTP usando a propriedade Request.headers:
```
app.get('/', (req, res) => {
console.log(req.headers)
})

app.get('/', (req, res) => {
req.header('User-Agent')
})
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

11. ### Como você pode alterar o valor do cabeçalho http de uma resposta?

Você pode alterar qualquer valor de cabeçalho HTTP usando Response.set():
```
res.set('Content-Type', 'text/html')
res.type('json')
// => 'application/json'

res.type('application/json')
// => 'application/json'

res.type('png')
// => image/png:
```

**[ Voltar ao topo ⬆ ](#table-of-contents---express-js)**

