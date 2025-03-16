# Perguntas e respostas da entrevista de backend

## Nível iniciante

### O que é um ponto de extremidade de API?
Um ponto de extremidade de API é uma URL específica que atua como um ponto de entrada em um serviço específico ou uma funcionalidade dentro de um serviço.

Por meio de um ponto de extremidade de API, os aplicativos clientes podem interagir com o servidor enviando solicitações (às vezes até com dados na forma de carga útil) e receber uma resposta dele.

Normalmente, cada ponto de extremidade pode ser mapeado para um único recurso dentro do servidor.

### Você pode explicar a diferença entre bancos de dados SQL e NoSQL?
Os bancos de dados SQL (ou bancos de dados relacionais, como também são conhecidos) dependem de um esquema predefinido (ou estrutura) para seus dados. Sempre que você descreve um registro ou tabela dentro do banco de dados, você o faz por meio de seu formato (nome e campos).

Em bancos de dados NoSQL, não há esquema, portanto, não há estrutura predefinida para os dados. Você geralmente tem coleções de registros que não são obrigadas a ter a mesma estrutura, mesmo que representem conceitualmente a mesma coisa.

### O que é uma API RESTful e quais são seus princípios básicos?
Para uma API ser RESTful (o que significa que ela está em conformidade com as diretrizes REST), ela precisa:

- Ela precisa seguir uma arquitetura cliente-servidor (o que todos os serviços baseados em HTTP fazem).
- Ela precisa fornecer uma interface uniforme, o que significa:
- Deve haver uma maneira de identificar recursos uns dos outros por meio de URIs (Unique Resource Identification).
- Deve haver uma maneira de modificar recursos por meio de sua representação.
- As mensagens devem ser autodescritivas, o que significa que cada mensagem deve fornecer informações suficientes para entender como processá-la.
- Os clientes que usam a API devem ser capazes de descobrir ações disponíveis para o recurso atual usando a resposta fornecida pelo servidor (isso é conhecido como HATEOAS ou Hypermedia como o Engine of Application State).
- Ela precisa ser stateless, o que significa que cada solicitação ao servidor deve conter todas as informações para processar a solicitação.
- Deve ser um sistema em camadas, o que significa que o cliente e o servidor não precisam estar conectados diretamente um ao outro, pode haver intermediários, mas isso não deve afetar a comunicação entre o cliente e o servidor.
- Os recursos devem ser armazenáveis ​​em cache pelo cliente ou pelo servidor.
- Opcionalmente, o servidor pode enviar código ao cliente para que ele execute (conhecido como "Código sob Demanda").

### Você pode descrever um ciclo típico de solicitação/resposta HTTP?
O protocolo HTTP é muito estruturado e consiste em um conjunto muito bem definido de etapas:

1. **Abrir a conexão**: O cliente abre uma conexão TCP com o servidor. A porta será a porta 80 para conexões HTTP e 443 para conexões HTTPS (seguras).
2. **Enviar a solicitação**: O cliente agora enviará a solicitação HTTP ao servidor. A solicitação contém as seguintes informações:
- Um método HTTP. Pode ser qualquer um deles (por exemplo, GET, POST, PUT, DELETE, etc.).
- Um URI (ou Uniform Resource Identifier). Isso especifica a localização dos recursos no servidor.
- A versão HTTP (geralmente HTTP/1.1 ou HTTP/2).
- Um conjunto de cabeçalhos. Eles incluem dados extras relacionados à solicitação; há uma lista completa de cabeçalhos HTTP que podem ser usados ​​aqui.
- O corpo opcional. Dependendo do tipo de solicitação, você também desejará enviar dados, e os dados são codificados dentro do corpo da solicitação.
3. **Solicitação processada pelo servidor**: Nesta fase, o servidor processará a solicitação e preparará uma resposta.
4. **Enviar a resposta HTTP de volta ao cliente**: Por meio do canal aberto, o servidor envia de volta uma resposta HTTP. A resposta conterá os seguintes elementos:
- A versão HTTP.
- O código de status. Há uma lista de códigos de status potenciais que descrevem o resultado da solicitação.
- Um conjunto de cabeçalhos com dados extras.
- O corpo opcional, assim como com a solicitação, o corpo da resposta é opcional.
5. **A conexão está fechada**: Este é geralmente o último passo, embora com versões mais recentes do protocolo, há opções para deixar o canal aberto e continuar enviando solicitações e respostas de um lado para o outro.

### Como você lidaria com uploads de arquivos em um aplicativo da web?
Da perspectiva de um desenvolvedor de backend, as seguintes considerações devem ser levadas em conta ao lidar com uploads de arquivos, independentemente da linguagem de programação que você está usando:

