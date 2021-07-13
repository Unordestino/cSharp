### Regras C#
* Começar com uma letra ou sublinhado ou @
* Maiúsculas e minúculas fazem diferença
* Só usa letras, números e sublinhado
* Podemos usar acentos
* Não pode conter espaços 
* Não pode ser palavra reservada

### Entrada de dados
> 
```
int n = int.Parse(Console.ReadLine());

string nome = Console.ReadLine();

int n = Convert.ToInt32(Console.ReadLine());

int.TryParse(Console.ReadLine(), out int n);

```
### Tabulações
```
\n Nova linha
\t Tabulação
\b Backspace
\A alerta
\\ Utiliza "\" Barra
\" Utiliza aspas
```

### Criar Documentarios 
>Comentarios em c#
```
#region
Console.WriteLine("Este é meu codigo comentado: ");
#endregion
```

### Tipos de conversões
* Conversões implicita 
* Conversões explícita
* Conversões por classes auxiliares

**Conversões implicita int -> float**
```
int a = 8;
float b = a;
```
**Conversões explicita float -> int**
```
float a = 8,9999f;
int b  = (int)a;
```
**Conversões por classes auxiliares**
```
float a = 8,9999f;
int b = Convert.ToInt16(a);
```

### Variavel 
>**Um objeto na memoria capaz de armazenar dados de diversos tipos.**

>Variavel Privada : ``` Somente pode ser acessada através do proprio script ```

>Variavel Publica : ``` Pode ser acessada através de outros script ```

### interporlações de variaveis 
>Meios de usar variaveis para ser impresso no console
```
Console.WriteLine("A soma de " + num1 + " + " + num2 + " é igual: " + (num1 + num2));
Console.WriteLine("A soma de {0} + {1} é igual: {2}", num1, num2, num1 + num2);
Console.WriteLine($"A soma de {num1} + {num2} é igual: {num1 + num2}");
```

### Formatações númericas
* :C ```Monetário```
* :D ```Decimal```
* :N ```Númerico```
* :E ```Cientifico```
* :X ```Hexadecimal```
>Exemplo de como usar
```
double num1 = 2356;
double num2 = 324;
Console.WriteLine("A soma de {0} + {1} é igual: {2:N3}", num1, num2, num1 / num2);
Console.WriteLine($"A soma de {num1} + {num2} é igual: {num1 / num2:N2}");
```

### Classes 
``` É uma forma de agrupar metodos e variáveis juntas ```
> **manter o código flexivel e minimizar repetições.**

> As classes dão suporte completo à herança, uma característica fundamental da programação orientada a objetos.
> Ao criar uma classe, você pode herdar de qualquer outra classe que não está definida como e outras classes podem herdar de sua classe
> e substituir métodos virtuais sealed de classe. Além disso, você pode implementar uma ou mais interfaces.

### Metodos 
> **Um meio de isolar o codigo que executa uma tarefa especifica e que possa ser chamada de outros lugares.**

>Um método é um bloco de código que contém uma série de instruções. 
>Um programa faz com que as instruções sejam executadas chamando o método e especificando os argumentos de método necessários

### Randorizador (Command)
>Gera números aleatorios
```
Random gerador = new Random();
int n = gerador .Next(4, 50); // Números aleatorios de 4 a 49 
```
### DateTime Dia, Mês, Ano (Command)
>Para definir : Hora, Minuto, Segundo, Ano, Mes e Dia atual do usuario!
```
int hora = DateTime.Now.Hour;
int minuto = DateTime.Now.Minute;
int segundo = DateTime.Now.Second;
int ano = DateTime.Now.Year;
int mes = DateTime.Now.Month;
int dia = DateTime.Now.Day;
```
### Temporizador Sleep (Command)
>Dar um delay ao progresso da aplicação

>OBS: é preciso utilizar  a biblioteca ```System.Threading```
```
Thread.Sleep(1000); //Adicionar um delay de mil milissegundos = 1 segundo para continuar a leitura do codigo
```

### Limpa Tela (Command)
```
Console.Clear();
```

### Imprime mensagem (Command)
```
Console.WriteLine();
```

### Pause o Programa (Command)
```
Console.WriteLine();
```

### Ordena Posição Do Texto (Command)
```
Console.SetCursorPosition(10,3);
```
### Cor Do Texto (Command)
```
Console.ForegroundColor = ConsoleColor.Blue
```
### Cor Do Fundo (Command)
```
Console.BackGroundColor = Console.Blue
```
### Reseta Color (Command)
```
Console.ResetColor ();
```


