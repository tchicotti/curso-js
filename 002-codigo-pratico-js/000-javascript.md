# Javascript

## Tipos de Dados em JavaScript: Um Guia Completo

JavaScript possui diversos tipos de dados que servem para representar diferentes tipos de informações. A compreensão desses tipos é fundamental para escrever código JavaScript eficiente e correto. Vamos explorar cada um deles com exemplos detalhados:

### Tipos de Dados Primitivos

-   **Number:** Representa números tanto inteiros quanto decimais.
    -   **Exemplos:**
        ```JavaScript 
        let idade = 30; // Número inteiro
        let altura = 1.75; // Número decimal
        const pi = 3.14159; // Constante matemática
        ```
-   **String:** Representa sequências de caracteres, ou seja, texto.
    -   **Exemplos:**
        ```JavaScript
        let nome = "João da Silva";
        let mensagem = "Olá, mundo!";
        let fraseComAspasSimples = 'Isso também é uma string';
        ```
-   **Boolean:** Representa valores lógicos, podendo ser `true` ou `false`.
    -   **Exemplos:**
        ```JavaScript
        let estaChovendo = true;
        let eMaiorDeIdade = false;
        let resultado = 5 > 3; // Resulta em `true`
        ```
-   **Null:** Representa a ausência intencional de um valor.
    -   **Exemplos:**
        ```JavaScript
        let valorIndefinido = null;
        ```
-   **Undefined:** Representa uma variável que foi declarada, mas ainda não foi atribuído nenhum valor.
    -   **Exemplos:**
        ```JavaScript
        let variavelNaoInicializada; // O valor inicial é `undefined`
        ```
-   **Symbol:** Representa um valor único e imutável, frequentemente usado como chave de objeto.
    -   **Exemplos:**
        ```JavaScript
        let id = Symbol("meuId");
        let objeto = { [id]: "valor" };
        ```

### Tipos de Dados Complexos

-   **Object:** Representa uma coleção não ordenada de pares chave-valor.
    -   **Exemplos:**
        ```JavaScript
        let pessoa = { nome: "Maria", idade: 25, cidade: "São Paulo" };
        let carro = { marca: "Fiat", modelo: "Uno", ano: 2010 };
        let array = [1, 2, 3, "quatro"]; // Arrays são um tipo especial de objeto
        ```

### Trabalhando com os Tipos de Dados

**Conversão de Tipos:**

-   **Conversão Explícita:**
    ```JavaScript
    let numero = "10";
    let numeroConvertido = Number(numero); // Converte para número
    ```
-   **Conversão Implícita:**
    ```JavaScript
    let soma = "5" + 2; // Resulta em "52" (concatenação)
    let outraSoma = "5" - 2; // Resulta em 3 (conversão implícita para número)
    ```

**Verificando o Tipo de Dado:**
```JavaScript
typeof valor; // Retorna o tipo de dado como uma string
console.log(typeof 10); // "number"`
console.log(typeof "Olá"); // "string"`
```

**Observações Importantes:**

-   **Tipagem Dinâmica:** JavaScript é uma linguagem de tipagem dinâmica, o que significa que o tipo de uma variável pode mudar durante a execução do código.
-   **Imutáveis vs. Mutáveis:** Os tipos primitivos são imutáveis, ou seja, seu valor não pode ser alterado após a criação. Já os objetos são mutáveis, podendo ter suas propriedades modificadas.
-   **NaN:** Representa "Not a Number" e é o resultado de operações matemáticas inválidas, como dividir um número por zero.

**Exemplo Completo:**



``` JavaScript
let nome = "Ana"; // String
let idade = 30; // Number
let estaAprovado = true; // Boolean
let carro = { marca: "Honda", modelo: "Civic" }; // Object

console.log("Olá, " + nome + "! Você tem " + idade + " anos.");
console.log("Está aprovado? " + estaAprovado);
console.log("Seu carro é um " + carro.marca + " " + carro.modelo);
// ou 
console.log(`Seu carro é um ${carro.marca} ${carro.modelo}`);
// Convertendo para string
let idadeComoString = idade.toString();
console.log(typeof idadeComoString); // "string"

