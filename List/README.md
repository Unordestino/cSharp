### Codigo List
```
List<string> l = new List<string>();

            l.Add("Maria");
            l.Add("Alex");
            l.Add("Bob");
            l.Add("Anna");
  ```
  ```l.Insert(2, "Marco");``` // Adiciona outro elemento a lista
   
  ```string s1 = l.Find(x => x[0] == 'A');``` // Mostra o primeiro elemento que começa com a letra 'A'
   
  ```string s2 = l.FindLast(x => x[0] == 'A');``` //  Mostra o ultimo elemento que começa com a letra 'A'
   
  ``` int pos1 = l.FindIndex(x => x[0] == 'A');``` // Mostra posição do primeiro elemento que começa com 'A'
   
  ```int pos2 = l.FindLastIndex(x => x[0] == 'A'); ```// Mostra posição do ultimo elemento que começa com 'A'
   
  ``` l.Remove("Alex"); ```// Remove um elemento da lista
   
  ```l.RemoveAll(x => x[0] == 'M');``` // Remove todos os elemento que começa com M
  

