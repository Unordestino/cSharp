# Exceções
* Uma exceção é qualquer condição de erro ou comportamento inesperado encontrado por um programa em execução

* No .NET, uma exceção é um objeto herdado da classe System.Exception

* Quando lançada, uma exceção é propagada na pilha de chamadas de 
métodos em execução, até que seja capturada (tratada) ou o
programa seja encerrado


# Estrutura try-catch-finaly

* Bloco Try
> Contém o código que representa a execução normal do trecho de código que pode acarretar em uma execução

* Bloco Catch
> Contém o codigo a ser executado caso uma exeção ocorra
> Deve ser especificado o tipo de exceção a ser tratada (upcasting é permitido)

* Bloco finally
> É um bloco que contém código a ser executado independentemente de ter ocorrido ou não uma execeção
> 
 Exemplo clássico: ```Fechar um arquivo ou conexão de banco de dados ao final do processamento.```

 ```
            try {
                int n1 = int.Parse(Console.ReadLine());
                int n2 = int.Parse(Console.ReadLine());

                int result = n1 / n2;

                Console.WriteLine(result);
                
            }
            catch (DivideByZeroException e) {
                Console.WriteLine("Error, Divisão por zero ");
            }
            catch (FormatException e) {
                Console.WriteLine("Error, Valor n reconhecido ");
            }
            finally {
                Console.WriteLine("Fim da aplicação");
            }
```
