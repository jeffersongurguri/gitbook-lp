# Exercícios - Désvios Condicionais

Com certeza! Aqui estão todos os exercícios de desvios condicionais em JavaScript, reunidos em um único arquivo Markdown para facilitar o acesso e a prática.

***

## Exercícios de Desvios Condicionais em JavaScript (Contexto: Automação)

**Objetivo:** Praticar o uso de `if-else` e `switch` para criar lógicas de decisão em cenários de automação.

***

#### Exercício 1: Controle de Temperatura de Ambiente

**Cenário:** Você está programando um sistema de automação residencial que controla a temperatura de um ambiente.

Tarefa:

Crie uma função controlarTemperatura(temperaturaAtual) que recebe a temperatura atual do ambiente como parâmetro.

* Se a temperatura for **menor que 20°C**, a função deve retornar "Ligar aquecedor".
* Se a temperatura for **entre 20°C e 25°C (inclusive)**, a função deve retornar "Manter temperatura ideal".
* Se a temperatura for **maior que 25°C**, a função deve retornar "Ligar ar-condicionado".

**Exemplo de uso:**

JavaScript

```javascript
console.log(controlarTemperatura(18)); // Deve retornar "Ligar aquecedor"
console.log(controlarTemperatura(22)); // Deve retornar "Manter temperatura ideal"
console.log(controlarTemperatura(27)); // Deve retornar "Ligar ar-condicionado"
```

***

#### Exercício 2: Status de Portão Automático

**Cenário:** Um sistema de automação para portões precisa identificar o status do portão (aberto, fechado, abrindo, fechando) com base em um código numérico.

Tarefa:

Crie uma função obterStatusPortao(codigoStatus) que recebe um código numérico como parâmetro.

* Use a estrutura `switch` para os seguintes casos:
  * `0`: Retornar "Portão Fechado"
  * `1`: Retornar "Portão Aberto"
  * `2`: Retornar "Portão Abrindo"
  * `3`: Retornar "Portão Fechando"
* Para qualquer outro código, retornar "Status desconhecido".

**Exemplo de uso:**

JavaScript

```javascript
console.log(obterStatusPortao(0)); // Deve retornar "Portão Fechado"
console.log(obterStatusPortao(1)); // Deve retornar "Portão Aberto"
console.log(obterStatusPortao(5)); // Deve retornar "Status desconhecido"
```

***

#### Exercício 3: Nível de Bateria de Dispositivo IoT

**Cenário:** Você está desenvolvendo um aplicativo para monitorar o nível de bateria de dispositivos IoT (Internet das Coisas).

Tarefa:

Crie uma função verificarBateria(nivelBateriaPercentual) que recebe o nível da bateria em porcentagem.

* Se o nível for **menor que 10%**, retornar "Bateria crítica! Carregar imediatamente.".
* Se o nível for **entre 10% e 30% (inclusive)**, retornar "Bateria baixa. Considerar carregar.".
* Se o nível for **entre 31% e 70% (inclusive)**, retornar "Bateria em nível normal.".
* Se o nível for **maior que 70%**, retornar "Bateria cheia.".

**Exemplo de uso:**

JavaScript

```javascript
console.log(verificarBateria(5));  // Deve retornar "Bateria crítica! Carregar imediatamente."
console.log(verificarBateria(25)); // Deve retornar "Bateria baixa. Considerar carregar."
console.log(verificarBateria(50)); // Deve retornar "Bateria em nível normal."
console.log(verificarBateria(90)); // Deve retornar "Bateria cheia."
```

***

#### Exercício 4: Controle de Iluminação Inteligente

**Cenário:** Um sistema de iluminação inteligente precisa ajustar a intensidade da luz com base na hora do dia.

Tarefa:

Crie uma função ajustarIluminacao(horaDoDia) que recebe a hora do dia (em formato 24h, de 0 a 23).

* Se a hora for **entre 6 e 17 (inclusive)**, retornar "Luz em intensidade alta (dia)".
* Se a hora for **entre 18 e 22 (inclusive)**, retornar "Luz em intensidade média (noite)".
* Se a hora for **entre 23 e 5 (inclusive)**, retornar "Luz em intensidade baixa (madrugada)".
* Para qualquer outro valor inválido de hora, retornar "Hora inválida".

**Exemplo de uso:**

JavaScript

```javascript
console.log(ajustarIluminacao(8));  // Deve retornar "Luz em intensidade alta (dia)"
console.log(ajustarIluminacao(19)); // Deve retornar "Luz em intensidade média (noite)"
console.log(ajustarIluminacao(2));  // Deve retornar "Luz em intensidade baixa (madrugada)"
console.log(ajustarIluminacao(25)); // Deve retornar "Hora inválida"
```

***

#### Exercício 5: Validação de Comando de Voz para Robô

**Cenário:** Um robô de serviço recebe comandos de voz e precisa validá-los antes de executar a ação.

Tarefa:

Crie uma função validarComandoRobo(comando) que recebe uma string com o comando.

* Use a estrutura `switch` para verificar os seguintes comandos válidos (case-insensitive):
  * "mover para frente"
  * "mover para trás"
  * "virar direita"
  * "virar esquerda"
  * "parar"
* Se o comando for válido, retornar "Comando 'X' recebido e válido.", onde 'X' é o comando original.
* Se o comando não for válido, retornar "Comando inválido. Tente novamente.".

**Dica:** Para tornar case-insensitive, você pode converter o `comando` para minúsculas antes de usar no `switch` (ex: `comando.toLowerCase()`).

**Exemplo de uso:**

JavaScript

```javascript
console.log(validarComandoRobo("Mover para frente")); // Deve retornar "Comando 'Mover para frente' recebido e válido."
console.log(validarComandoRobo("PARAR"));             // Deve retornar "Comando 'PARAR' recebido e válido."
console.log(validarComandoRobo("Abrir porta"));       // Deve retornar "Comando inválido. Tente novamente."
```

***

