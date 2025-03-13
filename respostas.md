QUESTÃO 1 - 
A alternativa correta é "a", pois uma variável var é global, porém, como o console.log foi escrito antes de ser atribuido um valor a ele, a resposta não é definida. Já no segundo console.log, a variável let ainda não existe, por isso, a resposta da erro.

QUESTÃO 2 - 
A alternativa correta é "b", pois a respota "Erro: número inválido" só deve ser exibida quando a soma não existir, ou seja, quando ambos os valores forem igual a 0. Nessa lógica a expressão está errada pois a condição correta não é "ou(||)", e sim "e(&&)", além disso, é necessário deixar claro a lógica para os dois termos, sendo necessário especificá-la em ambos.

QUESTÃO 3 - 
A alternativa correta é "b", pois dentro da função condicional "switch" há vários casos, cada um com um produto com preço diferente. O preço é uma variável let e tem sua alteração dentro da função, assim, para separar os valores em cada caso, o código utiliza o comando "break", porém, esse comando não se encontra após o preço dos produtos eletrônicos. Por conta disso, o sistema imprime o próximo valor da let preço, que é 200.

QUESTÃO 4 - 
A alternstiva correta é "d", pois o console.log imprime a variável let resultado, que é encontrada após diversas operações matemáticas com os valores da array let números. Após definidos os valores da array numeros, a let resultado faz as seguintes operações: numeros.map, que multilpica os todos os valores por 2; após isso, há o .filter, que filtra os valores acima de 5, mantendo apenas os números 6, 8, e 10 na array; por último, a expressão .reduce define uma sequência de iterações que soma os valores restantes, o que gera o valor final da let: 24.

QUESTÃO 5 - 
A alternativa correta é "c", pois o termo lista.splice edita a lista feita, alterando os termos 1 e 2, por abacaxi e manga, respectivamente, com isso, o console.log imprime o novo valor da lista.

QUESTÃO 6 - 
A alternativa correta é "a", pois a herança em JavaScript é usada para compartilhar métodos e propriedades entre classes, de maneira que uma classe "herde" métodos de outra. Isso evita a repetição de código e permite a reutilização das funcionalidades de uma classe base. Além disso, A herança é implementada através da palavra-chave extends. Quando uma classe utiliza extends, ela herda propriedades e métodos da classe base. 

QUESTÃO 7 - 
A alternativa correta é "a", pois a classe "funcionario" herda os atributos de "pessoa" diretamente, desde que esses atributos tenham sido inicializados pelo construtor da classe "pessoa". Além disso, o método "apresentar" da classe "funcionario" sobrepõe o método "apresentar" da classe "pessoa", o que significa que ele substitui o comportamento do método da classe pai. Contudo, antes de executar a lógica específica da classe filha, ele chama o método da classe pai utilizando "super.apresentar()", o que permite que a parte do código de "pessoa" seja executada, antes de adicionar a funcionalidade própria de "funcionario".

QUESTÃO 8 - 
A alternativa correta é "b", pois, de fato, o polimorfismo funciona assim. Basicamente esse resultado é obtido através da sobrescrita de métodos, onde métodos com o mesmo nome em classes diferentes podem ter implementações diferentes. Porém, o JavaScript não suporta a sobreposição de métodos, já que, ao tentar realizar essa sobreposição, o último método substitui os anteriores.

QUESTÃO 9 - 
``` JavaScript
function somaArray(numeros) {
        var soma = 0; // Cria a variável "soma" para poder realizar a operação desejada e atibui a ela o valor 0
        for (i = 0; i < numeros.length; i++) { // Altera a expressão ".size" para ".length", pois o primeiro não existe
            soma += 2*numeros[i]; // Adiciona a soma na operação, permitindo que o valor de soma seja o resultado da soma dos termos, e não o último valor
        }
        return soma;
    }
    console.log(somaArray([1, 2, 3, 4]));
```

QUESTÃ0 10 - 
``` JavaScript
class Produto { 
    constructor(nome, preco) {
        this.nome = nome;
        this.preco = preco;
    }
    calcularDesconto() {
        let desconto = this.preco / 10;
        console.log("O", this.nome, "custa R$", this.preco, "porém, tem um desconto de R$", desconto);
    }
}
    
const produto = new Produto("pizza", 40);
produto.calcularDesconto(); // Chama o método na instância "produto"
```

Aqui é criada a classe "produto" e seus atributos, nome e preço. Com isso, há o método "calcularDesconto", que define uma variável let "desconto", calcula o desconto do produto e imprime a resposta no console.log. Por fim, é criada a instância "produto", no caso, a pizza, e é chamado o método "calcularDesconto" para obter a resposta esperada. 

``` JavaScript
class Livro extends Produto {
        constructor(nome, preco) {
            super(nome, preco);
        }
        calcularDesconto() {
            let desconto = this.preco / 20;
            console.log("O livro", this.nome, "custa R$", this.preco, "porém, tem um desconto de R$", desconto);
        }
}
const produto = new Livro("Harry Potter", 80);
produto.calcularDesconto(); 
```
Nessa parte, é criada a classe "Livro" que herda a classe "Produto", carregando seus atributos por meio de "super" e alterando apenas a funcionalidade do método "calcularDesconto()". Após isso, é criado o novo produto (const produto) chamando a classe filha "Livro", e adicionadas as informações desse produto específico, no caso, o nome: Harry Potter; e o preço: 80. Assim, ao chamar o método "calcularDesconto()", é realizado o calculo com base nas informações fornecidas, e a resposta é imprimida no console.log.
