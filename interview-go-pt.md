### Sumário - Golang

| No. | Perguntas |
| --- | --------- |
|   | **Golang** |
| 1 | [O que é Golang?](#o-que-é-golang)|
| 2 | [Quais são os prós e contras do Golang?](#quais-são-os-prós-e-contras-do-golang)|
| 3 | [Que tipos de projetos são adequados para serem construídos em Golang?](#que-tipos-de-projetos-são-adequados-para-serem-construídos-em-golang)
| 4 | [Golang é uma linguagem orientada a objetos?](#golang-é-uma-linguagem-orientada-a-objetos)
| 5 | [Quais são os tipos de dados em Golang?](#quais-são-os-tipos-de-dados-em-golang)
| 6 | [É possível retornar múltiplos valores de uma função?](#é-possível-retornar-múltiplos-valores-de-uma-função)
| 7 | [O que é GOPATH?](#o-que-é-gopath)
| 8 | [O que são Goroutines?](#o-que-são-goroutines)
| 9 | [O que é nil em Go?](#o-que-é-nil-em-go)
| 10 | [Qual é a diferença entre array e slice em Go?](#qual-é-a-diferença-entre-array-e-slice-em-go)
| 11 | [Como funciona um compilador Go?](#como-funciona-um-compilador-go)
| 12 | [O que é uma Interface e por que você a utiliza?](#o-que-é-uma-interface-e-por-que-você-a-utiliza)
| 13 | [O que são concorrência e paralelismo e qual é a diferença entre ambos?](#o-que-são-concorrência-e-paralelismo-e-qual-é-a-diferença-entre-ambos)
| 14 | [Quais são as diferenças entre goroutines e threads?](#quais-são-as-diferenças-entre-goroutines-e-threads)
| 15 | [Para que servem os channels?](#para-que-servem-os-channels)
| 16 | [Você pode fazer algo em goroutines usando channels?](#você-pode-fazer-algo-em-goroutines-usando-channels)
| 17 | [O que é um Closure?](#o-que-é-um-closure)
| 18 | [O que são runtime e pacotes runtime?](#o-que-são-runtime-e-pacotes-runtime)
| 19 | [Como você pode saber quantos núcleos seu computador tem?](#como-você-pode-saber-quantos-núcleos-seu-computador-tem)
| 20 | [Como você diria a uma goroutine para usar menos núcleos do que você tem?](#como-você-diria-a-uma-goroutine-para-usar-menos-núcleos-do-que-você-tem)
| 21 | [Como você determinaria o tipo de uma variável e qual pacote usar para isso?](#como-você-determinaria-o-tipo-de-uma-variável-e-qual-pacote-usar-para-isso)
| 22 | [Quais tipos um map pode armazenar?](#quais-tipos-um-map-pode-armazenar)
| 23 | [O que são microsserviços?](#o-que-são-microsserviços)
| 24 | [Por que não existem classes em Go?](#por-que-não-existem-classes-em-go)
| 25 | [Diferença entre tempo de compilação e tempo de execução?](#diferença-entre-tempo-de-compilação-e-tempo-de-execução)
| 26 | [Como gerar um número verdadeiramente aleatório em golang?](#como-gerar-um-número-verdadeiramente-aleatório-em-golang)
| 27 | [Por que as goroutines são leves?](#por-que-as-goroutines-são-leves)
| 28 | [Se a capacidade não for definida em um slice, qual seria a capacidade?](#se-a-capacidade-não-for-definida-em-um-slice-qual-seria-a-capacidade)
| 29 | [Qual é a maneira mais fácil de verificar se um slice está vazio?](#qual-é-a-maneira-mais-fácil-de-verificar-se-um-slice-está-vazio)
| 30 | [Qual é a vantagem do Go avaliar tipos implícitos em tempo de compilação?](#qual-é-a-vantagem-do-go-avaliar-tipos-implícitos-em-tempo-de-compilação)


1. ### O que é Golang?


   Golang é uma linguagem de programação compilada, estaticamente tipada, projetada no Google por Robert Griesemer, Rob Pike e Ken Thompson. Golang foi projetada no Google em 2007 para melhorar a produtividade da programação em uma era de máquinas multicore, em rede e grandes bases de código.


**[ Voltar ao Topo ⬆ ](#sumário---golang)**


2. ### Quais são os prós e contras do Golang?

	**Prós:**
	* Facilidade de uso
    * Uma biblioteca padrão inteligente
    * Forte segurança integrada
    * Linguagem com coleta de lixo
    * Minimalismo e legibilidade
    * Concorrência


    **Contras:**
    * Sem genéricos
    * Código repetitivo para tratamento de erros e falta de verificações em tempo de compilação para erros não tratados
    * Escassez de recursos de paralelismo e concorrência de alto nível



**[ Voltar ao Topo ⬆ ](#sumário---golang)**


3. ### Que tipos de projetos são adequados para serem construídos em Golang?
     * Serviços em nuvem 
     * Plataformas de mídia
     * Provedores de transmissão
     * Projetos com arquitetura de microsserviços

  **[ Voltar ao Topo ⬆ ](#sumário---golang)**

4. ### Golang é uma linguagem orientada a objetos?
    
    Golang tem tipos e métodos e permite um estilo de programação orientado a objetos, mas não há hierarquia de tipos. Golang tem algumas propriedades da programação orientada a objetos como Encapsulamento, Composição, mas não tem herança, classes, sobrecarga de função.


  **[ Voltar ao Topo ⬆ ](#sumário---golang)**

5. ### Quais são os tipos de dados em Golang?

    1. **Tipo básico**: Números, strings e booleanos.
    2. **Tipo agregado**: Arrays e structs.
    3. **Tipo de referência**: Ponteiros, slices, maps, funções e channels.
    4. **Tipo de interface**


  **[ Voltar ao Topo ⬆ ](#sumário---golang)**


6. ### É possível retornar múltiplos valores de uma função?

    Sim. Uma função Go pode retornar múltiplos valores, cada um separado por vírgulas na declaração de retorno.

    ```go
	    package main

        import "fmt"
        
        func foo() (string, string) {
           return "foo", "ball"
        }
        
        func main() {
           fmt.Println(foo())
        }
	```


  **[ Voltar ao Topo ⬆ ](#sumário---golang)**    


7. ### O que é GOPATH?


    A variável de ambiente GOPATH especifica a localização do seu espaço de trabalho. Por padrão, é um diretório chamado go dentro do seu diretório home.    <br/>  
    O comando go env GOPATH imprime o GOPATH atual efetivo; ele imprime o local padrão se a variável de ambiente não estiver definida.          

  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

8. ### O que são Goroutines?

    Goroutines são "threads" incrivelmente leves gerenciados pelo runtime do Go. Elas nos permitem criar programas paralelos assíncronos que podem executar algumas tarefas muito mais rapidamente do que se fossem escritos de maneira sequencial.

  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

9. ### O que é nil em Go?
    nil é um identificador predeclarado em Go que representa valores zero para ponteiros, interfaces, channels, maps, slices e tipos de função.

  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

10. ### Qual é a diferença entre array e slice em Go?
    
    * **ARRAY**: Um array é uma coleção fixa de dados. A ênfase aqui está em fixo, porque uma vez que você define o comprimento de um array, ele não pode ser alterado.<br/>
   
    ```go
	arr := [4]int{3, 2, 5, 4}
	```
    * **SLICE**: Slices são muito mais flexíveis, poderosos e convenientes do que arrays. Ao contrário dos arrays, slices podem ser redimensionados usando a função integrada append.

    ```go
	slicee := make([]Type, length, capacity)
	```

  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

11. ### Como funciona um compilador Go?
   
    Um compilador Go passa pelas seguintes etapas, elas são resumidas. Se entrarmos em detalhes, você precisaria de um livro completo para entender cada módulo. Para fins de entrevista, anexei uma nota manuscrita, vou gerar uma forma digital em breve.

    ![go compiler](/img/go_compiler.jpeg)

  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   


12. ### O que é uma Interface e por que você a utiliza?
    
    A interface é uma coleção de métodos, bem como é um tipo personalizado.
    
    ```go
	package main
  
        import "fmt"
          
        // Criando uma interface
        type tank interface {
          
            // Métodos
            Tarea() float64
            Volume() float64
        }
          
        type myvalue struct {
            radius float64
            height float64
        }
          
        // Implementando métodos da
        // interface tank
        func (m myvalue) Tarea() float64 {
          
            return 2*m.radius*m.height +
                2*3.14*m.radius*m.radius
        }
          
        func (m myvalue) Volume() float64 {
          
            return 3.14 * m.radius * m.radius * m.height
        }
          
        // Método Principal
        func main() {
          
            // Acessando elementos da
            // interface tank
            var t tank
            t = myvalue{10, 14}
            fmt.Println("Área do tanque :", t.Tarea())
            fmt.Println("Volume do tanque:", t.Volume())
        }    
	```

    Interfaces podem tornar o código mais claro, mais curto, mais legível, e podem fornecer uma boa API entre pacotes, ou clientes (usuários) e servidores (provedores).

  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   


  13. ### O que são concorrência e paralelismo e qual é a diferença entre ambos?
   
    **Concorrência** :  
    Definição 1: Lidar com várias coisas ao mesmo tempo. <br/>
    Definição 2: Uma composição de processos executados independentemente (Exemplo: suponha que existam duas tarefas A e B, a forma como isso funciona é que a tarefa A é concluída em 70%, enquanto precisa esperar por algo, então pega a tarefa B e tenta completá-la, se a tarefa B tiver que esperar em 60% por algo, então pega a tarefa A, completa e volta para B)    

    **Paralelismo** : 
     Definição 1: Paralelismo é sobre fazer muitas coisas ao mesmo tempo. <br/>
     Definição 2: É a execução simultânea de computações (possivelmente relacionadas). (Exemplo: suponha que existam duas tarefas A e B, ele pega ambas as tarefas e tenta completar ambas juntas)

    ![cocurrency_parllel](/img/cocurrency_parllel.jpg)
 
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

  14. ### Quais são as diferenças entre goroutines e threads?
      **Threads**: Uma thread é apenas uma sequência de instruções que pode ser executada independentemente por um processador. As threads usam muita memória devido à sua grande pilha e requerem chamada ao SO para recursos (como memória), o que é lento. Portanto, nem sempre garante um desempenho melhor do que processos neste mundo de processadores multi-core.

      **Goroutines**: Goroutines existem apenas no espaço virtual do runtime Go e não no SO. E uma goroutine é criada com inicialmente apenas 2KB de tamanho de pilha. Cada função em Go já tem uma verificação se mais pilha é necessária ou não e a pilha pode ser copiada para outra região da memória com o dobro do tamanho original. Isso torna a goroutine muito leve em recursos.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

  15. ### Para que servem os channels?
     
      Channels são os tubos que conectam goroutines concorrentes. Você pode enviar valores para channels de uma goroutine e receber esses valores em outra goroutine.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**    

  16. ### Você pode fazer algo em goroutines usando channels?
         * Channels são seguros para goroutines e podem armazenar e passar valores entre goroutines
         * Channels fornecem semântica FIFO.
         * Channels fazem com que goroutines bloqueiem e desbloqueiem, o que acabamos de aprender. 
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

  17. ### O que é um Closure?
    
         Um closure é um valor de função que referencia variáveis de fora de seu corpo. A função pode acessar e atribuir às variáveis referenciadas.<br/>
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

  18. ### O que são runtime e pacotes runtime?
    
      O pacote runtime contém operações que interagem com o runtime do Go, como funções para controlar goroutines ou que fornecem alguns detalhes sobre o ambiente de código do Go. É também responsável pela coleta de lixo, finalização, tempo limite e muitos outros recursos importantes.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

  19. ### Como você pode saber quantos núcleos seu computador tem?
    
      ```go
	  runtime.NumCPU()
	  ```
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   

  20. ### Como você diria a uma goroutine para usar menos núcleos do que você tem?
    
      ```go
	  runtime.GOMAXPROCS(1)
	  ```
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**  
  
  
  21. ### Como você determinaria o tipo de uma variável e qual pacote usar para isso?
    
      Para determinar o tipo de uma variável, você pode usar o pacote reflect.
   
      ```go
	  import (
	      "fmt"
	      "reflect"
      )
	  
	  func main() {
	      //declaring a interface variable
	      var message interface{} = 10
	      //getting the type of interface using reflect package
	      fmt.Println(reflect.TypeOf(message))
	  }
	  ```
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**  
  
  
  22. ### Quais tipos um map pode armazenar?
    
      Um map é um tipo de referência que armazena um conjunto não ordenado de pares chave-valor, e o tipo da chave especifica quais valores podem e quais não podem ser usados como chaves, como tipos comparáveis. Os valores de um map podem ser qualquer tipo: builtin, derived, ou interface, referência, ou função.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**  
  
  
  23. ### O que são microsserviços?
    
      Microsserviços - também conhecido como arquitetura de microsserviços - é um estilo arquitetônico que estrutura uma aplicação como uma coleção de serviços que são:
    
      * Altamente sustentáveis e testáveis
      * Fracamente acoplados
      * Independentemente implantáveis
      * Organizados em torno de capacidades de negócios
      * Mantidos por uma pequena equipe
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   
  
  
  24. ### Por que não existem classes em Go?
    
      Os criadores de Go decidiram adotar uma abordagem diferente para a programação orientada a objetos que não depende de classes, mas ainda alcança muitos dos mesmos objetivos:
    
      * Modularidade
      * Encapsulamento
      * Reutilização
    
      Em vez de classes, Go usa composição e interfaces para alcançar esses objetivos. As estruturas (structs) são usadas para compor dados, e métodos podem ser adicionados a qualquer tipo.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   
  
  
  25. ### Diferença entre tempo de compilação e tempo de execução?
    
      O tempo de compilação é o período em que o programa de código-fonte é traduzido para o código de máquina. Em outras palavras, é o tempo em que o compilador compila o código. Se houver erros no programa de origem, o compilador os sinaliza.
      
      O tempo de execução é o período em que o programa está em execução e geralmente ocorre após o tempo de compilação. Se houver erros durante o tempo de execução, o programa pode lançar exceções ou até mesmo falhar completamente.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   
  
  
  26. ### Como gerar um número verdadeiramente aleatório em golang?
    
     ```go
       package main
        import (
	       "crypto/rand"
	       "fmt"
	       "math/big"
       )
 
       func main() {
         n, err := rand.Int(rand.Reader, big.NewInt(10))
         if err != nil {
           panic(err)
         }
         fmt.Println(n)
       }
    ```
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   
  
  
  27. ### Por que as goroutines são leves?
    
      As goroutines são leves porque elas têm uma pequena pilha que cresce e diminui conforme necessário. Isso permite que sejam mais eficientes em termos de memória em comparação com threads do sistema operacional.
      
      Além disso, o escalonador do Go gerencia as goroutines de forma eficiente, permitindo que um grande número de goroutines seja executado concorrentemente em um número limitado de threads do sistema operacional.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   
  
  
  28. ### Se a capacidade não for definida em um slice, qual seria a capacidade?
    
      Se a capacidade não for definida em um slice, a capacidade será igual ao comprimento. Quando você cria um slice usando a função `make`, você pode especificar o comprimento e a capacidade. Se você não especificar a capacidade, ela será definida como o mesmo valor do comprimento.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   
  
  
  29. ### Qual é a maneira mais fácil de verificar se um slice está vazio?
    
      A maneira mais fácil de verificar se um slice está vazio é verificar se seu comprimento é zero:
      
      ```go
      if len(mySlice) == 0 {
          // O slice está vazio
      }
      ```
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)**   
  
  
  30. ### Qual é a vantagem do Go avaliar tipos implícitos em tempo de compilação?
    
      A vantagem de Go avaliar tipos implícitos em tempo de compilação é que ele pode detectar erros de tipo antes que o programa seja executado, o que pode economizar tempo e recursos. Além disso, isso permite que o compilador otimize o código para diferentes tipos, o que pode levar a um melhor desempenho.
      
      Como Go é uma linguagem fortemente tipada, a avaliação de tipos em tempo de compilação também torna o código mais seguro e menos propenso a erros em tempo de execução relacionados a tipos incompatíveis.
   
  **[ Voltar ao Topo ⬆ ](#sumário---golang)** 