### Introdução

C# : uma linguiagem de programação
DotNet : .NET(2002): uma plataforma de desenvolvimento para se criar diversos tipos de aplicações, podendo usar várias linguagens de programação.

### Atalhos para Microsoft Visual Studio
```
Ctrl + K + C -> Comenta todo o codigo selecionado
Ctrl + D - > Duplica a linha de codigo 
Ctrl + Alt -> Utilizando a setinha pra cim ou para baixo cnsegue mover a linha de codigo
Ctrl + F5 -> Compila a aplicação
Ctrl + K + D - > Organiza todo o codigo automaticamente 
```
### Regras C#
* Começar com uma letra ou sublinhado ou @
* Maiúsculas e minúculas fazem diferença
* Só usa letras, números e sublinhado
* Podemos usar acentos
* Não pode conter espaços 
* Não pode ser palavra reservada

### Tipos de inteiros
>OBS ```Ushort, Uint, Ulong ``` Converte em positivo
* Byte.MinValue // O tipo byte vai de 0 até 255
* Sbyte.MaxValue // O tipo sbyte vai de -128 até 127
* Short.MinValue // O tipo short vai de - 32768 até 32767
* Ushort.MinValue // O tipo ushort vai de 0 até 65535

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
#### Debugging
```
F9 -> Marcar/Desmarcar breakpoint
F5 -> Iniciar/Continuar o bug
F10 -> Executar um passo (Pula função)
F11 -> Executar um passo (entra na função)
SHIFT + F11 -> sair do método em execução
SHIFT + F5 -> parar debug
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

### Split - coding

```
int.TryParse(Console.ReadLine(), out int n1);
char.TryParse(Console.ReadLine(), out char ch);
double.TryParse(Console.ReadLine(), out double n2);

string[] vet = Console.ReadLine().Split(' ');

string nome = vet[0];
char sexo = char.Parse(vet[1]);
int idade = int.Parse(vet[2]);

```
```
Console.Write("Dia");

string lineDia1 = Console.ReadLine();
string[] vet3 = lineDia1.Split(' ');
int.TryParse(vet3[0], out int diaInicial);

string line = Console.ReadLine();
string[] vet1 = line.Split(':');
int.TryParse(vet1[0], out int horaInicial);
int.TryParse(vet1[1], out int minutoInicial);
int.TryParse(vet1[2], out int segundoInicial);

```

### Randorizador (Command)
>Gera números aleatorios
```
Random gerador = new Random();
int n = gerador .Next(4, 50); // Números aleatorios de 4 a 49 
```
### Inverte frase (Coding)
```
string frase = Console.ReadLine();
char[] array = frase.ToCharArray();
Array.Reverse(array);
Console.WriteLine(array);
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
### Meotodo Trim 
Revome os espaços de inicio e fim
```
string msg = "         Hello World        ";
Console.ReadLine(msg.Trim);
```


