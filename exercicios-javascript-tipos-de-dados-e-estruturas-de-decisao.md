# Exercícios JavaScript - Tipos de Dados e Estruturas de Decisão

## Exercícios JavaScript - Tipos de Dados e Estruturas de Decisão

### 🟢 TRIVIAL

#### 1. Verificar se um número é positivo

Crie uma função que receba um número e retorne "positivo" se for maior que 0, "negativo" se for menor que 0, ou "zero" se for igual a 0.

```javascript
function verificarNumero(numero) {
    if (numero > 0) {
        return "positivo";
    } else if (numero < 0) {
        return "negativo";
    } else {
        return "zero";
    }
}

// Teste
console.log(verificarNumero(5));   // "positivo"
console.log(verificarNumero(-3));  // "negativo"
console.log(verificarNumero(0));   // "zero"
```

#### 2. Verificar tipo de dado

Escreva uma função que receba uma variável e retorne seu tipo usando `typeof`.

```javascript
function verificarTipo(valor) {
    return typeof valor;
}

// Teste
console.log(verificarTipo(42));        // "number"
console.log(verificarTipo("texto"));   // "string"
console.log(verificarTipo(true));      // "boolean"
console.log(verificarTipo({}));        // "object"
console.log(verificarTipo([]));        // "object"
console.log(verificarTipo(null));      // "object"
console.log(verificarTipo(undefined)); // "undefined"
```

#### 3. Par ou ímpar

Crie uma função que determine se um número é par ou ímpar.

```javascript
function parOuImpar(numero) {
    if (numero % 2 === 0) {
        return "par";
    } else {
        return "ímpar";
    }
}

// Versão mais concisa usando operador ternário
function parOuImparTernario(numero) {
    return numero % 2 === 0 ? "par" : "ímpar";
}

// Teste
console.log(parOuImpar(4));   // "par"
console.log(parOuImpar(7));   // "ímpar"
console.log(parOuImpar(0));   // "par"
```

#### 4. Maior de dois números

Faça uma função que receba dois números e retorne o maior deles.

```javascript
function maiorNumero(a, b) {
    if (a > b) {
        return a;
    } else {
        return b;
    }
}

// Versão mais concisa
function maiorNumeroTernario(a, b) {
    return a > b ? a : b;
}

// Usando Math.max
function maiorNumeroMath(a, b) {
    return Math.max(a, b);
}

// Teste
console.log(maiorNumero(10, 5));   // 10
console.log(maiorNumero(3, 8));    // 8
console.log(maiorNumero(7, 7));    // 7
```

#### 5. Verificar se é string vazia

Crie uma função que verifique se uma string está vazia ou não.

```javascript
function stringVazia(str) {
    if (str === "") {
        return true;
    } else {
        return false;
    }
}

// Versão mais concisa
function stringVaziaConcisa(str) {
    return str === "";
}

// Considerando também espaços em branco
function stringVaziaOuSoEspacos(str) {
    return str.trim() === "";
}

// Teste
console.log(stringVazia(""));          // true
console.log(stringVazia("texto"));     // false
console.log(stringVazia("   "));       // false
console.log(stringVaziaOuSoEspacos("   ")); // true
```

### 🔵 BÁSICO

#### 6. Calculadora simples

Desenvolva uma calculadora que receba dois números e uma operação (+, -, \*, /) e retorne o resultado.

```javascript
function calculadora(num1, num2, operacao) {
    switch (operacao) {
        case "+":
            return num1 + num2;
        case "-":
            return num1 - num2;
        case "*":
            return num1 * num2;
        case "/":
            if (num2 === 0) {
                return "Erro: Divisão por zero";
            }
            return num1 / num2;
        default:
            return "Operação inválida";
    }
}

// Teste
console.log(calculadora(10, 5, "+"));  // 15
console.log(calculadora(10, 5, "-"));  // 5
console.log(calculadora(10, 5, "*"));  // 50
console.log(calculadora(10, 5, "/"));  // 2
console.log(calculadora(10, 0, "/"));  // "Erro: Divisão por zero"
console.log(calculadora(10, 5, "%"));  // "Operação inválida"
```

#### 7. Classificação de idade