- **Execute validações do lado do servidor**: Valide se o tamanho do seu arquivo está dentro do intervalo e se o arquivo é do tipo necessário. Você pode verificar o guia OWASP para mais detalhes.
- **Use canais seguros**: Certifique-se de que o upload do arquivo seja feito por meio de uma conexão HTTPS.
- **Evite colisão de nomes**: Renomeie o arquivo, garantindo que o novo nome do arquivo seja exclusivo em seu sistema. Caso contrário, isso pode levar a erros de aplicativo por não conseguir salvar os arquivos enviados.
- **Mantenha metadados sobre seus arquivos**: armazene-os em seu banco de dados ou em algum outro lugar, mas certifique-se de mantê-los sob controle, para que você possa fornecer informações extras aos seus usuários. Além disso, se você estiver renomeando os arquivos por segurança e para evitar colisões de nomes, mantenha o controle do nome do arquivo original, caso o arquivo precise ser baixado de volta pelo usuário.

### Que tipo de testes você escreveria para um novo endpoint de API?
Como desenvolvedores de backend, temos que pensar sobre os tipos de testes que existem por aí.

- **Testes unitários**: Lembre-se sempre de testar apenas a lógica relevante por meio da interface pública do seu código (evite testar métodos privados ou funções inacessíveis dentro dos seus módulos). Concentre-se na lógica de negócios e não tente testar o código que usa serviços externos (como um banco de dados, o disco ou qualquer coisa fora do pedaço de código que você está testando).
- **Testes de integração**: Teste o endpoint completo por meio de sua interface pública (o endpoint HTTP real) e veja como ele se integra aos serviços externos que está usando (por exemplo, o banco de dados, outra API, etc.).
- **Testes de carga/testes de desempenho**: Você também pode querer verificar como o novo endpoint se comporta sob forte estresse. Isso pode não ser necessário dependendo da API que você está usando, mas, como regra geral, é uma boa opção para executar no final da fase de desenvolvimento antes de liberar o novo endpoint para produção.

### Descreva como o gerenciamento de sessão funciona em aplicativos da web
A seguir, uma visão geral de alto nível de como o gerenciamento de sessão funciona para aplicativos da web:

1. **A sessão é criada**: Isso acontece com a primeira interação do usuário com o sistema (durante o login). O backend do seu aplicativo criará um ID de sessão exclusivo que será armazenado e retornado ao usuário para uso em solicitações futuras.
2. **Armazenamento de informações da sessão**: Os dados da sessão precisam ser armazenados em algum lugar. Seja na memória ou dentro de um banco de dados, eles precisam ser indexados pelo ID da sessão do ponto anterior. Aqui, a melhor opção é usar um banco de dados (de preferência algo como o Redis com alto desempenho de E/S) para que os serviços possam ser dimensionados independentemente dos dados da sessão.
3. **O ID da sessão é enviado ao cliente**: A maneira mais comum de fazer isso é por meio de cookies. O backend pode configurar um cookie com o ID da sessão e o frontend pode lê-lo com segurança e usar esse ID como for necessário.
4. **O cliente envia o ID da sessão**: Após a criação do ID, o aplicativo cliente se identificará com o backend usando esse ID em cada solicitação.
5. **Acessando os dados da sessão no backend**: O backend acessará os dados da sessão armazenados usando o ID da sessão recebido do cliente.
6. **A sessão é encerrada**: Depois de um tempo, ou talvez por meio de uma ação do usuário, o ID da sessão será excluído, o que fará com que os dados da sessão sejam perdidos (ou removidos do BD). Isso efetivamente encerra as interações entre o cliente e o servidor como parte da sessão existente.

### Como você aborda o versionamento de API em seus projetos?
Existem várias maneiras de lidar com o versionamento de API, mas as mais comuns são:

- **Manter a versão na URL**: como um atributo de URL (por exemplo, /your-api/users?v=1) ou como parte da URL (por exemplo, /v1/your-api/users). Em ambas as situações, a versão é claramente visível para o desenvolvedor que usa a API.
- **Usar um cabeçalho personalizado**: outra opção é ter um cabeçalho personalizado (como api-version) em que o desenvolvedor deve especificar a versão da sua API que pretende usar.

### Como você protege um servidor de ataques de injeção de SQL?
Existem muitas maneiras de proteger seu banco de dados relacional de ataques de injeção de SQL, mas aqui estão três muito comuns.

- **Declarações preparadas com consultas parametrizadas**: Esta é provavelmente a maneira mais eficaz, pois é feita por uma biblioteca ou estrutura, e tudo o que você precisa fazer é escrever suas consultas deixando espaços reservados para onde os dados devem ir e, em seguida, em um local separado, fornecer os dados reais.
- **Use um ORM (Mapeamento Objeto-Relacional)**: Essas estruturas permitem que você abstraia a interação com seu banco de dados e crie as consultas SQL para você, levando em consideração todas as questões de segurança em torno dessa interação.
- **Escape de dados**: Se quiser fazer isso manualmente, você pode cuidar do escape de caracteres especiais que podem quebrar a forma como você constrói suas consultas SQL. Manter uma lista de caracteres na lista negra para escapar nessa situação é uma boa ideia, para que você possa examiná-los programaticamente.

