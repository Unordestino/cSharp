# Pilares Do POO
* Abstração
* Herança
* Encapsulamento
* Pocimorfismo

# Parametros por Referencia(Red/Out)
  ```
class ParametrosPorReferencia
    {
        public static void AlterarRef(ref int numero)
        {
            numero = numero + 1000;
        }

        public static void AlterarOut(out int numero1, out int numero2)
        {

            numero1 = 0;
            numero2 = 0;
            numero1 = numero1 + 15;
            numero2 = numero2 + 30;
        }
```

> Tipos ``` Ref para duas direções entrada e saida / Out apenas uma direção de saida ```

```
   static void Main(string[] args)
        {
            int a = 3;
            AlterarRef(ref a);
            Console.WriteLine(a);

            int b = 2;
            AlterarOut(out b, out int c);
            Console.WriteLine($"{b} {c}");

        }
```

# sealed class
>Quando aplicado a uma classe, o modificador sealed impede que outras classes herdem dela. No exemplo a seguir,
>a classe B herda da classe A, mas nenhuma classe pode herdar da classe B.

```
class A {}
sealed class B : A {}
```

# TermoThis

>Faz Referencia A classe ```Acessar``` sendo assim podendo utilizar a variavel ```senha``` que antes dava conflito.

```
    class Acessar
    {
        string senha = "abc123";

        public bool Login(string senha)
        {
            return this.senha == senha;
        }

    }
```

# Delegate

Um delegado é um tipo que encapsula com segurança um método, semelhante a um ponteiro de função em C e C++. No entanto, ao contrário dos ponteiros de função de C, delegados são orientados a objeto, fortemente tipados e seguros. O tipo de um delegado é definido pelo nome do delegado. O exemplo a seguir declara um delegado chamado Del que pode encapsular um método que usa uma cadeia de caracteres como um argumento e retorna nulo:

```
    class Matematica
    {
        public void Somar (int n1, int n2)
        {
            Console.WriteLine("A soma é: "+(n1 + n2));
        }

        public void Subtrair (int n1, int n2)
        {
            Console.WriteLine("A subtração é: " + (n1 - n2));
        }

        public void Dividir (int n1, int n2)
        {
            Console.WriteLine("A divisão é: "+ (n1 / n2));
        }

        public void Multiplicar(int n1, int n2)
        {
            Console.WriteLine("A multiplicação é: " + (n1 * n2));
        }
```

>Um objeto delegado é normalmente construído fornecendo-se o nome do método que o delegado encapsulará ou com uma função anônima. Quando um delegado é instanciado, uma >chamada de método feita ao delegado será passada pelo delegado para esse método. Os parâmetros passados para o delegado pelo chamador são passados para o método e o >valor de retorno, se houver, do método é retornado ao chamador pelo delegado. Isso é conhecido como invocar o delegado. Um delegado instanciado pode ser invocado como >se fosse o método encapsulado em si.

```
class Program
    {
        delegate void Operacao(int num1, int num2);

        static void Main(string[] args)
        {
            Matematica m = new Matematica();

            Operacao conta = null;

            conta += m.Somar;
            conta += m.Subtrair;
            conta += m.Multiplicar;
            conta += m.Dividir;
            conta += m.Multiplicar;

           conta(10, 2);
         
           Console.WriteLine("");

            conta -= m.Dividir;
            conta -= m.Subtrair;

            conta(10, 2);

        }

```

# Classes parciais

>Ao trabalhar em projetos grandes, dividir uma classe em arquivos separados permite que vários programadores trabalhem ao mesmo tempo.
>Ao trabalhar com código-fonte gerado automaticamente, o código pode ser adicionado à classe sem precisar recriar o arquivo de origem. O Visual Studio usa essa abordagem quando cria Windows Forms, código de wrapper de serviço Web e assim por diante. Você pode criar código que usa essas classes sem precisar modificar o arquivo que o Visual Studio cria.
>Ao usar geradores de origem para gerar funcionalidade adicional em uma classe.
Para dividir uma definição de classe, use o modificador de palavra-chave partial, como mostrado aqui:

```
    partial class Pessoa
    {

        public void Apresentar()
        {
            Console.WriteLine("Ola eu sou" + nome);
        }

        public static int CalCularIdade(int anoNascimento)
        {
            return DateTime.Now.Year - anoNascimento;
        }
    }
```
>A palavra-chave partial indica que outras partes da classe, struct ou interface podem ser definidas no namespace. Todas as partes devem usar a palavra-chave partial. Todas as partes devem estar disponíveis em tempo de compilação para formar o tipo final. Todas as partes devem ter a mesma acessibilidade, tais como public, private e assim por diante. ```OBS: são duas claes criadas interligadas ```

    partial class Pessoa
    {
        public static int maioridade = 18;

        public string nome;
        public int idade;

    }
      
# Propriedades da classe get e set

>O corpo do acessador get assemelha-se ao de um método. Ele deve retornar um valor do tipo de propriedade. A execução do acessador get é equivalente à leitura do valor do campo. Por exemplo, quando você estiver retornando a variável particular do acessador get e as otimizações estiverem habilitadas, a chamada ao método do acessador get será embutida pelo compilador, portanto, não haverá nenhuma sobrecarga de chamada de método. No entanto, um método do acessador get virtual não pode ser embutido porque o compilador não sabe, em tempo de compilação, qual método pode >ser chamado em tempo de execução. A seguir está um acessador get que retorna o valor de um campo particular _name:

```
    class Teste
    {
        private string _nome;
        public string sobrenome { get; } = "Silveira";

        private int _idade;

        public string Nome
        {
            get
            {
                return _nome; 
            }

            set
            {
                _nome = value;
            }
        }

        public int Idade
        {
            get
            {
                return _idade;
            }

            set
            {
               if(value < 18)
                {
                    Console.WriteLine("idade não permetida!");
                }
                else
                {
                    _idade = value;
                }
            }
        }
```
>O acessador set é semelhante a um método cujo tipo de retorno é void. Ele usa uma parâmetro implícito chamado value, cujo tipo é o tipo da >propriedade. No exemplo a seguir, uma acessador set é adicionado à propriedade Name: 
