### Table of Contents - Golang

| No. | Questions |
| --- | --------- |
|   | **Golang** |
| 1 | [What is Golang?](#what-is-golang)|
| 2 | [What are the pros and cons of Golang?](#what-are-the-pros-and-cons-of-golang)|
| 3 | [What kind of projects are suitable to be built in Golang?](#what-kind-of-projects-are-suitable-to-be-built-in-golang)
| 4 | [Is Golang an object oriented language?](#is-golang-an-object-oriented-language)
| 5 | [What are the data types in Golang?](#what-are-the-data-types-in-golang)
| 6 | [Can you return multiple values from a function?](#can-you-return-multiple-values-from-a-function)
| 7 | [What is a GOPATH?](#what-is-a-gopath)
| 8 | [What are Goroutines?](#what-are-goroutines)
| 9 | [What is nil in Go?](#what-is-nil-in-go)
| 10 | [What is the difference between array and slice in Go?](#what-is-the-difference-between-array-and-slice-in-go)
| 11 | [How does a go compiler work?](#how-does-a-go-compiler-work)
| 12 | [What is an Interface and Why do you use it?](#what-is-an-interface-and-why-do-you-use-it)
| 13 | [What are concurrency and parralism and what is the difference between both?](#what-are-concurrency-and-parralism-and-what-is-the-difference-between-both)
| 14 | [What are the difference between goroutines and threads?](#what-are-the-difference-between-goroutines-and-threads)
| 15 | [What are channels for?](#what-are-channels-for)
| 16 | [Can you do something in goroutines using channels?](#can-you-do-something-in-goroutines-using-channels)
| 17 | [What is a Closure?](#what-is-a-closure)
| 18 | [What are runtime  and runtime packages?](#what-are-runtime--and-runtime-packages)
| 19 | [How can you get how many cores your computer has?](#how-can-you-get-how-many-cores-your-computer-has)
| 20 | [How would you tell a goroutine to use less core than what you have?](#how-would-you-tell-a-goroutine-to-use-less-core-than-what-you-have)
| 21 | [How would you determine the type of a variable and Which package to use for it?](#how-would-you-determine-the-type-of-a-variable-and-which-package-to-use-for-it)
| 22 | [What all types can map store?](#what-all-types-can-map-store)
| 23 | [What are microservices?](#what-are-microservices)
| 24 | [Why are there no classes in Go?](#why-are-there-no-classes-in-go)
| 25 | [Difference between Compile time and runtime?](#difference-between-compile-time-and-runtime)
| 26 | [How to generate a true random number in golang?](#how-to-generate-a-true-random-number-in-golang)
| 27 | [Why are goroutines light-weight?](#why-are-goroutines-light-weight)
| 28 | [If capacity is not defined in slice, what would the capacity be?](#if-capacity-is-not-defined-in-slice,-what-would-the-capacity-be)
| 29 | [What is the easiest way to check if a slice is empty?](#what-is-the-easiest-way-to-check-if-a-slice-is-empty)
| 30 | [What is an advantage of Go evaluating implicit types at compile time?](#what-is-an-advantage-of-go-evaluating-implicit-types-at-compile-time)


1. ### What is Golang?


   Golang is a statically typed, compiled programming language designed at Google by Robert Griesemer, Rob Pike, and Ken Thompson. Golang was designed at Google in 2007 to improve programming productivity in an era of multicore, networked machines and large codebases.


**[ Back to Top ⬆ ](#table-of-contents---golang)**


2. ### What are the pros and cons of Golang?

	**Pros:**
	* Ease of use
    * A Smart Standard library
    * Strong security built-in
    * Garbage collected language.
    * Minimalism & Readability
    * Concurrency


    **Cons:**
    * No generics
    * Error-handling boilerplate & lack of compile-time checks unhandled errors
    * Shortage of high-level parallelism and concurrency features



**[ Back to Top ⬆ ](#table-of-contents---golang)**


3. ### What kind of projects are suitable to be built in Golang?
     * Cloud services 
     * Media platforms
     * Broadcast providers
     * Projects with microservice architecture

  **[ Back to Top ⬆ ](#table-of-contents---golang)**

4. ### Is Golang an object oriented language?
    
    Golang has types and methods and allows an object-oriented style of programming, there is no type hierarchy.Golang has some properties of object oriented programming like Encapsulation , Composition , but it doesn't have inheritance , classes , function overloading .


  **[ Back to Top ⬆ ](#table-of-contents---golang)**

5. ### What are the data types in Golang?

    1. **Basic type**: Numbers, strings, and booleans .
    2. **Aggregate type**: Array and structs .
    3. **Reference type**: Pointers, slices, maps, functions, and channels .
    4. **Interface type**


  **[ Back to Top ⬆ ](#table-of-contents---golang)**


6. ### Can you return multiple values from a function?

    Yes. A Go function can return multiple values, each separated by commas in the return statement.

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


  **[ Back to Top ⬆ ](#table-of-contents---golang)**    


7. ### What is a GOPATH?


    The GOPATH environment variable specifies the location of your workspace. It defaults to a directory named go inside your home directory    <br/>  
    The command go env GOPATH prints the effective current GOPATH; it prints the default location if the environment variable is unset.          

  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

8. ### What are Goroutines?

    Goroutines are incredibly lightweight “threads” managed by the go runtime. They enable us to create asynchronous parallel programs that can execute some tasks far quicker than if they were written in a sequential manner.

  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

9. ### What is nil in Go?
    nil is a predeclared identifier in Go that represents zero values for pointers, interfaces, channels, maps, slices and function types.

  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

10. ### What is the difference between array and slice in Go ?
    
    * **ARRAY** : An array is a fixed collection of data. The emphasis here is on fixed, because once you set the length of an array, it cannot be changed.<br/>
   
    ```go
	arr := [4]int{3, 2, 5, 4}
	```
    * **SLICE** : Slices are much more flexible, powerful, and convenient than arrays. Unlike arrays, slices can be resized using the built-in append function .

    ```go
	slicee := make([]Type, length, capacity)
	```

  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

11. ### How does a go compiler work?
   
    A Go compiler goes through the following steps , they are in brief , if we go in detail then you will need a complete book to understand each module, for interview purpose , I have attached a hand written note , I will generate a digital form soon 

    ![go compiler](/img/go_compiler.jpeg)

  **[ Back to Top ⬆ ](#table-of-contents---golang)**   


12. ### What is an Interface and Why do you use it?
    
    The interface is a collection of methods as well as it is a custom type.
    
    ```go
	package main
  
        import "fmt"
          
        // Creating an interface
        type tank interface {
          
            // Methods
            Tarea() float64
            Volume() float64
        }
          
        type myvalue struct {
            radius float64
            height float64
        }
          
        // Implementing methods of
        // the tank interface
        func (m myvalue) Tarea() float64 {
          
            return 2*m.radius*m.height +
                2*3.14*m.radius*m.radius
        }
          
        func (m myvalue) Volume() float64 {
          
            return 3.14 * m.radius * m.radius * m.height
        }
          
        // Main Method
        func main() {
          
            // Accessing elements of
            // the tank interface
            var t tank
            t = myvalue{10, 14}
            fmt.Println("Area of tank :", t.Tarea())
            fmt.Println("Volume of tank:", t.Volume())
        }    
	```

    Interfaces can make code clearer, shorter, more readable, and they can provide a good API between packages, or clients (users) and servers (providers).

  **[ Back to Top ⬆ ](#table-of-contents---golang)**   


  13. ### What are concurrency and parralism and what is the difference between both?
   
    **Concurrency** :  
    Defination 1 : Dealing with multiple things at once. <br/>
    Defination 2 : A Composition of independently executing processes(Example: suppose there are two tasks A and B , the way this work is A task done 70% meanwhile it has to wait for something , so it picks up task B and try to complete if suppose B task has to wait at 60% , for something then it picks up A task them completes it and comes back to B )    

    **Parralism** : 
     Defination 1 : Parallelism is about doing lots of things at once. <br/>
     Defination 2 : It is the simultaneous execution of (possibly related) computations. (Example: suppose there are two tasks A and B , it takes both tasks and try to complete both together )

    ![cocurrency_parllel](/img/cocurrency_parllel.jpg)
 
  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  14. ### What are the difference between goroutines and threads?
      **Threads** : A thread is just a sequence of instructions that can be executed independently by a processor. Threads  use a lot of memory due to their large stack and requires call to OS for resources (such as memory) which is slow. so doesn’t always guarantee a better performance than processes in this multi-core processor world.

      **Goroutines**:Goroutines exists only in the virtual space of go runtime and not in the OS. and A goroutine is created with initial only 2KB of stack size. Each function in go already has a check if more stack is needed or not and the stack can be copied to another region in memory with twice the original size. This makes goroutine very light on resources.
   
  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  15. ### What are channels for?
     
      Channels are the pipes that connect concurrent goroutines. You can send values into channels from one goroutine and receive those values into another goroutine.
   
  **[ Back to Top ⬆ ](#table-of-contents---golang)**    

  16. ### Can you do something in goroutines using channels?
         * Channels are goroutine-safe and can store and pass values between goroutines
         * Channels provide FIFO semantics.
         * Channels cause goroutines to block and unblock, which we just learned about. 
   
  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  17. ### What is a Closure?
    
         A closure is a function value that references variables from outside its body. The function may access and assign to the referenced variables.<br/>
   
  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  18. ### What are runtime  and runtime packages?
  
      The runtime library implements garbage collection, concurrency, stack management, and other critical features of the Go language. The Package runtime contains operations that interact with Go's runtime system, such as functions to control goroutines.
   
  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  19. ### How can you get how many cores your computer has?
      With the help of runtime package
     
      ```go
	     package main

         import (  
              "fmt"
              "runtime"
                )

            func main() {
            fmt.Println(runtime.NumCPU())
            }
	  ```
   
  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  20. ### How would you tell a goroutine to use less core than what you have?
      
        We can restrict the number of goroutines running at the same time , like below
 
  ```go
          package main

          import (
        	"flag"
        	"fmt"
        	"time"
        	"sync"
        ) 

        // Fake a long and difficult work.
        func DoWork() {
        	time.Sleep(500 * time.Millisecond)
        }
        
        func main() {
        	maxNbConcurrentGoroutines := flag.Int("maxNbConcurrentGoroutines", 2, "the number of goroutines that are allowed to run concurrently")
        	nbJobs := flag.Int("nbJobs", 5, "the number of jobs that we need to do")
        	flag.Parse()
        
        	concurrentGoroutines := make(chan struct{}, *maxNbConcurrentGoroutines)
        
        	var wg sync.WaitGroup
        
        	for i := 0; i < *nbJobs; i++ {
        		wg.Add(1)
        		go func(i int) {
        			defer wg.Done()
        			concurrentGoroutines <- struct{}{}
        			fmt.Println("doing", i)
        			DoWork()
        			fmt.Println("finished", i)
        			<-concurrentGoroutines
        		}(i)
        	}
        	wg.Wait()
        }
  ```
   
  **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  21. ### How would you determine the type of a variable and Which package to use for it?
      
      There are three different ways to find type of variable in Golang<br/>
       * **reflect.TypeOf Function**: Using the golang inbuilt package reflect we can find the Type of variable
            
            ```go
			    package main
  
             
                import (
                    "fmt"
                    "reflect"
                )

                func main(){
                var string_type =  "Hello Go";
                var complex_type =  complex(9, 15);
                
                 fmt.Println("string_type", reflect.TypeOf(string_type))
                 fmt.Println("complex_type = ", reflect.TypeOf(complex_type))
                }
			```
        * **reflect.ValueOf.Kind() Function** : Using the golang inbuilt package reflect we can find the Type of variable

             ```go
			    package main
  
              
                import (
                    "fmt"
                    "reflect"
                )

                func main(){
                var string_type =  "Hello Go";
                var complex_type =  complex(9, 15);
                
                 fmt.Println("string_type", reflect.ValueOf(string_type).Kind())
                 fmt.Println("complex_type = ", reflect.TypeOf(complex_type).Kind())
                }
			```
        * **%T with Printf** : You can use Printf also to find value of variable

            ```go
			    package main
  
             
                import (
                    "fmt"
                    "reflect"
                )

                func main(){
                var string_type =  "Hello Go";
                var complex_type =  complex(9, 15);
                
                 fmt.Printf("string_type=%T\n", string_type)
                 fmt.Printf("complex_type =%T\n", complex_type)
                }
			```
      
      **[ Back to Top ⬆ ](#table-of-contents---golang)**   




  22. ### What all types can map store?
      **Value** - The Value type of a mpa can be anything, including another map <br/>
      **Key** - The key type of Map can only be values that can be compared i.e - boolean, numeric, string, pointer, channel, and interface types, and structs or arrays , that excludes - slices, maps, and functions 
     
      **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  23. ### What are microservices?
      Microservices is an architectural style that structures an application as a collection of services that are
        * Highly maintainable and testable
        * Loosely coupled
        * Independently deployable
        * Organized around business capabilities
        * Owned by a small team <br/>

      **[ Back to Top ⬆ ](#table-of-contents---golang)**   

  24. ### Why are there no classes in Go ?
  
      Go doesn't require an explicit class definition as Java, C++, C#, etc do.  Instead, a "class" is implicitly defined by providing a set of "methods" which operate on a common type.  The type may be a struct or any other user-defined type.  For example:

      ```go
	  type Integer int;
        func (i *Integer) String() string {
            return strconv.itoa(i)
        }
	  ```
      is analogous to below code in java:<br/>

      ```java
	  class Integer {
            public int i;
            public String toString() { return Integer.toString(i); }
        }
	  ```
  **[ Back to Top ⬆ ](#table-of-contents---golang)**  

  25. ### Difference between Compile time and runtime?
      **Compile-time** is the time at which the source code is converted into an executable code <br/>
      **Run time** is the time at which the executable code is started running.

  **[ Back to Top ⬆ ](#table-of-contents---golang)**  


  26. ### How to generate a true random number in golang?
      The default number generator is deterministic, so it’ll produce the same sequence of numbers each time by default , so you need to seed it with different number you can do it with nano seconds like below <br/>
      
         ```go
	     package main
        import (
            "fmt"
            "math/rand"
             "time"
            )
        func main(){
        s1 := rand.NewSource(time.Now().UnixNano())
        r1 := rand.New(s1)
         fmt.Print(r1.Intn(100))
         }
	     ```

  **[ Back to Top ⬆ ](#table-of-contents---golang)**  


  27. ### Why are goroutines light-weight?
      A goroutine is created with initial only 2KB of stack size. Each function in go already has a check if more stack is needed or not and the stack can be copied to another region in memory with twice the original size. This makes goroutine very light

  **[ Back to Top ⬆ ](#table-of-contents---golang)**  

  28. ### If capacity is not defined in slice, what would the capacity be?
      It would be set by default to length of the slice 

  **[ Back to Top ⬆ ](#table-of-contents---golang)**  

  29. ### What is the easiest way to check if a slice is empty?
       You can use the length (len(slice)) property to find if the slice is empty

        ```go
		if(len(slice_data)==0){
        fmt.Println("Empty slice")
        }
		```
  **[ Back to Top ⬆ ](#table-of-contents---golang)**  

  30. ### What is an advantage of Go evaluating implicit types at compile time?
      Types can be implicitly inferred from expressions and don’t need to be explicitly specified.The special handling of interfaces and the implicit typing makes Go feel very lightweight and dynamic.

  **[ Back to Top ⬆ ](#table-of-contents---golang)**  