### Explique o conceito de ausência de estado em HTTP e como ele afeta os serviços de backend
HTTP é, por design, um protocolo sem estado, o que significa que cada solicitação é única e não relacionada a nenhuma solicitação anterior, mesmo do mesmo cliente.

Isso afeta os serviços web de backend, forçando-os a implementar suas próprias soluções de gerenciamento de estado se tal recurso for necessário.

### O que é conteinerização e como ela beneficia o desenvolvimento de backend?
É um método de virtualização leve para empacotar aplicativos e suas dependências, garantindo ambientes consistentes em diferentes sistemas.

Na verdade, é um benefício para o desenvolvimento de backend porque fornece isolamento e portabilidade, simplificando os processos de implantação e reduzindo conflitos entre versões de software e configurations.

### Quais medidas você tomaria para proteger uma API recém-desenvolvida?
Existem muitas maneiras de proteger uma API, aqui estão algumas das mais comuns:

- Adicione um método de autenticação, como OAuth, JWT, tokens de portador, autenticação baseada em sessão e outros.
- Use HTTPS para criptografar a transferência de dados entre o cliente e o servidor.
- Configure políticas CORS fortes para evitar solicitações indesejadas.
- Configure uma lógica de autorização forte para garantir que os clientes acessem apenas os recursos aos quais eles têm acesso.

### Como você escalaria um aplicativo de backend durante um pico de tráfego?
A maneira mais comum de escalar um aplicativo de backend durante picos de tráfego é ter várias instâncias do aplicativo por trás de um balanceador de carga e, quando o pico de tráfego acontecer, basta adicionar mais instâncias do aplicativo.

Isso é conhecido como dimensionamento horizontal e funciona melhor quando o aplicativo de backend não tem estado.

### Quais ferramentas e técnicas você usa para depurar um aplicativo de backend?
Se o aplicativo de backend que está sendo depurado estiver na máquina de desenvolvimento local, uma solução simples seria usar o próprio IDE. A maioria dos IDEs modernos, como IntelliJ, Eclipse e outros, tem recursos de depuração integrados.

Se o aplicativo de backend estiver no servidor, você terá que usar outras técnicas, como registro, o que pode ser feito com bibliotecas de registro. Ou você pode usar ferramentas mais complexas, como JProfiler ou NewRelic.

### Como você garante que seu código de backend seja sustentável e fácil de entender?
O truque aqui é seguir as melhores práticas e padrões de codificação, como:

- Modularidade.
- Seguir convenções de nomenclatura.
- Adicionar comentários de código.
- Fazer refatorações regulares para manter a dívida técnica sob controle.
- Manter mensagens de tratamento de erros consistentes em toda a plataforma.
- Executar testes de unidade em todo o código escrito.

## Nível intermediário

### Descreva como você implementaria uma pesquisa de texto completo em um banco de dados.
Você pode usar a funcionalidade nativa de pesquisa de texto completo de um banco de dados, como MySQL, Postgre ou até mesmo ElasticSearch.

No entanto, se você quiser implementá-lo você mesmo, as etapas seriam:

1. Pré-processar os dados de texto a serem pesquisados ​​e normalizá-los aplicando tokenização, derivação e remoção de stop words.
2. Em seguida, implementar um índice invertido, relacionando de alguma forma cada palavra única aos registros que contêm essa palavra.
3. Criar uma IU de pesquisa e normalizar a entrada do usuário da mesma forma que os dados de texto foram normalizados.
4. Em seguida, pesquisar cada palavra no banco de dados.
5. Classificar os resultados implementando uma lógica de pontuação com base em diferentes aspectos, como frequência de palavras.

### Como você abordaria o processamento em lote em um aplicativo de backend com muitos dados?
A melhor opção aqui seria usar uma estrutura de processamento em lote, como Hadoop ou Spark. Eles já estão preparados para processar grandes quantidades de dados em paralelo.

### Você pode explicar o uso e os benefícios de uma fila de mensagens em um sistema distribuído?
Uma fila de mensagens em um sistema distribuído pode atuar como o componente principal de uma arquitetura reativa. Cada serviço pode disparar e ouvir eventos vindos da fila. Dessa forma, quando os eventos chegam, esses serviços podem reagir a eles sem precisar consultar ativamente outros serviços para obter uma resposta.

### Quais estratégias você usaria para gerenciar conexões de banco de dados em um cenário de alta carga?
Durante um cenário de alta carga, há várias coisas que um desenvolvedor pode fazer para melhorar o desempenho da conexão de banco de dados:

