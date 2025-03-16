### Sumário - MongoDB e Mongoose

| No. | Perguntas |
| --- | --------- |
|   | **MongoDB e Mongoose** |
| 1 | [O que é MongoDB?](#o-que-é-mongodb)|
| 2 | [Quais são as diferenças entre NoSQL e SQL?](#quais-são-as-diferenças-entre-nosql-e-sql)|
| 3 | [Como estabelecer conexão com banco de dados MongoDB em uma aplicação Node?](#como-estabelecer-conexão-com-banco-de-dados-mongodb-em-uma-aplicação-node)|
| 4 | [O que são propriedades virtuais no Mongoose?](#o-que-são-propriedades-virtuais-no-mongoose)|
| 5 | [Como podemos adicionar ou criar nossos próprios métodos de instância no Mongoose?](#como-podemos-adicionar-ou-criar-nossos-próprios-métodos-de-instância-no-mongoose)|
| 6 | [Como podemos adicionar ou criar nossos próprios métodos estáticos no Mongoose?](#como-podemos-adicionar-ou-criar-nossos-próprios-métodos-estáticos-no-mongoose)|
| 7 | [O que são middlewares do Mongoose?](#o-que-são-middlewares-do-mongoose)|
| 8 | [Como consultar dados usando Mongoose?](#como-consultar-dados-usando-mongoose)|
| 9 | [O que é Population no Mongoose?](#o-que-é-population-no-mongoose)|
| 10| [O que é Datamasking?](#o-que-é-datamasking)|
| 11| [O que é hashing e como funciona?](#o-que-é-hashing-e-como-funciona)|
| 12| [O que são salts e por que são tão importantes?](#o-que-são-salts-e-por-que-são-tão-importantes)|
| 13| [O que são peppers e por que são tão importantes?](#o-que-são-peppers-e-por-que-são-tão-importantes)|
| 14| [O que são JWT?](#o-que-são-jwt)|
| 15| [Quais são os diferentes métodos de autenticação?](#quais-são-os-diferentes-métodos-de-autenticação)|
| 16| [Quais são as desvantagens de usar autenticação baseada em sessão?](#quais-são-as-desvantagens-de-usar-autenticação-baseada-em-sessão)|
| 17| [Quais são as desvantagens de usar autenticação baseada em JWT?](#quais-são-as-desvantagens-de-usar-autenticação-baseada-em-jwt)|

1. ### O que é MongoDB?

   MongoDB é um banco de dados orientado a documentos, multiplataforma, que fornece alta performance, alta disponibilidade e fácil escalabilidade. Classificado como um programa de banco de dados NoSQL, o MongoDB usa documentos semelhantes a JSON com esquema.<br/>
   MongoDB é escrito em C++<br/>
   
   MongoDB é conhecido por ser usado pela Cidade de Chicago, Codecademy, Google Search, Foursquare, IBM, Orange S.A., The Gap, Inc., Uber, Coinbase, Sega, Barclays, HSBC, eBay, Cisco, Bosch e Urban Outfitters.

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

2. ### Quais são as diferenças entre NoSQL e SQL?

   | Parâmetro | SQL | NOSQL |
   | --------- | --- | ----- |
   |Definição |Bancos de dados SQL são primariamente chamados de RDBMS ou Bancos de Dados Relacionais |Bancos de dados NoSQL são primariamente chamados de bancos de dados Não-relacionais ou distribuídos |
   |Linguagem de Consulta|Linguagem de consulta estruturada (SQL) |Sem linguagem de consulta declarativa |
   |Tipo |Bancos de dados SQL são baseados em tabelas |Bancos de dados NoSQL podem ser baseados em documentos, pares chave-valor, bancos de dados de grafos |
   |Esquema |Bancos de dados SQL têm um esquema predefinido |Bancos de dados NoSQL usam esquema dinâmico para dados não estruturados |
   |Capacidade de escalar |Bancos de dados SQL são escaláveis verticalmente |Bancos de dados NoSQL são escaláveis horizontalmente |
   |Exemplos|Oracle, Postgres e MS-SQL |MongoDB, Redis, Neo4j, Cassandra, Hbase|
   |Melhor adequado para |Uma escolha ideal para ambientes com consultas complexas intensivas |Não é uma boa opção para consultas complexas |
   |Armazenamento de dados hierárquicos |Bancos de dados SQL não são adequados para armazenamento de dados hierárquicos|Mais adequado para armazenamento de dados hierárquicos, pois suporta o método de pares chave-valor |
   |Variações|Um tipo com pequenas variações|Muitos tipos diferentes que incluem armazenamentos chave-valor, bancos de dados de documentos e bancos de dados de grafos|
   |Consistência |Deve ser configurado para forte consistência |Depende do SGBD, pois alguns oferecem forte consistência como MongoDB, enquanto outros oferecem apenas consistência eventual, como Cassandra |
   |Hardware|Hardware especializado para BD (Oracle Exadata, etc.)|Hardware de commodities |
   |Rede |Rede altamente disponível (Infiniband, Fabric Path, etc.) |Rede de commodities (Ethernet, etc.) |
   |Melhores características |Suporte multiplataforma, Seguro e gratuito |Fácil de usar, Alto desempenho e Ferramenta flexível |
   |Principais empresas que usam |Hootsuite, CircleCI, Gauges |Airbnb, Uber, Kickstarter |
   |Modo ACID vs. BASE|ACID (Atomicidade, Consistência, Isolamento e Durabilidade) é um padrão para RDBMS |Base (Basicamente Disponível, Estado Suave, Eventualmente Consistente) é um modelo de muitos sistemas NoSQL |
   |Salário médio|₹ 5,58,704 por ano|₹ 6,04,959 por ano|
   
   

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

3. ### Como estabelecer conexão com banco de dados MongoDB em uma aplicação Node?

	**Conexão com o Banco de Dados**
	Crie um arquivo ./config/database.js na raiz do projeto.

	Conexão com o Banco de Dados

	Em seguida, vamos adicionar código que se conecta ao banco de dados.

	no arquivo database.js 
	```
	const mongoose = require('mongoose');
	const server = '127.0.0.1:27017'; // SUBSTITUA COM SEU SERVIDOR DB
	const database = 'fcc-Mail';      // SUBSTITUA COM O NOME DO SEU DB

     mongoose.connect(`mongodb://${server}/${database}`)
       .then(() => {
         console.log('Conexão com o banco de dados bem-sucedida')
       })
       .catch(err => {
         console.error('Erro na conexão com o banco de dados')
       })
 
	module.exports = { mongoose } 
	```
	**MongoDB Atlas**
	Cadastre-se no MongoDB Atlas e ele ajudará você a fazer uma conexão por url, tendo uma chave secreta e senha

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**


4. ### O que são propriedades virtuais no Mongoose?

  Uma propriedade virtual não é persistida no banco de dados. Podemos adicioná-la ao nosso esquema como um auxiliar para obter e definir valores, mas ela não será armazenada no banco de dados.
  
  ```
	userSchema.virtual('fullName').get(function() {
	return this.firstName + ' ' + this.lastName
	})
	
	userSchema.virtual('fullName').set(function(name) {
	let str = name.split(' ')
  
	this.firstName = str[0]
	this.lastName = str[1]
	})
	
	const user = new User()
	user.fullName = 'Thomas Anderson'
	console.log(user.toJSON())  // Exibe os campos do modelo como JSON
	console.log()
	console.log(user.fullName)  // Exibe o nome completo
	//O código acima produzirá a seguinte saída:

	{ _id: 5a7a4248550ebb9fafd898cf,
		firstName: 'Thomas',
		lastName: 'Anderson' }
	//Thomas Anderson
  ```

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**


5. ### Como podemos adicionar ou criar nossos próprios métodos de instância no Mongoose?

   Podemos criar métodos auxiliares personalizados no esquema e acessá-los através da instância do modelo. Esses métodos terão acesso ao objeto do modelo e podem ser usados de forma bastante criativa.
   
   ```
	userSchema.methods.details = function() {
	return this.username + ' - ' +  this.email
	}
	//Este método será acessível através de uma instância do modelo:
	const user = new User({
	username: 'user2',
	email: 'user2@gmail.com'
	})
	```

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**


6. ### Como podemos adicionar ou criar nossos próprios métodos estáticos no Mongoose?

  De forma semelhante aos métodos de instância, podemos criar métodos estáticos no esquema. Vamos criar um método para recuperar todos os usuários no banco de dados:
  ```
  userSchema.statics.getUsers = function() {
  return new Promise((resolve, reject) => {
    this.find((err, docs) => {
      if(err) {
        console.error(err)
        return reject(err)
      }
      resolve(docs)
			})
		})
	}
  ```

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

7. ### O que são middlewares do Mongoose?

   Middlewares são funções que são executadas em estágios específicos de um pipeline. O Mongoose suporta middlewares para as seguintes operações:<br/>

	Aggregate<br/>
	Document<br/>
	Model<br/>
	Query<br/>

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

8. ### Como consultar dados usando Mongoose?

   O Mongoose possui uma API muito rica que lida com muitas operações complexas suportadas pelo MongoDB. Considere uma consulta onde podemos construir incrementalmente componentes de consulta.<br/>

	Neste exemplo, vamos:<br/>

	Encontrar todos os usuários<br/>
	Pular os primeiros 100 registros<br/>
	Limitar os resultados a 10 registros<br/>
	Ordenar os resultados pelo campo firstName<br/>
	Selecionar o firstName<br/>
	Executar essa consulta<br/>
	```
	User.find()                   // encontra todos os usuários
         .skip(100)                // pula os primeiros 100 itens
         .limit(10)                // limita a 10 itens
         .sort({firstName: 1}      // ordena em ordem crescente por firstName
         .select({firstName: true} // seleciona apenas firstName
         .exec()                   // executa a consulta
         .then(docs => {
            console.log(docs)
          })
         .catch(err => {
            console.error(err)
          })
	```

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

9. ### O que é Population no Mongoose?

  Population é o processo de substituir automaticamente os caminhos especificados no documento por documento(s) de outra(s) coleção(ões). Podemos popular um único documento, múltiplos documentos, objeto simples, múltiplos objetos simples ou todos os objetos retornados de uma consulta.

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

10. ### O que é Datamasking?

  Mascaramento de dados é um método de criar uma versão estruturalmente semelhante, mas não autêntica, dos dados de uma organização que pode ser usada para fins como testes de software e treinamento de usuários. O objetivo é proteger os dados reais, tendo um substituto funcional para ocasiões em que os dados reais não são necessários.<br/>
  Você pode simplesmente usar **$project** para ocultar o campo de celular<br/>
  Ou talvez você tenha um campo extra em seu documento para indicar se a informação é pública ou não, ou seja, dado os documentos<br/>

**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

11. ### O que é hashing e como funciona?

  Hashing é o processo de converter uma entrada de qualquer comprimento em uma string de texto de tamanho fixo, usando uma função matemática.
  ![hashing](https://miro.medium.com/max/4000/0*Zkd2fcKuVGirbNpl.png)
  Quando o usuário fornece uma entrada, ela será convertida em um valor de comprimento fixo por uma função de hash, e o valor resultante será chamado de texto hasheado, e deve ser sempre único para valores diferentes.
  
**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

12. ### O que são salts e por que são tão importantes?

  É um valor único que pode ser adicionado ao final da senha para criar um valor hash diferente. Isso adiciona uma camada de segurança ao processo de hashing.<br/>
  Eles são tão importantes porque previnem **ataques de força bruta** (tentativa de todas as combinações possíveis de senha) e também contra **tabelas rainbow** (uma tabela contendo todos os textos hash comuns e suas respectivas senhas).<br/>
  
**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

13. ### O que são peppers e por que são tão importantes?

	Um pepper é um segredo adicionado a uma entrada, como uma senha, antes de ser hasheada com uma função de hash criptográfica.<br/>
	Um pepper desempenha um papel comparável ao de um salt, mas enquanto um salt não é secreto (apenas único) e pode ser armazenado junto com a saída hasheada,<br/> um pepper é secreto e não deve ser armazenado com a saída. O hash e o salt geralmente são armazenados em um banco de dados, mas um pepper deve ser armazenado separadamente (por exemplo, em um arquivo de configuração) para evitar que seja obtido pelo atacante em caso de violação do banco de dados. <br/> Onde o salt só precisa ser longo o suficiente para ser único, um pepper tem que ser seguro para permanecer secreto (pelo menos 112 bits é recomendado pelo NIST), caso contrário, um atacante só precisa de uma entrada conhecida para quebrar o pepper.<br/> Finalmente, o pepper deve ser gerado novamente para cada aplicação em que é implantado, caso contrário, uma violação de uma aplicação resultaria em menor segurança de outra aplicação.


  
**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

14. ### O que são JWT?

	JSON Web Token (JWT) é um padrão aberto (RFC 7519) que define uma maneira compacta e autossuficiente para transmitir informações com segurança entre as partes como um objeto JSON.<br/>
	Alguns cenários em que os JSON Web Tokens são úteis:<br/>
	**Autorização**: Este é o cenário mais comum para usar JWT. Uma vez que o usuário está logado, cada solicitação subsequente incluirá o JWT, permitindo que o usuário acesse rotas, serviços e recursos que são permitidos com esse token. Single Sign On é um recurso que usa amplamente JWT hoje em dia, devido à sua pequena sobrecarga e sua capacidade de ser facilmente usado em diferentes domínios.<br/>

	**Troca de Informações**: JSON Web Tokens são uma boa maneira de transmitir informações com segurança entre as partes. Como os JWTs podem ser assinados—por exemplo, usando pares de chaves pública/privada—você pode ter certeza de que os remetentes são quem dizem ser. Além disso, como a assinatura é calculada usando o cabeçalho e a carga útil, você também pode verificar se o conteúdo não foi adulterado.<br/>
	
	![jwt](https://research.securitum.com/wp-content/uploads/sites/2/2019/10/jwt_ng1_en.png)


  
**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**

15. ### Quais são os diferentes métodos de autenticação?

	

    Use **chaves de API** se você espera que os desenvolvedores construam aplicações internas que não precisam acessar mais do que os dados de um único usuário.<br/>
    Use **tokens de acesso OAuth** se você quiser que os usuários forneçam autorização facilmente para aplicações sem precisar compartilhar dados privados ou examinar documentação para desenvolvedores.<br/>
	Use **cookies de sessão**, aqui o servidor é responsável por criar uma sessão para o usuário específico quando o usuário faz login, depois disso o id da sessão é armazenado em um cookie no navegador do usuário. Para cada solicitação enviada pelo usuário, o cookie também será enviado, onde o servidor pode comparar o id da sessão do cookie com as informações da sessão armazenadas no servidor, assim a identidade do usuário é verificada.
  



  
**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**


16. ### Quais são as desvantagens de usar autenticação baseada em sessão?

	

   **Chave Secreta Comprometida**: O melhor e o pior sobre JWT é que ele depende de apenas uma Chave. Considere que a Chave seja vazada por um desenvolvedor/administrador descuidado ou malicioso, todo o sistema está comprometido!<br/>
  **Não pode gerenciar o cliente a partir do servidor**<br/>**Não pode enviar mensagens para clientes** <br/>**Algoritmo criptográfico pode ser depreciado**<br/>**Sobrecarga de Dados**: O tamanho do token JWT será maior do que o de um token de Sessão normal<br/>Complicado de entender: JWT usa algoritmos de Assinatura criptográfica para verificar os dados e obter o ID do usuário a partir do token. Entender o Algoritmo de Assinatura em si requer noções básicas de criptografia. <br/>



  
**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**


17. ### Quais são as desvantagens de usar autenticação baseada em JWT?

	

   **Autenticação baseada em sessão**:<br/> Como as sessões são armazenadas na memória do servidor, a escalabilidade se torna um problema quando há um grande número de usuários usando o sistema ao mesmo tempo.<br/>Os cookies normalmente funcionam em um único domínio ou subdomínios e são normalmente desativados pelo navegador se funcionarem entre domínios (cookies de terceiros). Isso apresenta problemas quando as APIs são servidas de um domínio diferente para dispositivos móveis e web.



  
**[ Voltar ao Topo ⬆ ](#sumário---mongodb-e-mongoose)**