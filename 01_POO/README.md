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