- Usar pools de conexão para reutilizar conexões reduz o tempo necessário para estabelecer uma nova.
- Balancear a carga do tráfego do banco de dados (as consultas) entre um grupo de bancos de dados ajudaria a distribuir a carga.
- Até mesmo otimizar suas consultas pode reduzir o tempo que você está usando cada conexão, ajudando a otimizar o uso de recursos e minimizando o tempo que você está gastando com cada conexão ativa.

### Como você configuraria um pipeline de integração contínua/implantação contínua (CI/CD) para serviços de backend?
Há várias considerações a serem feitas ao configurar pipelines de Integração Contínua e Entrega Contínua:

- Usar o controle de origem como gatilho para todo o processo (git, por exemplo). Os pipelines de construção para seus serviços de backend devem ser executados quando você envia seu código para uma ramificação específica.
- Escolha a plataforma de CI/CD certa para suas necessidades, há muitas por aí, como GitHub Actions, GitLab CI/CD, CircleCI e muito mais.
- Certifique-se de ter testes de unidade automatizados que podem ser executados dentro desses pipelines.
- A implantação automática deve acontecer somente se todos os testes forem executados com sucesso, caso contrário, o pipeline deve falhar, impedindo que o código quebrado alcance qualquer ambiente.
- Use um repositório de artefatos como JFrog Artifactory ou Nexus Repository para armazenar serviços construídos com sucesso.
- Finalmente, considere configurar uma estratégia de reversão caso algo dê errado e a versão final implantada do seu serviço seja corrompida de alguma forma.

### Você pode descrever uma estratégia de cache distribuído para um aplicativo de alta disponibilidade?
Neste cenário, Você precisa considerar os seguintes pontos:

- Implemente um cluster de servidores que atuarão como cache distribuído. Implemente um processo de fragmentação de dados para distribuir uniformemente os dados entre todos os servidores de cache e certifique-se de que ele use um algoritmo de hash consistente para minimizar a reorganização do cache quando um servidor entra ou sai do cluster.
- Adicione replicação de cache para ter redundância de seus dados em caso de falha, dessa forma, seu cache distribuído também será tolerante a falhas.
- A invalidação de cache é essencial em qualquer solução de cache, pois seus dados ficarão obsoletos se você não os atualizar com frequência.

### Quais métodos você pode usar para gerenciar tarefas em segundo plano em seus aplicativos?
Depende muito de sua pilha de tecnologia e do que essas tarefas em segundo plano estão fazendo. E por isso, há muitas opções:

- Usando filas de tarefas como RabbitMQ ou Amazon SQS. Elas permitirão que você tenha trabalhadores em segundo plano como processos secundários enquanto seu aplicativo continua funcionando.
- Existem estruturas de trabalho em segundo plano como Celery para Python ou Sidekiq para Ruby.
- Você também pode confiar apenas em tarefas cron se quiser.
- Se sua linguagem de programação permitir, você também pode usar threads ou workers para executar essas tarefas em segundo plano, mas dentro do mesmo aplicativo.

### Como você lida com criptografia e descriptografia de dados em um aplicativo focado em privacidade?
Para esse tipo de aplicativo, você precisa distinguir entre "dados em repouso" e "dados em trânsito". O primeiro descreve seus dados enquanto eles estão armazenados em seu banco de dados (ou qualquer armazenamento de dados que você tenha). E o último (dados em trânsito) descreve seus dados enquanto eles estão viajando entre serviços de backend ou mesmo entre o servidor e o cliente.

Para "dados em trânsito", você deve garantir que a conexão aconteça dentro de um canal seguro e criptografado, como HTTPS.

E para "dados em repouso", use algoritmos de criptografia fortes, como AES, RSA ou ECC, e certifique-se de manter suas chaves associadas em algum lugar seguro, como dentro de uma ferramenta dedicada de gerenciamento de segredos ou serviços de gerenciamento de chaves (KMS).

### O que são webhooks e como você os implementou em projetos anteriores?
Webhooks são retornos de chamada HTTP definidos pelo usuário, eles são acionados por um evento específico dentro de um sistema. Eles são usados ​​principalmente para notificar sobre resultados de tarefas assíncronas de várias etapas para evitar manter uma conexão HTTP aberta.

Quanto à implementação de um webhook, considere o seguinte:

- **Definição de evento**: certifique-se de definir exatamente quais eventos acionarão a mensagem para o webhook e o tipo de payload associado a esses eventos.
- **Criação de endpoint**: com base na etapa anterior, defina um endpoint HTTP que possa lidar com a solicitação esperada (especialmente com a parte do payload). Em outras palavras, se você estiver recebendo dados na solicitação do webhook, certifique-se de criar o endpoint como um endpoint POST, caso contrário, você pode usar um GET.
- **Segurança**: lembre-se de implementar alguma forma de medidas de segurança em torno do seu endpoint do webhook para que ele não possa ser explorado.