```

---
## Trabalhando com Arrays e Objetos em JavaScript

### Arrays

**O que são Arrays?**

Arrays em JavaScript são como listas ordenadas de valores. Cada valor (ou elemento) em um array possui um índice numérico, começando em 0. Arrays são extremamente úteis para armazenar coleções de dados relacionados.

**Criando um Array:**

```javascript
let frutas = ["maçã", "banana", "laranja"];
```

**Acessando elementos:**

```javascript
console.log(frutas[0]); // Imprime: maçã
```

**Modificando elementos:**

```javascript
frutas[1] = "pera";
```

**Adicionando elementos:**

* **No final:**
  ```javascript
  frutas.push("uva");
  ```
* **No início:**
  ```javascript
  frutas.unshift("melão");
  ```

**Removendo elementos:**

* **Último elemento:**
  ```javascript
  frutas.pop();
  ```
* **Primeiro elemento:**
  ```javascript
  frutas.shift();
  ```

**Métodos importantes:**

* **forEach:** Itera sobre cada elemento do array.
* **map:** Cria um novo array aplicando uma função a cada elemento.
* **filter:** Cria um novo array com os elementos que passam em um teste.
* **reduce:** Reduz um array a um único valor.
* **find:** Retorna o primeiro elemento que satisfaz uma condição.
* **indexOf:** Retorna o índice do primeiro elemento que corresponde a um valor.

**Exemplo:**

```javascript
const numeros = [1, 2, 3, 4, 5];

// Dobrar cada número
const numerosDobrados = numeros.map(numero => numero * 2);

// Filtrar números pares
const numerosPares = numeros.filter(numero => numero % 2 === 0);

// Somar todos os números
const soma = numeros.reduce((total, numero) => total + numero, 0);
```

### Objetos

**O que são Objetos?**

Objetos em JavaScript são coleções não ordenadas de pares chave-valor. Cada chave é uma string única e o valor associado pode ser de qualquer tipo de dado, incluindo outros objetos.

**Criando um Objeto:**

```javascript
let pessoa = {
  nome: "João",
  idade: 30,
  cidade: "São Paulo"
};
```

**Acessando propriedades:**

```javascript
console.log(pessoa.nome); // Imprime: João
```

**Modificando propriedades:**

```javascript
pessoa.idade = 31;
```

**Adicionando propriedades:**

```javascript
pessoa.profissao = "Programador";
```

**Removendo propriedades:**

```javascript
delete pessoa.cidade;
```

**Métodos:**

Objetos podem ter métodos, que são funções associadas a eles.

```javascript
let carro = {
  marca: "Fiat",
  modelo: "Uno",
  ligar: function() {
    console.log("Ligando o carro...");
  }
};
```

**Exemplo:**

```javascript
let livro = {
  titulo: "O Senhor dos Anéis",
  autor: "J.R.R. Tolkien",
  ano: 1954,
  paginas: 1178,
  ler: function() {
    console.log("Estou lendo " + this.titulo);
  }
};
```

### Diferenças entre Arrays e Objetos

| Característica | Arrays | Objetos |
|---|---|---|
| Ordem | Ordenados por índice numérico | Não ordenados, acessados por chave |
| Chaves | Índices numéricos (0, 1, 2, ...) | Strings únicas |
| Uso | Armazenar coleções de dados semelhantes | Modelar entidades com propriedades e métodos |

**Quando usar Arrays e Objetos:**

* **Arrays:** Para armazenar listas de dados do mesmo tipo.
* **Objetos:** Para representar entidades com propriedades e comportamentos distintos.

**Exemplo prático:**

```javascript
let produtos = [
  { nome: "Banana", preco: 3.99 },
  { nome: "Maçã", preco: 2.99 },
  { nome: "Laranja", preco: 1.99 }
];
```

Neste exemplo, `produtos` é um array de objetos. Cada objeto representa um produto com suas propriedades (nome e preço).

**Observações:**

* **JSON:** É um formato de texto para armazenar dados estruturados, baseado em objetos JavaScript.
* **Herança:** Objetos em JavaScript podem herdar propriedades e métodos de outros objetos.
* **Prototipos:** JavaScript utiliza prototipagem para criar objetos a partir de outros objetos.

--- 

## If e Else em JavaScript: Controlando o Fluxo do Seu Código

As estruturas condicionais `if` e `else` são fundamentais em JavaScript para tomar decisões e executar diferentes blocos de código com base em determinadas condições. Elas permitem que seu programa siga diferentes caminhos dependendo dos valores das variáveis ou do resultado de expressões.

### Como funciona o if

* **Condição:** O `if` sempre começa com uma condição dentro de parênteses. Essa condição é uma expressão que resulta em um valor booleano (verdadeiro ou falso).
* **Bloco de código:** Se a condição for verdadeira, o código dentro das chaves `{}` após o `if` será executado.

**Exemplo:**

```javascript
let idade = 18;

