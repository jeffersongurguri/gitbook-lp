# Lista de Exercícios de JavaScript: Fundamentos de Programação

***

### Seção 1: Variáveis, Tipos de Dados e Operações

* Exercício 1: Boas-vindas Personalizadas
  * Enunciado: Crie um programa que armazene um nome, uma idade e uma cidade em variáveis. Em seguida, exiba uma mensagem de boas-vindas completa, por exemplo: "Olá, \[Nome]! Que legal saber que você tem \[Idade] anos e mora em \[Cidade]!"
  * Dica: Defina os valores das variáveis diretamente no seu código.
  *   Solução:

      JavaScript

      ```javascript
      let nome = "Maria";
      let idade = 17;
      let cidade = "Fortaleza";

      console.log(`Olá, ${nome}! Que legal saber que você tem ${idade} anos e mora em ${cidade}!`);
      ```
* Exercício 2: Calculadora Simples de Média
  * Enunciado: Desenvolva um programa que defina duas notas em variáveis (por exemplo, `nota1` e `nota2`). Calcule a média aritmética dessas notas e exiba o resultado no console com uma mensagem clara, como: "A média das notas é: \[Média]".
  * Exemplo:
    * Entrada (definida no código): Nota 1 = 7.5, Nota 2 = 8.5
    * Saída Esperada: "A média das notas é: 8.0"
  *   Solução:

      JavaScript

      ```javascript
      let nota1 = 7.5;
      let nota2 = 8.5;

      let media = (nota1 + nota2) / 2;

      console.log(`A média das notas é: ${media}`);
      ```
* Exercício 3: Cálculo da Área do Retângulo
  * Enunciado: Faça um programa que defina a largura e a altura de um retângulo em variáveis. Calcule a área total desse retângulo e mostre o resultado no console.
  * Dica: A fórmula da área de um retângulo é `largura * altura`.
  *   Solução:

      JavaScript

      ```javascript
      let largura = 10;
      let altura = 5;

      let area = largura * altura;

      console.log(`A área do retângulo é: ${area}`);
      ```

***

### Seção 2: Estruturas Condicionais (if-else)

* Exercício 1: Verificador de Maioridade
  * Enunciado: Crie um programa que defina uma idade em uma variável. Se a idade for 18 ou mais, exiba a mensagem "Você é maior de idade." Caso contrário, exiba "Você é menor de idade."
  *   Solução:

      JavaScript

      ```javascript
      let idadeUsuario = 19; // Pode testar com outros valores como 15

      if (idadeUsuario >= 18) {
          console.log("Você é maior de idade.");
      } else {
          console.log("Você é menor de idade.");
      }
      ```
* Exercício 2: Classificador de Notas
  * Enunciado: Defina uma nota (de 0 a 10) em uma variável. Com base nessa nota, o programa deve informar a situação do aluno:
    * Se a nota for maior ou igual a 7: "Aprovado"
    * Se a nota for maior ou igual a 5 e menor que 7: "Recuperação"
    * Se a nota for menor que 5: "Reprovado"
  * Exemplo:
    * Entrada (definida no código): 6.0
    * Saída Esperada: "Recuperação"
  *   Solução:

      JavaScript

      ```javascript
      let notaAluno = 6.0; // Pode testar com outros valores como 8.5, 4.0

      if (notaAluno >= 7) {
          console.log("Aprovado");
      } else if (notaAluno >= 5 && notaAluno < 7) {
          console.log("Recuperação");
      } else {
          console.log("Reprovado");
      }
      ```
* Exercício 3: Par ou Ímpar
  * Enunciado: Defina um número inteiro em uma variável. Utilize uma estrutura condicional para verificar se o número é par ou ímpar e exiba o resultado correspondente no console.
  * Dica: Lembre-se de usar o operador de módulo (`%`) para verificar se um número é par (o resto da divisão por 2 é zero).
  *   Solução:

      JavaScript

      ```javascript
      let numero = 7; // Pode testar com outros valores como 10, 0

      if (numero % 2 === 0) {
          console.log("O número é par.");
      } else {
          console.log("O número é ímpar.");
      }
      ```

***

### Seção 3: Estruturas de Repetição (for, while)

