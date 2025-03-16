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
