# 2 VARIÁVEIS E TIPOS DE DADOS SIMPLES

> Página 57

Ao executar *hello_world.py*, o arquivo terminado em *.py* indica que é um programa Python. Seu editor então passa o programa pelo interpretador
Python, que lê o programa todo e determina o que cada palavra significa.
Por exemplo, quando vê a palavra **`print`**, o interpretador exibe na tela o que quer que esteja dentro dos parênteses.

## Variáveis

Toda variável armazena um valor, que é a informação associada a essa variável.
<<<<<<< Updated upstream
### FAÇA VOCÊ MESMO

Escreva um programa separado para resolver cada um destes exercícios. Salve cada programa com um nome de arquivo que siga as convenções-padrão de
Python, com letras minúsculas e underscores, por exemplo, *simple_message.py* e
*simple_messages.py*.
=======

### FAÇA VOCÊ MESMO

Escreva um programa separado para resolver cada um destes exercícios. Salve cada programa com um nome de arquivo que siga as convenções-padrão de
Python, com letras minúsculas e underscores, por exemplo, [simple_message.py](D:\repoCode\ws-python\python-crash-course\python_work\simple_message.py) e
[simple_messages.py](D:\repoCode\ws-python\python-crash-course\python_work\simple_messages.py).
>>>>>>> Stashed changes

**2.1 – Mensagem simples:**  
Armazene uma mensagem em uma variável e, em
seguida, exiba essa mensagem.

**2.2 – Mensagens simples:**  
Armazene uma mensagem em uma variável e, em
seguida, exiba essa mensagem. Então altere o valor de sua variável para uma nova mensagem e mostre essa nova mensagem.

## Strings

> Página 61

Uma **string** é simplesmente uma série de caracteres. Tudo que estiver entre aspas é considerada uma string em Python, e você pode usar aspas *simples* ou *duplas* em torno de suas strings, assim.

`"This is a string."`
`'This is also a string.'`

Essa flexibilidade permite usar aspas e apóstrofos em suas strings:

```py
'I told my friend, "Python is my favorite language!"'
"The language 'Python' is named after Monty Python, not the snake."
"One of Python's strengths is its diverse and supportive community."
```

### Mudando para letras maiúsculas e minúsculas em uma string usando métodos

```py
name = "ada lovelace"
print(name.title())

# Output:   Ada Lovelace
```

O método **`title()`** aparece depois da variável
na instrução `print()`.

* Um método é uma ação que Python pode executar em
um dado.

O ponto (**.**) após **name** em **`name.title()`** informa ao Python que o método `title()` deve atuar na variável **name**.

* Todo método é seguido de um conjunto de parênteses, pois os métodos, com frequência, precisam de informações adicionais para realizar sua tarefa.  
Essas informações são fornecidas entre os parênteses. A função `title()` não precisa de nenhuma informação adicional, portanto seus parênteses estão vazios.  

**`title()`** exibe cada palavra com uma letra maiúscula no início.

Vários outros métodos úteis estão disponíveis para tratar letras
maiúsculas e minúsculas também. Por exemplo, você pode mudar uma
string para que tenha somente letras maiúsculas ou somente letras
minúsculas, assim:

```py
name = "Ada Lovelace"
print(name.upper())
print(name.lower())
```

Essas instruções exibirão o seguinte:

```py
>>> ADA LOVELACE
>>> ada lovelace
```


O método lower() é particularmente útil para armazenar dados. Muitas
vezes, você não vai querer confiar no fato de seus usuários fornecerem
letras maiúsculas ou minúsculas, portanto fará a conversão das strings para
letras minúsculas antes de armazená-las.

### Combinando ou concatenando strings

Muitas vezes, será conveniente combinar strings. Por exemplo, você pode querer armazenar um primeiro nome e um sobrenome em variáveis
separadas e, então, combiná-las quando quiser exibir o nome completo de alguém:

```py
first_name = "ada"
last_name = "lovelace"
full_name = first_name + " " + last_name # u

print(full_name)
```

* Python usa o símbolo de adição (+) para combinar strings.
* Esse método de combinar strings se chama *concatenação*.

```py
first_name = "ada"
last_name = "lovelace"
full_name = first_name + " " + last_name

print("Hello, " + full_name.title() + "!")
```

Esse código devolve uma saudação simples, porém formatada de modo elegante

```py
message = "Hello, " + full_name.title() + "!"
print(message)
```

armazenando a mensagem em uma variável, deixa a instrução *print* final muito mais simples.

### Acrescentando espaçosem branco em strings com tabulações ou quebras de linha

Em programação, *espaços em branco* se referem a qualquer caractere que não é mostrado, como espaços, tabulações e símbolos de fim de linha.

<<<<<<< Updated upstream
* Para acrescentar uma tabulação em seu texto, utilize a combinaçã de caracteres `\t`:  
=======
* Para acrescentar uma tabulação em seu texto, utilize a combinação de caracteres `\t`:  
>>>>>>> Stashed changes

```py
In [1]: print("Python")
Python

In [2]: print("\tPython")
        Python
```

Para acrescentar uma quebra de linha em uma string, utilize a combinação de caracteres `\n`:

```py
In [3]: print("Languages:\nPython\nC\nJavaScript")     
Languages:
Python
C
JavaScript
```

Também podemos combinar tabulações e quebras de linha em uma única string. A string "\n\t" diz a Python para passar para uma nova linha e
iniciar a próxima com uma tabulação.