Crie uma função que classifique a idade: criança (0-12), adolescente (13-17), adulto (18-59), idoso (60+).

```javascript
function classificarIdade(idade) {
    if (idade >= 0 && idade <= 12) {
        return "criança";
    } else if (idade >= 13 && idade <= 17) {
        return "adolescente";
    } else if (idade >= 18 && idade <= 59) {
        return "adulto";
    } else if (idade >= 60) {
        return "idoso";
    } else {
        return "idade inválida";
    }
}

// Teste
console.log(classificarIdade(8));   // "criança"
console.log(classificarIdade(15));  // "adolescente"
console.log(classificarIdade(25));  // "adulto"
console.log(classificarIdade(70));  // "idoso"
console.log(classificarIdade(-5));  // "idade inválida"
```

#### 8. Dia da semana

Faça uma função que receba um número (1-7) e retorne o dia da semana correspondente.

```javascript
function diaDaSemana(numero) {
    switch (numero) {
        case 1:
            return "Segunda-feira";
        case 2:
            return "Terça-feira";
        case 3:
            return "Quarta-feira";
        case 4:
            return "Quinta-feira";
        case 5:
            return "Sexta-feira";
        case 6:
            return "Sábado";
        case 7:
            return "Domingo";
        default:
            return "Número inválido. Use 1-7.";
    }
}

// Versão com array
function diaDaSemanaArray(numero) {
    const dias = ["", "Segunda-feira", "Terça-feira", "Quarta-feira", 
                  "Quinta-feira", "Sexta-feira", "Sábado", "Domingo"];
    
    if (numero >= 1 && numero <= 7) {
        return dias[numero];
    } else {
        return "Número inválido. Use 1-7.";
    }
}

// Teste
console.log(diaDaSemana(1));  // "Segunda-feira"
console.log(diaDaSemana(7));  // "Domingo"
console.log(diaDaSemana(8));  // "Número inválido. Use 1-7."
```

#### 9. Verificar se é número

Crie uma função que determine se um valor é realmente um número (não NaN, não string numérica).

```javascript
function ehNumero(valor) {
    return typeof valor === "number" && !isNaN(valor);
}

// Versão mais rigorosa (exclui Infinity)
function ehNumeroFinito(valor) {
    return typeof valor === "number" && !isNaN(valor) && isFinite(valor);
}

// Teste
console.log(ehNumero(42));        // true
console.log(ehNumero("42"));      // false
console.log(ehNumero(NaN));       // false
console.log(ehNumero(Infinity));  // true
console.log(ehNumero(true));      // false
console.log(ehNumeroFinito(Infinity)); // false
```

#### 10. Comparar três números

Escreva uma função que receba três números e retorne qual é o maior, o menor, e o do meio.

```javascript
function compararTresNumeros(a, b, c) {
    const numeros = [a, b, c].sort((x, y) => x - y);
    
    return {
        menor: numeros[0],
        meio: numeros[1],
        maior: numeros[2]
    };
}

// Versão sem usar sort
function compararTresNumerosSemSort(a, b, c) {
    let maior, menor, meio;
    
    // Encontrar maior
    if (a >= b && a >= c) {
        maior = a;
    } else if (b >= a && b >= c) {
        maior = b;
    } else {
        maior = c;
    }
    
    // Encontrar menor
    if (a <= b && a <= c) {
        menor = a;
    } else if (b <= a && b <= c) {
        menor = b;
    } else {
        menor = c;
    }
    
    // O do meio é o que sobra
    meio = (a + b + c) - maior - menor;
    
    return { menor, meio, maior };
}

// Teste
console.log(compararTresNumeros(10, 5, 8));  // {menor: 5, meio: 8, maior: 10}
console.log(compararTresNumeros(3, 3, 7));   // {menor: 3, meio: 3, maior: 7}
```

#### 11. Validar senha simples

Crie uma função que verifique se uma senha tem pelo menos 6 caracteres e contenha pelo menos um número.

