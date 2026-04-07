# Apostila de Algoritmo e Programação

# Capítulo: Introdução

_Professor:_  Evandro Jardini

## Conceitos iniciais

**Lógica**
 A lógica de programação é necessária para pessoas que desejam trabalhar com desenvolvimento de sistemas e
programas, ela permite definir a sequência lógica para o desenvolvimento.

Então o que é lógica?
>Lógica de programação é a técnica de encadear pensamentos para atingir determinado objetivo

**Sequência Lógica**  
Estes pensamentos, podem ser descritos como uma sequência de instruções, que devem ser seguidas para se cumprir uma determinada tarefa.  

>Sequência Lógica são passos executados até atingir um objetivo ou solução de um problema.

**Instruções**  

- Em informática, instrução é a informação que indica a um computador uma ação elementar a executar.
  
- Convém ressaltar que uma ordem isolada não permite realizar o processo completo, para isso é necessário um conjunto de instruções colocadas em ordem sequencial lógica.
  
- Por exemplo, se quisermos fazer uma omelete de batatas, precisaremos colocar em prática uma série de instruções:
  - Descascar as batatas, bater os ovos, fritar as batatas, etc...

- É evidente que essas instruções tem que ser executadas em uma ordem adequada: **não se pode bater os ovos da omelete antes de quebrá-los**.

**Algoritmo**  

- Um algoritmo é formalmente uma sequência finita de passos que levam a execução de uma tarefa.
- Podemos pensar em algoritmo como uma receita, uma sequência de instruções que dão cabo de uma meta específica.
- Estas tarefas não podem ser redundantes nem subjetivas na sua definição, devem ser claras e precisas.
- Exemplo:
* Algoritmo para somar dois números quaisquer*:
```
Escreva o primeiro número no retângulo A.
Escreva o segundo número no retângulo B.
Some o número do retângulo A com o número do retângulo B.
Coloque o resultado da soma de A com B no retângulo C.

Retangulo A        Retangulo B             Retangulo C
 ┌──────┐          ┌──────┐                  ┌──────┐                                   
 │  ?   |          │  ?   |                  │  ?   |
 └──────┘          └──────┘                  └──────┘
```


## Formas de Representação de Algoritmos  

**Descrição Textual ou Narrativa**

- VANTAGENS:  
 - O português é bastante conhecido por nós;
- DESVANTAGENS:  
 - imprecisão;  
 - pouca confiabilidade (a imprecisão acarreta a desconfiança);  
 - extensão (normalmente, escreve-se muito para dizer pouca coisa).

<br/>
<br/>
<br/>

**Fluxograma**  

O fluxograma é um tipo de algoritmo que utiliza símbolos gráficos para representar as ações ou instruções a serem seguidas.  

Assim como o pseudocódigo, o fluxograma é utilizado para organizar o raciocínio lógico a ser seguido para a resolução de um problema ou para definir os passos para a execução de uma tarefa. 

Também é utilizado para documentar rotinas de um sistema, mas só é recomendado para os casos pouco extensos.  


**Pseudolinguagens**

O pseudocódigo é um tipo de algoritmo que utiliza uma linguagem flexível, intermediária entre a linguagem Narrativa e a linguagem de programação.

É também para documentar rotinas de um sistema.

A palavra 'pseudocódigo' significa 'falso código'. Esse nome se deve à proximidade que existe entre um algoritmo escrito em pseudocódigo e a maneira pela qual um programa é representado em uma linguagem de programação.


**Fases**
Entretanto ao montar um algoritmo, precisamos primeiro dividir o problema apresentado em três fases fundamentais.

```mermaid
flowchart LR
    A(ENTRADA) --> B(PROCESSAMENTO);
    B --> C(SAÍDA);

```

Onde temos:
**ENTRADA**: São os dados de entrada do algoritmo;  
**PROCESSAMENTO**: São os procedimentos utilizados para chegar ao resultado final;  
**SAÍDA**: São os dados já processados. São as informações.  


### Exemplo de Algoritmo
Imagine o seguinte problema:  
- Calcular a média final dos alunos da disciplina de algoritmos.
- Sabendo que a média é calculada por: (Prova1 + Prova2 + Prova3 + Prova4) /4

