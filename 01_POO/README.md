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