### Quais considerações devem ser levadas em conta para a conformidade com o GDPR em um sistema de backend?
As seguintes são considerações importantes a serem levadas em conta:

- **Capture apenas o que você precisa e o que você disse aos seus usuários que capturaria**: Lembre-se de que, para cumprir com o GDPR, você precisa pedir o consentimento do seu usuário para coletar seus dados e especificar os pontos de dados reais que está coletando. Portanto, concentre-se neles e em nada mais.
- **Proteja seus dados**: Como parte dos regulamentos, você precisa garantir que seus dados estejam protegidos tanto em trânsito quanto em repouso. Há auditorias de segurança regulares que precisam acontecer para garantir que a segurança seja mantida alta.
- **O usuário tem direitos sobre os dados que você capturou**: portanto, certifique-se de dar a eles os endpoints ou serviços corretos para lê-los, editá-los ou até mesmo removê-los, se quiserem.

### Explique como você lidaria com processos de longa duração em solicitações da web.
Para solicitações da web que acionam processos de longa duração, a melhor opção é implementar uma arquitetura reativa. Isso significa que quando um serviço recebe uma solicitação, ele a transforma em uma mensagem dentro de uma fila de mensagens, e o processo de longa duração a pega sempre que estiver pronto para isso.

Enquanto isso, o cliente que envia essa solicitação recebe uma resposta imediata reconhecendo que a solicitação está sendo processada. O próprio cliente também pode ser conectado à fila de mensagens (ou por meio de um proxy) e aguardar um evento "pronto" com sua carga útil dentro.

### Discuta a implementação da limitação de taxa para proteger APIs de abuso.
Para implementar a limitação de taxa, você precisa manter os seguintes pontos em mente:

- **Defina seus limites**: Defina exatamente a quantidade de solicitações que um cliente pode fazer. Isso pode ser medido em solicitações por minuto, por dia ou por segundo.
- **Escolha uma estratégia de limitação**: Escolha um algoritmo de limitação de taxa, como o contador de janela fixa, janela de log deslizante, token bucket ou leaky bucket.
- **Armazene seus contadores em algum lugar**: Use um armazenamento de dados rápido (como o Redis) para controlar o número de solicitações ts ou timestamps para cada cliente.
- Quando o limite for atingido, tente responder com um código de status padrão, como 429, que indica que houve "Muitas solicitações".
- Se quiser levar isso adiante, você pode usar um API Gateway existente que já fornece essa funcionalidade ou adicionar suporte para picos repentinos de tráfego para evitar penalizar clientes que estão um pouco acima dos limites de vez em quando.

### Como você instrumenta e monitora o desempenho de aplicativos de backend?
Uma ótima maneira de monitorar o desempenho de aplicativos de backend é usar um sistema de gerenciamento de desempenho de aplicativos (APM), como New Relic, AppDynamics ou mesmo Dynatrace.

Eles rastrearão o desempenho do seu aplicativo e fornecerão insights sobre os gargalos que você pode ter com o mínimo de esforço de sua parte.

### O que são microsserviços e como você decomporia um monólito em microsserviços?
Microsserviços são um estilo de arquitetura de software que permite estruturar seus aplicativos de backend como uma coleção de serviços independentes, cada um trabalhando em torno de uma necessidade comercial específica.

Se você está procurando decompor um monólito em um conjunto de microsserviços, você tem que manter os seguintes pontos em mente:

1. Comece identificando os limites lógicos do seu monólito. Sua lógica interna abordará múltiplas responsabilidades e tipos de recursos. Encontre os limites entre eles para entender onde um serviço começa e outro termina.
2. Defina seus serviços com base nos limites do ponto anterior e comece a desacoplar as necessidades de dados também. Em múltiplas tabelas ou mesmo bancos de dados individuais sempre que fizer sentido.
3. Comece a refatorar incrementalmente o monólito e extrair a lógica necessária para cada microsserviço individual em seu próprio projeto.
4. Quando terminar, seu monólito original não deverá mais ser necessário, e todos os seus microsserviços terão seu próprio pipeline de implantação independente e repositório de código.

### Como você gerenciou dependências de API em sistemas de backend?
Uma ótima maneira de lidar com dependências de API em sistemas de backend é aproveitar o versionamento de API. Por meio dessa prática simples, você pode garantir que seus sistemas estejam realmente usando a API correta, mesmo que haja várias versões dela.

Isso também permite que você tenha vários sistemas de backend usando diferentes versões da mesma API sem qualquer risco de inconsistência ou de atualizações quebrando seus sistemas.