* Exercício 1: Contagem Progressiva
  * Enunciado: Usando a estrutura de repetição `for`, crie um programa que exiba no console os números de 1 a 10, um por linha.
  *   Solução:

      JavaScript

      ```javascript
      for (let i = 1; i <= 10; i++) {
          console.log(i);
      }
      ```
* Exercício 2: Tabuada Dinâmica
  * Enunciado: Defina um número (de 1 a 10) em uma variável. Usando um laço `for`, o programa deve exibir a tabuada completa desse número (multiplicando de 1 a 10) no console.
  * Exemplo:
    * Entrada (definida no código): 5
    *   Saída Esperada:

        ```
        5 x 1 = 5
        5 x 2 = 10
        ...
        5 x 10 = 50
        ```
  *   Solução:

      JavaScript

      ```javascript
      let numeroTabuada = 5; // Pode testar com outros valores como 7, 3

      console.log(`Tabuada do ${numeroTabuada}:`);
      for (let i = 1; i <= 10; i++) {
          console.log(`${numeroTabuada} x ${i} = ${numeroTabuada * i}`);
      }
      ```
* Exercício 3: Somador de Números (Loop com condição de parada)
  * Enunciado: Crie um programa que, usando a estrutura `while`, simule a soma de uma sequência de números. Defina uma lista de números em um array e some-os até encontrar o número 0 (que serve como condição de parada). No final, exiba o total da soma no console.
  * Dica: Você vai precisar de uma variável para acumular a soma e uma condição no `while` que verifique se o número atual do array é diferente de zero.
  *   Solução:

      JavaScript

      ```javascript
      let numerosParaSomar = [10, 5, 12, 0, 7, 3]; // O 0 indica o fim da soma
      let soma = 0;
      let i = 0;

      // Enquanto o número atual não for 0 e ainda houver números no array
      while (i < numerosParaSomar.length && numerosParaSomar[i] !== 0) {
          soma += numerosParaSomar[i];
          i++;
      }

      console.log(`A soma total dos números é: ${soma}`);
      ```

***

### Seção 4: Utilização de Arrays (Vetores)

* Exercício 1: Minha Lista de Compras
  * Enunciado: Crie um array chamado `listaDeCompras` com 5 itens de supermercado da sua preferência (ex: "Arroz", "Feijão", etc.). Em seguida, use um loop (`for` ou `for...of`) para exibir cada item da lista no console.
  *   Solução:

      JavaScript

      ```javascript
      let listaDeCompras = ["Arroz", "Feijão", "Macarrão", "Café", "Açúcar"];

      console.log("Minha Lista de Compras:");
      for (let i = 0; i < listaDeCompras.length; i++) {
          console.log(`- ${listaDeCompras[i]}`);
      }
      /*
      // Alternativa usando for...of
      for (let item of listaDeCompras) {
          console.log(`- ${item}`);
      }
      */
      ```
* Exercício 2: Média das Notas da Turma
  * Enunciado: Crie um array chamado `notas` com 4 notas de alunos. Calcule a média dessas notas e exiba o resultado no console.
  * Dica: Você pode usar um loop para somar todos os elementos do array e depois dividir pelo número total de elementos.
  *   Solução:

      JavaScript

      ```javascript
      let notas = [7.5, 8.0, 6.5, 9.0];
      let somaNotas = 0;

      for (let i = 0; i < notas.length; i++) {
          somaNotas += notas[i];
      }

      let mediaNotas = somaNotas / notas.length;
      console.log(`A média das notas da turma é: ${mediaNotas.toFixed(2)}`); // toFixed(2) para 2 casas decimais
      ```
* Exercício 3: Encontrando o Maior Número
  * Enunciado: Dado o seguinte array de números: `[15, 8, 90, 23, 5, 77]`. Crie um programa que encontre e exiba o maior valor presente nesse array no console.
  * Dica: Você pode inicializar uma variável com o primeiro elemento do array e depois percorrer o restante, comparando e atualizando o maior valor encontrado.
  *   Solução:

      JavaScript

      ```javascript
      let numeros = [15, 8, 90, 23, 5, 77];
      let maiorNumero = numeros[0]; // Assume que o primeiro é o maior inicialmente

      for (let i = 1; i < numeros.length; i++) {
          if (numeros[i] > maiorNumero) {
              maiorNumero = numeros[i];
          }
      }

      console.log(`O maior número no array é: ${maiorNumero}`);
      ```