if (idade >= 18) {
  console.log("Você é maior de idade.");
}
```

### Como funciona o else

* **Condição alternativa:** O `else` é usado em conjunto com o `if` para executar um bloco de código caso a condição do `if` seja falsa.

**Exemplo:**

```javascript
let idade = 17;

if (idade >= 18) {
  console.log("Você é maior de idade.");
} else {
  console.log("Você é menor de idade.");
}
```

### If...else if...else

* **Múltiplas condições:** Quando você precisa verificar várias condições, pode usar `else if` para criar mais ramificações.

**Exemplo:**

```javascript
let nota = 7;

if (nota >= 9) {
  console.log("Parabéns, você tirou A!");
} else if (nota >= 7) {
  console.log("Você tirou B.");
} else if (nota >= 5) {
  console.log("Você tirou C.");
} else {
  console.log("Você precisa estudar mais.");
}
```

### Operadores de comparação

Para criar condições em seus `if`, você utilizará os operadores de comparação:

* **Igualdade:** `==` (igualdade fraca), `===` (igualdade estrita)
* **Desigualdade:** `!=` (desigualdade fraca), `!==` (desigualdade estrita)
* **Maior que:** `>`
* **Menor que:** `<`
* **Maior ou igual:** `>=`
* **Menor ou igual:** `<=`

### Operadores lógicos

Para combinar várias condições, você pode usar os operadores lógicos:

* **E:** `&&` (ambas as condições devem ser verdadeiras)
* **Ou:** `||` (pelo menos uma das condições deve ser verdadeira)
* **Negação:** `!` (inverte o valor booleano)

**Exemplo:**

```javascript
let temCarteiraDeMotorista = true;
let idadeMinima = 18;

if (temCarteiraDeMotorista && idade >= idadeMinima) {
  console.log("Você pode dirigir.");
}
```

### Exemplos práticos

* **Verificar se um número é par:**

```javascript
let numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par.");
} else {
  console.log("O número é ímpar.");
}
```

* **Validar um formulário:**

```javascript
let nome = "João";
let email = "joao@email.com";
let senha = "123";

if (nome !== "" && email.includes("@") && senha.length >= 8) {
  console.log("Formulário válido!");
} else {
  console.log("Por favor, preencha todos os campos corretamente.");
}
```

**Em resumo:**

As estruturas `if` e `else` são essenciais para criar programas que tomam decisões com base em diferentes condições. Ao entender como utilizá-las em conjunto com operadores de comparação e lógicos, você poderá criar programas mais complexos e dinâmicos.

---

## Laços de Repetição em JavaScript: Automatizando Tarefas Repetitivas

Laços de repetição, ou *loops* em inglês, são estruturas de controle que permitem executar um bloco de código repetidamente enquanto uma determinada condição for verdadeira. Eles são essenciais para automatizar tarefas repetitivas e iterar sobre conjuntos de dados.

### Tipos de Laços em JavaScript

**1. Laço `for`:**

* **Sintaxe:**
  ```javascript
  for (inicialização; condição; incremento) {
      // Código a ser executado repetidamente
  }
  ```
* **Explicação:**
  * **Inicialização:** Uma expressão executada apenas uma vez no início do laço, geralmente para declarar e inicializar um contador.
  * **Condição:** Uma expressão que é verificada antes de cada iteração. Se a condição for verdadeira, o bloco de código é executado.
  * **Incremento:** Uma expressão executada após cada iteração, geralmente para atualizar o contador.

* **Exemplo:**
  ```javascript
  for (let i = 0; i < 5; i++) {
      console.log(i);
  }
  ```
  Este código irá imprimir os números de 0 a 4 no console.

**2. Laço `while`:**

* **Sintaxe:**
  ```javascript
  while (condição) {
      // Código a ser executado enquanto a condição for verdadeira
  }
  ```
* **Explicação:**
  * **Condição:** A condição é verificada no início de cada iteração. Se a condição for verdadeira, o bloco de código é executado.

* **Exemplo:**
  ```javascript
  let i = 0;
  while (i < 5) {
      console.log(i);
      i++;
  }
  ```
  Este código é equivalente ao exemplo anterior do `for`.

**3. Laço `do...while`:**

* **Sintaxe:**
  ```javascript
  do {
      // Código a ser executado pelo menos uma vez
  } while (condição);
  ```
* **Explicação:**
  * O bloco de código é executado pelo menos uma vez, e a condição é verificada após a primeira execução. Se a condição for verdadeira, o laço continua.

* **Exemplo:**
  ```javascript
  let i = 0;
  do {
      console.log(i);
      i++;
  } while (i < 5);
  ```
  Este código também é equivalente aos exemplos anteriores.

### Quando usar cada tipo de laço?

* **`for`:** Ideal quando você sabe o número exato de iterações.
* **`while`:** Ideal quando você precisa repetir um bloco de código enquanto uma determinada condição for verdadeira, sem saber o número exato de iterações.
* **`do...while`:** Ideal quando você precisa garantir que o bloco de código seja executado pelo menos uma vez, mesmo que a condição inicial seja falsa.

### Exemplo prático: Iterando sobre um array

```javascript
const frutas = ["maçã", "banana", "laranja"];