### Descreva o conceito de consistência eventual e suas implicações em sistemas de backend.
A consistência eventual é um modelo de consistência usado em computação distribuída. Este modelo garante que qualquer informação escrita em um sistema distribuído se tornará consistente (o que significa que todos os servidores terão a mesma versão desses dados) eventualmente, ao contrário de outros onde a consistência imediata é garantida.

Para sistemas de backend, isso implica que há uma necessidade de sincronização de dados entre todas as partes do sistema distribuído e, além disso, uma necessidade potencial de resolver conflitos de dados, se diferentes partes do seu sistema estiverem lidando com diferentes versões do mesmo registro de dados.

### O que é um proxy reverso e como ele é útil no desenvolvimento de backend?
Um proxy reverso é um servidor que fica na frente de vários outros servidores e redireciona o tráfego para esses servidores da web com base em regras lógicas diferentes. Por exemplo, você pode ter dois servidores da web, um para clientes da sua empresa e outro para seus funcionários.

Você pode configurar um proxy reverso para redirecionar o tráfego para um ou outro, dependendo do valor de um cabeçalho enviado na solicitação ou da URL real que está sendo solicitada.

Ele é muito útil no desenvolvimento de backend porque permite que você faça muitas coisas diferentes, por exemplo:

- Balanceamento de carga de tráfego entre várias instâncias do mesmo serviço de backend.
- Fornece uma camada extra de segurança ocultando a localização dos serviços de backend e lidando com ataques, como DDoS.
- Ele pode armazenar em cache o conteúdo, reduzindo a carga do servidor em seus servidores da web.
- Ele permite que você alterne os serviços de backend sem afetar as URLs públicas.

### Como você lidaria com o estado da sessão em um ambiente de aplicativo com balanceamento de carga?
Em um cenário de aplicativo com balanceamento de carga, o principal problema com o estado da sessão é que, se o sistema de backend estiver manipulando dados da sessão na memória, as solicitações subsequentes do mesmo cliente precisarão chegar ao mesmo servidor, caso contrário, os dados da sessão serão fragmentados e inúteis.

Existem duas maneiras principais de resolver esse problema:

- **Sessões persistentes**: isso permite que você configure o balanceador de carga para redirecionar solicitações do mesmo cliente para o mesmo servidor todas as vezes. A desvantagem disso é que o tráfego nem sempre é distribuído igualmente entre todas as cópias dos seus serviços de backend.
- **Armazenamento de sessão centralizado**: essa solução envolve levar os dados da sessão para fora dos seus serviços de backend para um armazenamento de dados centralizado que todas as cópias do seu serviço podem acessar. Isso torna mais fácil no balanceador de carga, mas requer lógica extra e mais "partes móveis".

Depende de você e de seus requisitos técnicos específicos determinar qual estratégia funciona melhor para você.

## Nível avançado

### O que é replicação de banco de dados e como ela pode ser usada para tolerância a falhas?
A replicação de banco de dados implica na replicação de dados em várias instâncias do mesmo banco de dados. Nesse cenário, geralmente há um banco de dados que atua como mestre para todos os clientes que o conectam, e o restante atua como "escravos", onde eles simplesmente recebem atualizações sobre os dados que estão sendo alterados/adicionados.

As duas principais implicações disso na tolerância a falhas são:

- Um cluster de banco de dados pode suportar problemas no servidor mestre promovendo um dos escravos sem perder nenhum dado no processo.
- Os escravos podem ser usados ​​como servidores somente leitura, aumentando a quantidade de solicitações de leitura que podem ser executadas nos dados sem afetar o desempenho do banco de dados.

### Descreva o uso da estratégia de implantação azul-verde em serviços de backend
A estratégia azul-verde envolve ter dois ambientes de produção idênticos, tendo um deles servindo tráfego real enquanto o outro está se preparando para ser atualizado com a próxima versão ou apenas ocioso, esperando para ser usado como backup.

### Você pode explicar os modelos de consistência em bancos de dados distribuídos (por exemplo, teorema CAP)?
O teorema CAP diz que bancos de dados distribuídos não podem fornecer simultaneamente mais de duas das seguintes garantias:

- **Consistência de dados**: significa que cada leitura está sempre retornando o resultado mais recente da operação de gravação. Isso é muito relevante neste modelo porque estamos lidando com vários servidores e os dados precisam ser replicados quase imediatamente para garantir a consistência.
- **Disponibilidade**: significa que cada solicitação sempre receberá uma resposta válida.
- **Tolerância de partição**: o sistema distribuído continua a operar e trabalhar sem perda de dados, mesmo durante interrupções parciais da rede.

Por exemplo, se o sistema for consistente e altamente disponível, ele não será capaz de suportar interrupções parciais da rede. Se, por outro lado, o sistema for altamente disponível e tolerante a partições, ele não será capaz de garantir a consistência imediata dos dados.

