### Arrays
Um Array é um conjunto de elementos de um mesmo tipo de dados onde cada elemento do conjunto é 
acessado pela posição no array que é dada através de um índice (uma sequência de números inteiros)
Um array de uma dimensão é também conhecido como vetor,e um array de mais de uma dimensão e conhecido como uma matriz.
```
string[] alunos = new string[5];
            alunos[0] = "Anderson";
            alunos[1] = "Bia";
            alunos[2] = "Carlos";
            alunos[3] = "Daniel";
            alunos[4] = "Emanuel";

            foreach (var aluno in alunos)
            {
                Console.WriteLine(aluno);
            }

            double somatorio = 0;
            double[] notas = { 9.7, 4.8, 8.4, 8.2, 6.8 };

            foreach (var nota in notas)
            {
                somatorio += nota;
            }

            double media = somatorio / notas.Length;
            Console.WriteLine(media);
```

### Declarando Arrays em C#

>Na linguagem C#  os arrays possuem o índice com base zero, ou seja, o primeiro elemento do array possui o índice zero (0).

>Um array de uma dimensão é declarado informando o tipo de dados do array seguido do nome do array, lembrando que devemos colocar colchetes ([]) depois do tipo do array e não após o seu nome:

>Ex:  int[] tabela; ==> correto     int tabela[];  ==> incorreto

>Na linguagem C# o tamanho do arrray não é parte do seu tipo, isso permite declarar uma array e em seguida atribuir qualquer array de objetos int a ele, sem considerar o seu tamanho:
```
Ex:      int[] numeros;                  //declara numeros como um array de inteiros de qualquer tamanho
         numeros = new int[10];          // numeros agora é um array de 10 elementos
         numeros = new int[20];          // numeros agora é um array de 20 elementos
```

