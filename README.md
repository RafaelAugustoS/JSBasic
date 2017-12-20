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