```javascript
function validarSenha(senha) {
    if (senha.length < 6) {
        return false;
    }
    
    // Verificar se tem pelo menos um número
    for (let i = 0; i < senha.length; i++) {
        if (!isNaN(senha[i]) && senha[i] !== " ") {
            return true;
        }
    }
    
    return false;
}

// Versão usando regex
function validarSenhaRegex(senha) {
    return senha.length >= 6 && /\d/.test(senha);
}

// Teste
console.log(validarSenha("abc123"));     // true
console.log(validarSenha("abcdef"));     // false
console.log(validarSenha("ab1"));        // false
console.log(validarSenhaRegex("senha9")); // true
```

#### 12. Conversor de notas

Faça uma função que converta notas numéricas (0-100) em conceitos (A, B, C, D, F).

```javascript
function converterNota(nota) {
    if (nota < 0 || nota > 100) {
        return "Nota inválida";
    }
    
    if (nota >= 90) {
        return "A";
    } else if (nota >= 80) {
        return "B";
    } else if (nota >= 70) {
        return "C";
    } else if (nota >= 60) {
        return "D";
    } else {
        return "F";
    }
}

// Teste
console.log(converterNota(95));  // "A"
console.log(converterNota(85));  // "B"
console.log(converterNota(75));  // "C"
console.log(converterNota(65));  // "D"
console.log(converterNota(45));  // "F"
console.log(converterNota(105)); // "Nota inválida"
```

### 🟡 MÉDIO

#### 13. Validador de CPF básico

Crie uma função que verifique se um CPF tem 11 dígitos e não é uma sequência repetida (111.111.111-11).

```javascript
function validarCPFBasico(cpf) {
    // Remove pontos e traços
    const cpfLimpo = cpf.replace(/[.-]/g, "");
    
    // Verifica se tem 11 dígitos
    if (cpfLimpo.length !== 11) {
        return false;
    }
    
    // Verifica se são todos números
    if (!/^\d+$/.test(cpfLimpo)) {
        return false;
    }
    
    // Verifica se não é sequência repetida
    const primeiroDigito = cpfLimpo[0];
    if (cpfLimpo.split("").every(digito => digito === primeiroDigito)) {
        return false;
    }
    
    return true;
}

// Teste
console.log(validarCPFBasico("123.456.789-10")); // true
console.log(validarCPFBasico("111.111.111-11")); // false
console.log(validarCPFBasico("123.456.789-1"));  // false
console.log(validarCPFBasico("abc.def.ghi-jk")); // false
```

#### 14. Calculadora de IMC com classificação

Desenvolva uma função que calcule o IMC e retorne a classificação (abaixo do peso, normal, sobrepeso, obesidade).

```javascript
function calcularIMC(peso, altura) {
    if (peso <= 0 || altura <= 0) {
        return "Valores inválidos";
    }
    
    const imc = peso / (altura * altura);
    let classificacao;
    
    if (imc < 18.5) {
        classificacao = "Abaixo do peso";
    } else if (imc < 25) {
        classificacao = "Peso normal";
    } else if (imc < 30) {
        classificacao = "Sobrepeso";
    } else if (imc < 35) {
        classificacao = "Obesidade grau I";
    } else if (imc < 40) {
        classificacao = "Obesidade grau II";
    } else {
        classificacao = "Obesidade grau III";
    }
    
    return {
        imc: imc.toFixed(2),
        classificacao: classificacao
    };
}

// Teste
console.log(calcularIMC(70, 1.75));  // {imc: "22.86", classificacao: "Peso normal"}
console.log(calcularIMC(50, 1.70));  // {imc: "17.30", classificacao: "Abaixo do peso"}
console.log(calcularIMC(90, 1.75));  // {imc: "29.39", classificacao: "Sobrepeso"}
```

#### 15. Verificador de ano bissexto

Implemente a lógica completa para determinar se um ano é bissexto.

```javascript
function ehAnoBissexto(ano) {
    // Um ano é bissexto se:
    // 1. É divisível por 4 E
    // 2. Se for divisível por 100, também deve ser divisível por 400
    
    if (ano % 4 !== 0) {
        return false;
    }
    
    if (ano % 100 !== 0) {
        return true;
    }
    
    if (ano % 400 === 0) {
        return true;
    }
    
    return false;
}

// Versão mais concisa
function ehAnoBissextoConciso(ano) {
    return (ano % 4 === 0 && ano % 100 !== 0) || (ano % 400 === 0);
}

// Teste
console.log(ehAnoBissexto(2024));  // true
console.log(ehAnoBissexto(2023));  // false
console.log(ehAnoBissexto(1900));  // false
console.log(ehAnoBissexto(2000));  // true
```

