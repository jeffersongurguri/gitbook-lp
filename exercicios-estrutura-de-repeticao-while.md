# Exercícios - Estrutura de Repetição - While

Com certeza! Aqui estão todos os exercícios de estruturas de repetição `while` em JavaScript, reunidos em um único arquivo Markdown para você praticar.

***

## Exercícios de Estruturas de Repetição `while` em JavaScript (Contexto: Automação)

**Objetivo:** Praticar o uso do laço `while` para criar lógicas de repetição e controle em cenários de automação.

***

#### Exercício 1: Contagem Regressiva de Lançamento

**Cenário:** Você está programando o painel de controle de um lançamento de foguete automatizado que exibe uma contagem regressiva.

Tarefa:

Crie uma função contagemRegressiva(tempoInicial) que recebe um número inteiro tempoInicial como parâmetro. A função deve imprimir no console a contagem regressiva a partir desse tempo até 0. Ao chegar em 0, deve imprimir "Lançamento!". Use um laço while.

**Exemplo de uso:**

JavaScript

```
contagemRegressiva(5);
// Saída esperada:
// 5
// 4
// 3
// 2
// 1
// Lançamento!
```

***

#### Exercício 2: Monitoramento de Nível de Gás

**Cenário:** Um sensor em um sistema de automação industrial monitora o nível de gás em um tanque. O sistema precisa alertar quando o nível atingir ou ultrapassar um limite crítico.

Tarefa:

Crie uma função monitorarNivelGas(nivelAtual, limiteCritico) que recebe o nivelAtual de gás (um número) e o limiteCritico (um número). A função deve simular o monitoramento, incrementando o nivelAtual em 0.5 a cada iteração, e imprimir o nível atual. O laço while deve continuar enquanto o nivelAtual for menor que o limiteCritico. Quando o limite for atingido ou ultrapassado, deve imprimir "Alerta: Nível de gás crítico!".

**Exemplo de uso:**

JavaScript

```
monitorarNivelGas(98, 100);
// Saída esperada:
// Nível de Gás: 98.5
// Nível de Gás: 99
// Nível de Gás: 99.5
// Nível de Gás: 100
// Alerta: Nível de gás crítico!
```

***

#### Exercício 3: Tentativas de Conexão de Dispositivo

**Cenário:** Um dispositivo IoT tenta se conectar a uma rede. Você precisa programar o número máximo de tentativas antes de falhar.

Tarefa:

Crie uma função tentarConexao(maxTentativas) que recebe o número máximo de tentativas. A função deve simular as tentativas de conexão, imprimindo "Tentando conexão... (Tentativa X de Y)" a cada iteração, onde X é a tentativa atual e Y é o número máximo. Use um laço while. Se a conexão for bem-sucedida (simule com um número aleatório ou simplesmente deixe o laço rodar até o fim), imprima "Conexão estabelecida!" ou "Falha na conexão após X tentativas.".

**Considerando para este exercício que a conexão sempre falhará para fins de demonstração do `while`:** O laço deve rodar até o `maxTentativas` ser alcançado.

**Exemplo de uso:**

JavaScript

```
tentarConexao(3);
// Saída esperada:
// Tentando conexão... (Tentativa 1 de 3)
// Tentando conexão... (Tentativa 2 de 3)
// Tentando conexão... (Tentativa 3 de 3)
// Falha na conexão após 3 tentativas.
```

***

#### Exercício 4: Varredura de Sensores com Limite de Leituras

**Cenário:** Um sistema automatizado realiza varreduras contínuas de um conjunto de sensores até atingir um determinado número de leituras.

Tarefa:

Crie uma função realizarVarredura(leiturasDesejadas) que recebe o número de leituras que o sistema deve fazer. A função deve simular a leitura dos sensores, imprimindo "Realizando leitura do sensor... (Leitura N de M)" a cada iteração. Use um laço while para garantir que o número de leituras desejadas seja alcançado. Ao final, imprima "Varredura de sensores concluída!".

**Exemplo de uso:**

JavaScript

```
realizarVarredura(4);
// Saída esperada:
// Realizando leitura do sensor... (Leitura 1 de 4)
// Realizando leitura do sensor... (Leitura 2 de 4)
// Realizando leitura do sensor... (Leitura 3 de 4)
// Realizando leitura do sensor... (Leitura 4 de 4)
// Varredura de sensores concluída!
```

***

#### Exercício 5: Enfileiramento de Tarefas de Impressão

**Cenário:** Uma impressora 3D automatizada tem uma fila de tarefas a serem processadas. O sistema deve processar as tarefas uma a uma até que a fila esteja vazia.

Tarefa:

Crie uma função processarFilaImpressao(quantidadeTarefas) que recebe a quantidade inicial de tarefas na fila. A função deve simular o processamento, imprimindo "Processando tarefa de impressão... (Restam X tarefas)" a cada iteração, onde X é o número de tarefas restantes. Use um laço while para continuar o processamento enquanto houver tarefas na fila (ou seja, a quantidade de tarefas for maior que 0). Ao final, imprima "Todas as tarefas de impressão concluídas!".

**Exemplo de uso:**

JavaScript

```
processarFilaImpressao(3);
// Saída esperada:
// Processando tarefa de impressão... (Restam 2 tarefas)
// Processando tarefa de impressão... (Restam 1 tarefas)
// Processando tarefa de impressão... (Restam 0 tarefas)
// Todas as tarefas de impressão concluídas!
```

***

**Instruções para os alunos:**

1. Crie um novo arquivo JavaScript (por exemplo, `automacao_while.js`).
2. Copie e cole todo o conteúdo deste Markdown nele.
3. Para cada exercício, escreva a função correspondente.
4. Teste suas funções com os exemplos fornecidos e adicione seus próprios testes para garantir que tudo funcione como esperado.
5. Execute seu código usando Node.js (se estiver no ambiente de desenvolvimento) ou no console do navegador.

Espero que essa compilação seja útil para a sua prática de JavaScript!