Para montar o algoritmo proposto, faremos três perguntas:  

* **Quais são os dados de entrada?**  
  R: Os dados de entrada são Prova1, Prova2, Prova3 e Prova4.
  
* **Qual será o processamento a ser utilizado?**  
  R: O procedimento será somar todos os dados de entrada e dividi-los por 4 (quatro)
  
* **Quais serão os dados de saída?**  
  R: O dado de saída será a média final.  

  



Inicialmente, temos de solicitar as 4 notas, depois calcular a média e, por mim, mostrar ao usuário a média das notas:

```Go
Algoritmo
• Receba a nota da prova1  // Entreda de dados  
• Receba a nota de prova2  // Entreda de dados  
• Receba a nota de prova3  // Entreda de dados    
• Receba a nota da prova4  // Entreda de dados  

• Some todas as notas  // Processamento de dados
• divida o resultado da soma por 4  // Processamento dos dados

• Mostre o resultado da divisão  // Saída dos daddos.
```

## Atributos e Tipo de Dados

**Variáveis** e **constantes** são os elementos básicos que um programa manipula. 

**Variáveis**

Uma variável é:
• Um espaço reservado na memória do computador para armazenar um tipo de dado determinado.  
• Como se fosse uma caixa na memória RAM onde se guarda um dado específico em um formato pré-determinado.  
* Cada váriável vai reservar um local na memória para guardar um dado.  

```mermaid
block
columns 3
Memória:3
block:group1:3    
    A["Variável A"] B["Variável B"] C["Variável C"]
end
```

As Variáveis devem receber nomes para poderem ser referenciadas e modificadas quando necessário.  

**Exemplos de nomes de variáveis**:
 - *codigo_da_peca*
 - *aux*
 - *temp*
 - *i*
 - *casa1* 

Os nomes devem ter as seguintes propriedades:  
 - Não utilizar espaços entre as letras. Em vez de usar *volume de chuva*, o correto pode ser *volumeChuva*, *volume_de_chuva* ou *volume_chuva*.
   
 – Não iniciar o nome da variável com números:  
  - Em vez de *2valor*, use *valor2*.

- Não utilizar **palavras reservadas**, isto é, palavras que são utilizadas nos algoritmos para representar ações específicas.
  - A particula *se* é usada para representar uma condição lógica.
  - A palavra *var* é usada para representar a área de declaração de  variáveis.
    
- Não utilizar caracteres especiais, como acentos, síbolos (? : / @ # & etc).

**Tipo de dados**

Embora uma variável possa assumir diferentes valores, ela só pode armazenar um valor a cada 
instante.  
Um programa deve conter declarações que especificam de que *tipo de dados* são as variáveis que ele utilizará e *as vezes* um valor inicial.  

❗ Os tipos de dados indicam o que a variável pode receber.

Alguns tipos de dados:  
 - **Inteiro**: são para armazenamento de números inteiros.
 - **Real**: são para o armazenamento de números que possuam casas decimais.
 - **Literal** ou **caracter**: Específicas para dados que contenham letras e/ou números.
   - Pode em determinados momentos conter somente dados literais ou somente numéricos.
   - Se usado somente para armazenamento de números, **não poderá** ser utilizada para operações matemáticas.
   - A atribuição direta a uma variável do tipo literal deve ser feita usando aspas "valor".
     - Exemplo: ingrediente <- "farinha"

**Representação da memória de duas vaiáveis do tipo de dados literal e um valor já atribuído**

```mermaid

erDiagram
    Cor {
        Literal Verde        
    }

    Cidade {
        Literal Votuporanga
    }

```

**Declaração de Variáveis**
- As variáveis, antes de serem utilizadas, devem ser declaradas numa seção do próprio algoritmo.  
- Esta seção é definida com a palavra reservada *var*.
- Na declaração de uma variável deve ser indicado seu nome e seu tipo de dado.
- Exemplo:

```Go
var
  cor :literal
  cidadde :caracter
  idade :inteiro
  salario :real

```
