# Ferramental com Node no Win

### O que é o Winget?

O **Winget** (ou Gerenciador de Pacotes do Windows) é uma ferramenta de linha de comando gratuita e de código aberto desenvolvida pela Microsoft. Pensem nele como um "App Store" para o terminal. Com ele, em vez de você precisar:

1. Abrir o navegador.
2. Pesquisar pelo site do programa (ex: Node.js).
3. Procurar o link de download correto.
4. Baixar o instalador.
5. Clicar em "Avançar" várias vezes.

Você simplesmente abre o seu terminal (PowerShell ou Prompt de Comando) e digita um único comando. Simples assim!

**Principais vantagens:**

* **Rapidez:** Instala, atualiza e remove programas com um único comando.
* **Segurança:** Busca os pacotes em repositórios confiáveis, evitando downloads de fontes duvidosas.
* **Automação:** Facilita a configuração de um novo ambiente de desenvolvimento, permitindo instalar todas as suas ferramentas de uma só vez com um script.
* **Padronização:** Garante que toda a equipe esteja usando as mesmas versões de software.

***

### Tutorial: Instalando o Node.js com o Winget

Vamos ao que interessa! Instalar o Node.js com o Winget é um processo de dois passos: procurar o pacote e instalá-lo.

#### Pré-requisito

O Winget já vem instalado por padrão no **Windows 11** e nas versões mais recentes do **Windows 10**. Para verificar se você o tem, abra o **PowerShell** e digite:

```powershell
winget --version
```

Se aparecer a versão, está tudo pronto! Se não, você pode instalá-lo a partir da [Microsoft Store](https://www.google.com/search?q=https://apps.microsoft.com/store/detail/instalador-de-aplicativo/9NBLGGH4NNS1).

#### Passo 1: Procurar o Pacote do Node.js

Primeiro, vamos pesquisar pelo Node.js no repositório do Winget para ver as versões disponíveis.

Abra o PowerShell e execute o comando:

```powershell
winget search nodejs
```

A saída será algo parecido com isto:

```
Nome    ID                          Versão      Fonte
------------------------------------------------------
Node.js OpenJS.Nodejs               20.11.1     winget
Node.js OpenJS.Nodejs.LTS           20.11.1     winget
Node.js OpenJS.Nodejs.Current       21.7.1      winget
```

Note que temos algumas opções. A mais comum e recomendada para a maioria dos casos é a versão **LTS** (Long-Term Support), que é a mais estável. A ID para ela é `OpenJS.Nodejs.LTS`.

#### Passo 2: Instalar o Node.js

Agora que já sabemos a ID do pacote, vamos usar o comando `winget install`.

```powershell
winget install OpenJS.Nodejs.LTS
```

O Winget vai baixar o instalador oficial e executá-lo para você de forma silenciosa. Ao final do processo, o Node.js e o npm (Node Package Manager) estarão instalados e prontos para uso.

#### Passo 3: Verificar a Instalação

Para confirmar que tudo deu certo, feche e abra novamente o PowerShell (para atualizar as variáveis de ambiente) e verifique as versões do Node.js e do npm:

```powershell
node -v
```

```powershell
npm -v
```

Se os comandos retornarem os números das versões, parabéns! Você instalou o Node.js de forma rápida e eficiente com o Winget. 🎉
