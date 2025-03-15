# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro ✔

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

A alternativa correta é a A), pois as variaveis foram colocadas no lugar errado, e então a var dá undefined porque ... e a let da erro pois ...

**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0) ✔

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

A resposta correta é a B), pois antes o codigo tava lendo que se em um dos numeros da soma fosse 0 daria erro, mas o certo seria ele fala isso do resultado, então trocando para o codigo da alternativa b) ele faz o certo lendo o resultado que não pode dá 0.
______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.✔

c) O código imprime 50.

d) O código gera um erro.

A alternativo correta é a B), pois a falta do break no case "eletrônico" faz a execução passar direto por ele e ir para case "vestuário".
______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24✔

A alternativa correta é a D), pois no primeiro passo ele dobra todos os numeros da array, deois ele filtra os numeros maiores que 5 e depos ele soma os valores maoiores que 5.
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]✔

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

A resposta correta é a C), pois no codigo ele fala para colocar essas duas frutas nos lugares 1 e 2, e como já tem frutas lá ele coloca no lugar delas.
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.✔

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.✔

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

A alternativa correta é a A), porque e afirmativa III não está correta, JavaScript suporta herança de classe.
______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.✔

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
Código corrigido:
```javascript
function somaArray(numeros) {
  let soma = 0;
  for (let i = 0; i < numeros.length; i++) {  //fazendo o codigo ler a array começando por 
  // 0 que é o 1, deppis falando que ele vai usar apenas e todos os numeros que estão 
  // na array e por ultimo fala que ele vai someando mais um a variavel pra ir somando 
  // os outros numeros da array.
    soma += 2 * numeros[i]; // aqui é onde ocorre a soma e a multiplicação dos valores.
  }
  return soma;
}
console.log(somaArray([1, 2, 3, 4])); // e aqui é onde fala pra imprimar a resposta.
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Meu código:
```javascript
class Produto { //criando a classe produto
  constructor(nome, preco) {
    this.nome = nome; //crindo as propriedades da classe produto
    this.preco = preco;
  }

  calcularDesconto() { // crinado função para calcular o preço 
    let desconto = this.preco * 0.10; //calculando os 105 do preço
    let precoComDesconto = this.preco - desconto; //subtraindo os 10% do preço original
    return precoComDesconto;
  }
}

class Livro extends Produto { //criando uma outra classe que herda as propriedades da classe produto
  constructor(nome, preco) {
    super(nome, preco); //chamando as propriedades herdadas
  }
  calcularDesconto() {  // crinado função para calcular o preço 
    const desconto = this.preco * 0.20; //calculando os 105 do preço
    const precoComDesconto = this.preco - desconto; //subtraindo os 10% do preço original
    return precoComDesconto;
  }
}

let produto = new Produto ("faca", 40); //crinado um produto na classe produto
let livro = new Livro ("your name", 65);  //criando um livro na classe livro
//imprimindo o nome, o preço e preço com desconte dos novos produtos
console.log(`produto: ${produto.nome}, valor original: ${produto.preco}, mas você ganhou 10% de desconto, que fica: ${produto.calcularDesconto()}`);
console.log(`produto: ${livro.nome}, valor original: ${livro.preco}, mas você ganhou 20% de desconto, que fica: ${livro.calcularDesconto()}`);
```