#### 16. Validador de email básico

Crie uma função que verifique se um email tem formato válido (contém @ e ponto, não começa/termina com caracteres especiais).

```javascript
function validarEmailBasico(email) {
    // Verifica se é string e não está vazia
    if (typeof email !== "string" || email.trim() === "") {
        return false;
    }
    
    const emailLimpo = email.trim();
    
    // Deve conter exatamente um @
    const arrobas = emailLimpo.split("@");
    if (arrobas.length !== 2) {
        return false;
    }
    
    const [usuario, dominio] = arrobas;
    
    // Usuário não pode estar vazio
    if (usuario.length === 0) {
        return false;
    }
    
    // Domínio deve conter pelo menos um ponto
    if (!dominio.includes(".")) {
        return false;
    }
    
    // Não pode começar ou terminar com caracteres especiais
    const caracteresEspeciais = /^[.@]|[.@]$/;
    if (caracteresEspeciais.test(emailLimpo)) {
        return false;
    }
    
    // Deve ter algo após o último ponto
    const partesDominio = dominio.split(".");
    if (partesDominio[partesDominio.length - 1].length < 2) {
        return false;
    }
    
    return true;
}

// Teste
console.log(validarEmailBasico("user@example.com"));    // true
console.log(validarEmailBasico("user@example"));        // false
console.log(validarEmailBasico("@example.com"));        // false
console.log(validarEmailBasico("user@"));               // false
console.log(validarEmailBasico("user@example."));       // false
console.log(validarEmailBasico("user@example.c"));      // false
```

#### 17. Jogo de pedra, papel, tesoura

Desenvolva uma função que simule o jogo, recebendo as escolhas de dois jogadores e determinando o vencedor.

```javascript
function pedraPapelTesoura(jogador1, jogador2) {
    const opcoes = ["pedra", "papel", "tesoura"];
    
    // Validar entradas
    if (!opcoes.includes(jogador1.toLowerCase()) || !opcoes.includes(jogador2.toLowerCase())) {
        return "Opção inválida. Use: pedra, papel ou tesoura";
    }
    
    const p1 = jogador1.toLowerCase();
    const p2 = jogador2.toLowerCase();
    
    // Empate
    if (p1 === p2) {
        return "Empate!";
    }
    
    // Vitórias do jogador 1
    if ((p1 === "pedra" && p2 === "tesoura") ||
        (p1 === "papel" && p2 === "pedra") ||
        (p1 === "tesoura" && p2 === "papel")) {
        return "Jogador 1 vence!";
    } else {
        return "Jogador 2 vence!";
    }
}

// Teste
console.log(pedraPapelTesoura("pedra", "tesoura"));  // "Jogador 1 vence!"
console.log(pedraPapelTesoura("papel", "pedra"));    // "Jogador 1 vence!"
console.log(pedraPapelTesoura("pedra", "papel"));    // "Jogador 2 vence!"
console.log(pedraPapelTesoura("pedra", "pedra"));    // "Empate!"
```

#### 18. Classificador de triângulos

Faça uma função que determine se três lados podem formar um triângulo e classifique-o (equilátero, isósceles, escaleno).

```javascript
function classificarTriangulo(a, b, c) {
    // Verificar se os valores são positivos
    if (a <= 0 || b <= 0 || c <= 0) {
        return "Lados devem ser positivos";
    }
    
    // Verificar se podem formar um triângulo (desigualdade triangular)
    if (a + b <= c || a + c <= b || b + c <= a) {
        return "Não forma um triângulo";
    }
    
    // Classificar o triângulo
    if (a === b && b === c) {
        return "Triângulo equilátero";
    } else if (a === b || b === c || a === c) {
        return "Triângulo isósceles";
    } else {
        return "Triângulo escaleno";
    }
}

// Teste
console.log(classificarTriangulo(3, 3, 3));    // "Triângulo equilátero"
console.log(classificarTriangulo(3, 3, 4));    // "Triângulo isósceles"
console.log(classificarTriangulo(3, 4, 5));    // "Triângulo escaleno"
console.log(classificarTriangulo(1, 1, 5));    // "Não forma um triângulo"
console.log(classificarTriangulo(-1, 2, 3));   // "Lados devem ser positivos"
```

