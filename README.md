# JavaScript Basico 

Primeiro iremos instalar o <a href="https://nodejs.org/en/" target="_BLANK">`NodeJS`</a> para podermos testar nossas aplicações diretamente da linha de comando.

Feito isso, vamos testar se tudo ocorreu da forma certa, abra o `terminal` e digite

```
  $ node -v 
  // O resultado deve ser algo assim "v8.6.0"
```

Se o seu resultado for similar, siginifca que já podemos iniciar os estudos, agora digite o seguinte comando para poder acessar o terminal do `node`

```
   $ node
   > 
```

Agora que estamos dentro do terminal do `node`, vamos começar com declarações de variaveis.

# Var
Em JavaScript, toda variavel que é declarada com a palavra-chave `var` é "elevada" (hosting) até o topo do contexto de execução. Exemplo:

```
  // Declaramos a variavel
  var nome = "Rafael Augusto"
  console.log(nome)
  
  function newFunction(){
    nome = "Rafael Torres"
    console.log(nome)
  }
  
  newFunction()
  
  console.log(nome)
```

# Let
A partir do JavaScript 6, além de podermos utilizar a palavra-chave `var` na declaração de variaveis, tambem podemos utilizar a palavra-chave `let`. A diferença entre elas é que quando utilizamos `let`, estamos atribuindo escopo de bloco à variavel sendo craido e, portanto, não ocorre o hoisting.

```
  // Declaramos a variavel
  let nome = "Rafael Augusto"
  console.log(nome)
  
  function newFunction(){
    let nome = "Rafael Torres"
    console.log(nome)
  }
  
  newFunction()
  
  console.log(nome)
```

# Const
Podemos declarar uma variavel como constante atraves da palavra-chave `const`. Mas o que é uma constante? Uma vez que tenha sido atribuido um valor à uma variavel que tenha sido declarada usando a palavra-chave `const`, seu valor não pode ser alterado. Por esta razão, todas as constantes devem obrigatoriamente ser inicializadas na declação.

```
  const nome = "Rafael Augusto"
  console.log(nome)
  
  nome = "Rafael Torres"
  // "TypeError: Assignment to constant variable.
```

Agora que iniciamos da maneira correta, vamos entender alguns processos.

# Funções

Em JavaScript, quando envolvemos uma palavra com citações, ela é chamada de uma string , e quando terminamos com uma linha de código, terminamos com um ponto-e-vírgula (opicional).

O JavaScript também possui recursos internos, chamados de funções. Para chamar uma função, simplesmente escrevemos seu nome (desta vez sem aspas) e terminamos com um conjunto de parênteses. Tente chamar a `alert` função como você vê a baixo.

```
  alert()
```

# String Function Parameter

Você provavelmente teve o resultado de uma caixa com um valor `undefined`, porem isso não é nada de mais né? Agora vamos passar um parametro para nossa função.

```
  alert("Rafael Augusto")
```

<img src="http://sobresagas.com/wp-content/uploads/2016/07/uau.gif">

# Combining Strings

O JavaScript não só pode combinar números - ele também pode combinar Strings

Crie um alert que combine seu nome e uma string, como abaixo:

```
  alert(nome + " é impressionante ;)")
```

Agora, sem mais delongas, vamos iniciar um projeto bem basico, o primeiro projeto será uma lista de tarefas, que ao adicionarmos, o item irá aparecer automaticamente na lista, e tambem iremos poder excluir.
Estou levando em consideração, que já saiba (PELO MENOS O BASICO, SE NÃO, SAIA DAQUI) de `HTML` e `CSS`. Não irei explicar nenhuma estrutura de `HTML` ou `CSS`, o curso é de `JS`.

Vamos começar criando um arquivo chamado `index.html`, com a seguinte estrutura.

**index.html**

```
  <!DOCTYPE html>
  <html>
    <head>
      <meta charset="utf-8">
      <title>Lista de Tarefas com JS</title>
    </head>
    
    <body>
      
    </body>
  </html>
  
```

E em seguida, criaremos nossa `list` com alguns produtos que já estarão disponiveis de inicio

```
  <ul id="list">
    <li>iPhone</li>
    <li>iPad</li>
    <li>iPod</li>
    <li>iMac</li>
  </ul>
```

Para ficar mais legal visualmente, vamos dar uma estilizada

```
#list{
  margin: 0;
  padding: 0;
}

#list li{
  list-style: none;
  padding: 10px;
  background: #FFF;
  margin-top: 5px;
}
```
O resultado será esse: 

<img src="https://i.imgur.com/SrxT8am.png">
