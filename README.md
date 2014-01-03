.todo
=====

> Uma sintax para escrever uma To Do List

## Como funciona

Isso é uma sintaxe para criar uma To Do List pequena, de forma que no seu próprio editor de código você consiga listar de forma simples de entender o que você precisa fazer, o que você já fez e o que tem alguma observação a ser verificada

Básicamente, isso implica em ter um arquivo chamado `.todo` na raiz de um projeto, ou qualquer outro local que você queira usar.

É recomendado usar isso para To Do Lists pequenas, se você precisar de grandes To Do Lists, você pode usar ferramentas mais completas para isso como Trello, entre outras disponíveis.

Neste arquivo `.todo` temos uma lista não ordenada onde o delimitador * inicia um item da To Do List e o item é fechado assim que é encontrado outro demilitador, seja ele qual for.

### Primeira To Do List
**Exemplo 1.0**
```text
* Fazer compras no mercado
* Preparar lanche da tarde
* Desligar todas as luzes antes de dormir
```

### To Do List com itens aninhados
**Exemplo 1.1**
```text
* Fazer compras no mercado
    * Comprar Queijo
    * Comprar Peito de Peru
    * Comprar Coca-Cola
* Preparar lanche da tarde
* Desligar todas as luzes antes de dormir
```

### To Do List com descrição de um item da lista
Também é permitido uma descrição de um item delimitados por > (maior que), um item automáticamente pega como sua descrição, o > a logo depois de sua própria declaração
**Exemplo 1.2**
```text
* Fazer compras no mercado
    > Perguntar para a esposa o que precisa
* Preparar lanche da tarde
```
**Exemplo 1.3**
```text
* Fazer compras no mercado
    > Perguntar para a esposa o que precisa
    * Comprar Queijo
    * Comprar peito de Peru
        > Lembrar de checar o dia que foi aberto
    * Comprar Coca-Cola
* Preparar lanche da tarde
```

O mesmo pode ser usado para itens aninhados

### Item completado
Ao finalizar um item, basta usar o delimitador #, invés do * para dizer que o item foi completado
**Exemplo 1.4**
```text
# Fazer compras no mercado
* Preparar lanche da tarde
* Desligar todas as luzes antes de dormir
```

Assim, sabemos que o primeiro item da lista foi completado

### Item com observação

Por vários motivos você pode precisar fazer uma observação a algum item da lista, somos que você foi ao mercado, mas não trouxe o Queijo, por que você não trouxe o queijo?
**Exemplo 1.5**
```text
* Fazer compras no mercado
    * Comprar Queijo
        ! Não tinha queijo
    * Comprar Coca-Cola
* Preparar lanche da tarde
```

## Obrigatoriedades da sintax

É de suma importânia que qualquer arquivo .todo seja indentado apenas com um tipo de indentação, não sendo possível misturar espaços com tabs, nem tabs do tamanho de 2 espaços com tabs do tamanho de 4 espaços. Caso isso seja encontrado, o parser deve retornar um erro.

### Exemplos de listas com boa indentação:

Usando 4 espaços
```text
* Item 1
    * Sub item 1
* Item 2
```

Usando 2 Espaços
```text
* Item 1
  * Sub item 1
* Item 2
```

Usando tab do tamanho de 2 espaços
```text
* Item 1
	* Sub item 1
* Item 2
```

### Exemplo de listas com má indentação:

Usando tabs e espaços
```text
* Item 1
	  * Sub item 1
* Item 2
```

```text
* Item 1
  * Sub item 1
	* Sub item 2
* Item 2
```

## To Do List

* Criar plugin de sintaxe highlight para sublime
* Obter feedbacks sobre esse ideia, e verificar se já não existe algo semelhante

## Projetos similares
 * [PlainTasks](https://github.com/aziz/PlainTasks)