### Como você gerencia migrações de esquema em um ambiente de entrega contínua?
Os dois principais aspectos a serem considerados ao gerenciar migrações de esquema, especialmente em ambientes de CD, são:

- Rastreie suas migrações de esquema dentro do controle de versão. Mantenha essas versões de arquivos com seu código, pois há uma relação direta entre essas versões.
- Use ferramentas de migração automatizadas, como Flyway ou Liquibase, para simplificar o processo e mantê-lo padrão.

### Quais estratégias existem para lidar com idempotência no design de API REST?
Para APIs REST, você pode aproveitar os verbos HTTP e definir suas operações idempotentes usando verbos inerentemente idempotentes, como GET, PUT e DELETE.

Ou você sempre pode implementar manualmente uma lógica baseada em chave para evitar repetir a mesma operação várias vezes se a chave fornecida pelo cliente for sempre a mesma.

### Descreva a implementação de uma solução de logon único (SSO)
Em um nível muito alto, as etapas necessárias para implementar uma solução SSO são:

1. Escolher um provedor de identidade, como Okta ou Keycloack.
2. Cada aplicativo será integrado ao provedor de identidade da etapa anterior usando um protocolo SSO padrão, como SAML, OpenID ou qualquer outro.
3. Para o primeiro acesso do usuário, o aplicativo se conectará ao IdP e autenticará o usuário, obtendo um token de acesso em troca.
4. Em seguida, durante as solicitações subsequentes, o aplicativo validará o token fornecido por meio do IdP.

### Explique como você desenvolveria um sistema de back-end para lidar com fluxos de dados de dispositivos IOT
Uma arquitetura de captura e processamento de dados em tempo real exigiria os seguintes componentes:

- Use um serviço de ingestão de dados escalável, como Kafka ou AWS Kinesis, que seja compatível com um dos muitos protocolos padrão de IoT (como MQTT ou CoAP).
- Processe os dados por meio de mecanismos de processamento em tempo real, como Apache Flink ou Spark Streaming.
- Armazene os dados em um data lake escalável, idealmente um sistema compatível com séries temporais, como o InfluxDB.

### Como você arquitetaria um backend para dar suporte à sincronização de dados em tempo real entre dispositivos?
Se quiser dar suporte à sincronização de dados em tempo real, você terá que encontrar uma maneira de criar canais de comunicação estáveis ​​e eficientes entre dispositivos e encontrar uma maneira de resolver potenciais conflitos de sincronização de dados quando vários dispositivos estiverem tentando alterar o mesmo registro.

Então, para canais de comunicação, você pode usar um dos seguintes:

- Canais bidirecionais baseados em soquete que permitem a troca de dados em tempo real.
- Usando um modelo pub/sub para distribuir dados de forma eficiente entre vários dispositivos. Você pode usar algo como Redis ou Kafka para isso.

Para resoluções de conflitos de dados, você pode usar algoritmos como Transformação Operacional (OT) ou Tipos de Dados Replicados Sem Conflito (CRDTs).

### Discuta os benefícios e desvantagens de mArquiteturas de microsserviços em sistemas de backend.
Benefícios:

- **Escalabilidade**: os microsserviços podem ser dimensionados independentemente uns dos outros.
- **Flexibilidade tecnológica**: você pode usar diferentes pilhas de tecnologia dependendo das necessidades específicas de cada microsserviço.
- **Implantações mais rápidas**: os microsserviços podem ser implantados individualmente, melhorando a velocidade com que você entrega as alterações para a produção.

Desvantagens:

- **Arquitetura excessivamente complexa**: em algumas situações, uma arquitetura baseada em microsserviços pode se tornar muito complexa para gerenciar e orquestrar.
- **Depuração**: a depuração de problemas em uma arquitetura baseada em microsserviços pode ser difícil, pois os dados fluem por vários serviços durante uma única solicitação.
- **Sobrecarga de comunicação**: em comparação com uma abordagem monolítica, a comunicação entre microsserviços pode ser excessivamente complexa.

### Como você abordaria o teste de carga de uma API de backend?
1. Primeiro, você precisa entender os objetivos e configurar um ambiente de teste. O ideal é que seu ambiente se assemelhe muito à produção.
2. Projete e implemente seus testes com as ferramentas que você selecionou (como JMeter, LoadRunner ou qualquer outra).
3. Comece a aumentar gradualmente a carga em seus testes enquanto monitora o desempenho e a estabilidade do seu sistema.
4. Otimize sua API de backend e volte para a primeira etapa para redesenhar seus testes e tente novamente até ficar satisfeito com os resultados.

### Descreva como você implementaria uma estratégia de remoção de cache do lado do servidor.
Para definir essa estratégia, você precisará definir os seguintes elementos:

- O limite de tamanho que acionará a remoção do cache quando excedido.
- Uma estratégia de monitoramento para determinar se a estratégia de remoção está funcionando corretamente ou se precisa de ajuste.
- Um mecanismo de invalidação de cache.
- E uma política de remoção, que pode ser uma das seguintes:
- LRU (Least Recently Used): Remove os itens menos acessados ​​recentemente.
- LFU (Least Frequently Used): Remove os itens acessados ​​com menos frequência.
- FIFO (First-In, First-Out): Remova itens na ordem em que foram adicionados.
- Random: Selecione aleatoriamente os itens para remover.
- TTL (Time-To-Live): Expire itens após um certo tempo.

### O que são IDs de correlação e como eles podem ser usados ​​para rastrear solicitações entre serviços?
IDs de correlação são identificadores exclusivos adicionados em solicitações feitas para arquiteturas distribuídas para facilitar o rastreamento de solicitações em toda a arquitetura. Lembre-se de que, geralmente, quando uma solicitação atinge um sistema de backend distribuído, os dados da solicitação passam por vários serviços da Web antes de gerar uma resposta.

Isso facilita a compreensão da jornada que cada solicitação percorre para depurar quaisquer problemas potenciais ou questões de desempenho.

### Explique a diferença entre bloqueio otimista e pessimista e quando usar cada um
Bloqueio otimista é uma estratégia que:

- Assume que os conflitos são raros e não acontecem com tanta frequência.
- Permite acesso simultâneo aos dados.
- Verifica se há conflitos antes de confirmar.
- É melhor usado em cenários de alta leitura e baixa gravação.

O bloqueio pessimista, por outro lado, é uma estratégia que:

- Assume que os conflitos são muito comuns.
- Bloqueia dados e impede o acesso simultâneo.
- Mantém esses bloqueios durante a duração de uma transação.
- É mais adequado para cenários de alta gravação ou quando a integridade dos dados é crítica.

### Quais métodos você usaria para evitar deadlocks em transações de banco de dados?
Existem muitas maneiras de evitar deadlocks em transações de BD; algumas das mais comuns são:

- Usar a ordenação de bloqueios para adquirir bloqueios em uma ordem global consistente, evitando condições de espera circulares.
- Usar tempos limite para transações de BD para eliminar automaticamente operações de longa duração que podem levar a deadlocks.
- Usar o controle de simultaneidade otimista sempre que possível, para evitar manter bloqueios por muito tempo.

### Como você protegeria a comunicação entre serviços em uma arquitetura de microsserviços?
Partindo da base de entendimento de que sua comunicação entre serviços deve ocorrer somente dentro de redes privadas (idealmente, nenhum tráfego público deve atingir esses serviços), aqui estão algumas recomendações:

- Use canais criptografados, como TLS para evitar ataques comuns, como man-in-the-middle.
- Use um gateway de API para gerenciar e autenticar o tráfego que atinge essa rede privada.
- Aplique autenticação e autorização para mensagens entre serviços, certificando-se de que somente microsserviços válidos possam se comunicar e, quando o fizerem, tenham acesso somente ao que faz sentido para eles.

### Discuta técnicas para prevenir e detectar anomalias de dados em sistemas de larga escala
Algumas técnicas comuns incluem:

- Adicionar e implementar regras de validação para evitar entrada de dados inválidos. Por meio da definição de esquemas e restrições de esquema para impor certos padrões mínimos, você pode evitar que anomalias de dados aconteçam.
- Implemente o controle de versão de dados para reverter facilmente se houver alguma anomalia detectada.
- Implemente uma forte prática de qualidade de dados para garantir que qualquer informação que entre em seu sistema seja validada e flagged if required.

### Descreva o processo de criação de uma solução global de armazenamento de dados de alta disponibilidade para um aplicativo multinacional.
A construção de um armazenamento de dados de alta disponibilidade envolve várias áreas, incluindo:

- **Ambientes multizona**: se você estiver usando soluções baseadas em nuvem (como Azure, AWS, GCP ou outras), provavelmente terá esse requisito atendido instantaneamente (exceto para algumas regiões específicas do mundo). Isso é para garantir a disponibilidade mesmo durante interrupções parciais da rede.
- **Replicação de dados**: garanta que seus dados estejam sendo replicados entre servidores de todas as zonas. Isso é para garantir que, se houver uma falha que derrube alguns servidores (ou até mesmo zonas inteiras), não haja perda de dados.
- **Balanceamento de carga**: garanta que o tráfego esteja adequadamente balanceado entre todas as suas zonas de disponibilidade para garantir a menor latência para todos os seus clientes.
- **Política de governança de dados**: configure uma política de governança de dados adequada para garantir que o acesso aos dados seja regulado.
- **Conformidade regulatória**: conformidade total com os regulamentos de dados locais (como o GDPR).