for (let i = 0; i < frutas.length; i++) {
    console.log(frutas[i]);
}
```

### Outros recursos

* **`break`:** Interrompe o laço imediatamente.
* **`continue`:** Pula para a próxima iteração do laço.
* **`for...in`:** Itera sobre as propriedades enumeráveis de um objeto.
* **`for...of`:** Itera sobre os valores de um objeto iterável (como arrays).

**Observações:**

* **Cuidado com loops infinitos:** Se a condição de um laço nunca se tornar falsa, o programa entrará em um loop infinito.
* **Otimização:** Em alguns casos, é possível otimizar o código utilizando métodos como `map`, `filter` e `reduce` para trabalhar com arrays, em vez de usar laços tradicionais.

### Exemplos de uso do `break` e `continue`

**Exemplo 1: Encontrar o primeiro número par em um array**

```javascript
const numeros = [1, 3, 5, 2, 8, 10];

for (let i = 0; i < numeros.length; i++) {
  if (numeros[i] % 2 === 0) {
    console.log("O primeiro número par é:", numeros[i]);
    break;
  }
}
```


**Exemplo 2: Encontrar um valor específico em um objeto**


```javascript
const pessoa = {
  nome: 'João da Silva',
  idade: 30,
  cidade: 'São Paulo'
};

for (const propriedade in pessoa) {
  if (propriedade === 'idade') {
    console.log("A idade é:", pessoa[propriedade]);
    break;
  }
}
```

**Exemplo 3: Imprimir apenas os números ímpares**

```javascript
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    continue; // Pula para a próxima iteração se o número for par
  }
  console.log(i);
}
```



**Exemplo 4: Somar apenas os números positivos**


```javascript
const numeros = [1, -2, 3, -4, 5];
let soma = 0;

for (let indice = 0; indice < numeros.length; indice++) {
  if (numeros[indice] < 0) {
    continue; // Pula para a próxima iteração se o número for negativo
  }
  soma += numeros[indice];
}
console.log("A soma dos números positivos é:", soma);
```

**Outros exemplos:**

* **Verificar se um aluno foi aprovado em uma disciplina:**
  ```javascript
  const notaFinal = 7;
  const notaAprovacao = 6;

  if (notaFinal >= notaAprovacao) {
    console.log("Aprovado!");
  } else {
    console.log("Reprovado!");
  }
  ```
* **Calcular o valor total de uma compra:**
  ```javascript
  const produtos = [
    { nome: "Banana", preco: 3.99 },
    { nome: "Maçã", preco: 2.99 }
  ];
  let valorTotal = 0;

  for (let i = 0; i < produtos.length; i++) {
    valorTotal += produtos[i].preco;
  }
  console.log("O valor total da compra é:", valorTotal);
  ```