#### 19. Conversor de temperatura múltiplo

Crie uma função que converta temperaturas entre Celsius, Fahrenheit e Kelvin.

```javascript
function converterTemperatura(valor, de, para) {
    const unidades = ["celsius", "fahrenheit", "kelvin"];
    
    if (!unidades.includes(de.toLowerCase()) || !unidades.includes(para.toLowerCase())) {
        return "Unidade inválida. Use: celsius, fahrenheit ou kelvin";
    }
    
    const origem = de.toLowerCase();
    const destino = para.toLowerCase();
    
    // Se são iguais, retorna o mesmo valor
    if (origem === destino) {
        return valor;
    }
    
    let celsius;
    
    // Converter para Celsius primeiro
    switch (origem) {
        case "celsius":
            celsius = valor;
            break;
        case "fahrenheit":
            celsius = (valor - 32) * 5/9;
            break;
        case "kelvin":
            celsius = valor - 273.15;
            break;
    }
    
    // Converter de Celsius para o destino
    let resultado;
    switch (destino) {
        case "celsius":
            resultado = celsius;
            break;
        case "fahrenheit":
            resultado = celsius * 9/5 + 32;
            break;
        case "kelvin":
            resultado = celsius + 273.15;
            break;
    }
    
    return parseFloat(resultado.toFixed(2));
}

// Teste
console.log(converterTemperatura(0, "celsius", "fahrenheit"));    // 32
console.log(converterTemperatura(32, "fahrenheit", "celsius"));   // 0
console.log(converterTemperatura(273.15, "kelvin", "celsius"));   // 0
console.log(converterTemperatura(100, "celsius", "kelvin"));      // 373.15
```

#### 20. Sistema de desconto progressivo

Implemente um sistema que calcule descontos baseados no valor da compra (0-100: 0%, 101-500: 5%, 501-1000: 10%, 1000+: 15%).

```javascript
function calcularDesconto(valorCompra) {
    if (valorCompra < 0) {
        return "Valor inválido";
    }
    
    let percentualDesconto;
    
    if (valorCompra <= 100) {
        percentualDesconto = 0;
    } else if (valorCompra <= 500) {
        percentualDesconto = 0.05; // 5%
    } else if (valorCompra <= 1000) {
        percentualDesconto = 0.10; // 10%
    } else {
        percentualDesconto = 0.15; // 15%
    }
    
    const valorDesconto = valorCompra * percentualDesconto;
    const valorFinal = valorCompra - valorDesconto;
    
    return {
        valorOriginal: valorCompra,
        percentualDesconto: (percentualDesconto * 100) + "%",
        valorDesconto: parseFloat(valorDesconto.toFixed(2)),
        valorFinal: parseFloat(valorFinal.toFixed(2))
    };
}

// Teste
console.log(calcularDesconto(80));    // 0% desconto
console.log(calcularDesconto(300));   // 5% desconto
console.log(calcularDesconto(800));   // 10% desconto
console.log(calcularDesconto(1500));  // 15% desconto
```

### 🔴 AVANÇADO

#### 21. Validador de cartão de crédito (Algoritmo de Luhn)

Implemente o algoritmo de Luhn para validar números de cartão de crédito.

```javascript
function validarCartaoCredito(numero) {
    // Remove espaços e traços
    const numeroLimpo = numero.replace(/[\s-]/g, "");
    
    // Verifica se contém apenas números
    if (!/^\d+$/.test(numeroLimpo)) {
        return false;
    }
    
    // Verifica se tem entre 13 e 19 dígitos
    if (numeroLimpo.length < 13 || numeroLimpo.length > 19) {
        return false;
    }
    
    // Algoritmo de Luhn
    let soma = 0;
    let alternar = false;
    
    // Percorre da direita para esquerda
    for (let i = numeroLimpo.length - 1; i >= 0; i--) {
        let digito = parseInt(numeroLimpo[i]);
        
        if (alternar) {
            digito *= 2;
            if (digito > 9) {
                digito -= 9;
            }
```