```py
print("Languages:\n\tPython\n\tC\n\tJavaScript")
Languages:
        Python
        C
        JavaScript
```

Quebras de linha e tabulações são muito úteis quando geramos muitas linhas de saída usando apenas algumas linhas de código.

<<<<<<< Updated upstream
### Removendo espaçosembranco

> página 65

[to be continued...]() 
=======
### Removendo espaços em branco

> página 65

Python é capaz de encontrar espaços em branco dos lados direito e
esquerdo de uma string.  

**`rstrip()`** - O método garante que não haja espaços em branco do lado direito de uma string.

```py
u >>> favorite_language = 'python '
v >>> favorite_language
'python '
w >>> favorite_language.rstrip()
'python'
x >>> favorite_language
'python '
```
O valor armazenado em *favorite_language* em **u** contém um espaço em
branco extra no final da string.  
podemos ver o espaço no final do valor **v**.  
Quando o método **`rstrip()`** atua na variável *favorite_language* em **w**, esse espaço extra é removido.   Entretanto, a remoção é temporária. Se solicitar o valor de *favorite_language* novamente, você poderá ver que a string é a mesma que foi fornecida, incluindo o espaço em branco extra **x**.  
Para remover o espaço em branco da string de modo permanente, você
deve armazenar o valor com o caractere removido de volta na variável:

```py
u >>> favorite_language = favorite_language.rstrip()
>>> favorite_language
'python'
```
Para remover o espaço em branco da string, você deve remover o espaço
em branco do lado direito da string e então armazenar esse valor de volta
na variável original, como mostrado em **u**.

>  Alterar o valor de uma variável e então armazenar o novo valor de volta na variável original é uma operação frequente em programação. É assim que o valor de uma variável pode mudar à medida que um programa é executado ou em resposta à entrada de usuário.

Também podemos remover espaços em branco do lado esquerdo de uma
string usando o método **`lstrip()`**, ou remover espaços em branco dos dois
lados ao mesmo tempo com **`strip()`**:

 ```py
 u >>> favorite_language = ' python '
 v >>> favorite_language.rstrip()
 ' python'
 w >>> favorite_language.lstrip()
 'python '
 x >>> favorite_language.strip()
 'python'
 ```

Nesse exemplo, começamos com um valor que tem espaços em branco
no início e no fim **u**. Então removemos os espaços extras do lado direito
em **v**, do lado esquerdo em **w** e de ambos os lados em **x**.

> No mundo real, essas funções de remoção são usadas com mais frequência para limpar entradas de usuário antes de armazená-las em um programa.

## Evitando erros de sintaxe com strings

> página 67

Eis o modo de usar aspas simples e duplas corretamente. Salve este programa como *apostrophe.py* e então execute-o:

```py
message = "One of Python's streingths is its diverse community"
print(message)
```

O apóstrofo aparece entre um conjunto de aspas duplas, portanto o interpretador Python não terá nenhum problema para ler a string corretamente

No entanto, se você usar aspas simples, o interpretador Python não será capaz de identificar em que ponto a string deve terminar:

```py
message = 'One of Python's strengths is its diverse community.'
print(message)
```

Você verá a saída a seguir:

```ps
File "apostrophe.py", line 1
message = 'One of Python's strengths is its diverse community.'
                        ^u
SyntaxError: invalid syntax
```

Na saída, podemos ver que o erro ocorre em **u**, logo depois da segunda aspa simples. Esse erro de sintaxe informa que o interpretador não reconheceu algo como código Python válido.

### FAÇA VOCÊ MESMO

Salve cada um dos exercícios a seguir em um arquivo separado com um nome como *name_cases.py*. Se não souber o que fazer, descase um pouco ou consulte as sugestões que estão no Apêndice C.

[2.3 – Mensagem pessoal](python_work\personal_message.py): Armazene o nome de uma pessoa em uma variável e apresente uma mensagem a essa pessoa. Sua mensagem deve ser simples, como “Alô Eric, você gostaria de aprender um pouco de Python hoje?”.

[2.4 – Letras maiúsculas e minúsculas em nomes](python_work\letters_upperLowerCapitalize.py): Armazene o nome de uma pessoa em uma variável e então apresente o nome dessa pessoa em letras minúsculas, em letras maiúsculas e somente com a primeira letra maiúscula.

[2.5 – Citação famosa](python_work\famous_citation.py): Encontre uma citação de uma pessoa famosa que você admire. Exiba a citação e o nome do autor. Sua saída deverá ter a aparência a seguir, incluindo as aspas:
Albert Einstein certa vez disse: “Uma pessoa que nunca cometeu um erro jamais tentou nada novo.”

[2.6 – Citação famosa 2](python_work\famous_citation2.py): Repita o Exercício 2.5, porém, desta vez, armazene o nome da pessoa famosa em uma variável chamada *famous_person*. Em seguida, componha sua mensagem e armazene-a em uma nova variável chamada message. Exiba sua mensagem.

[2.7 – Removendo caracteres em branco de nomes](python_work\remove_caracter_in_blank.py): Armazene o nome de uma pessoa e inclua alguns caracteres em branco no início e no final do nome.  
> Lembre-se de usar cada combinação de caracteres, **`\t`** e **`\n`**, pelo menos uma vez.  
Exiba o nome uma vez, de modo que os espaços em branco em torno do nome sejam mostrados.  
Em seguida, exiba o nome usando cada uma das três funções de remoção de espaços: **`lstrip()`**, **`rstrip()`** e **`strip()`**.