### Entrada de dados
> 
```
int n = int.Parse(Console.ReadLine());

string nome = Console.ReadLine();

int n = Convert.ToInt32(Console.ReadLine());

int.TryParse(Console.ReadLine(), out int n);

```

### Regras C#
* Começar com uma letra ou sublinhado ou @
* Maiúsculas e minúculas fazem diferença
* Só usa letras, números e sublinhado
* Podemos usar acentos
* Não pode conter espaços 
* Não pode ser palavra reservada

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
> 
Variavel Privada : ``` Somente pode ser acessada através do proprio script ```

Variavel Publica : ``` Pode ser acessada através de outros script ```
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
