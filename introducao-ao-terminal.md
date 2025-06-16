# Introdução ao Terminal

## 🚀 Introdução ao Terminal PowerShell

### Um primeiro olhar sobre o terminal moderno da Microsoft

***

### O que é o PowerShell? 🤔

O **PowerShell** é um terminal de linha de comando e uma linguagem de script desenvolvido pela Microsoft. Diferente do antigo _Prompt de Comando (CMD)_, ele é construído sobre a plataforma .NET, o que o torna muito mais poderoso e flexível.

* **Multiplataforma**: Funciona no Windows, Linux e macOS.
* **Orientado a Objetos**: Em vez de texto, o PowerShell trabalha com objetos, permitindo uma manipulação de dados mais estruturada.
* **Automatização**: É a ferramenta ideal para automatizar tarefas administrativas e gerenciar sistemas.

***

### Abrindo o Terminal 🚀

Para começar, você pode encontrar o PowerShell de algumas formas:

1. **Menu Iniciar**: Simplesmente digite "PowerShell" na busca.
2. **Menu de Contexto (Win+X)**: Pressione `Windows + X` e selecione "Terminal" ou "PowerShell".
3. **Executar**: Pressione `Windows + R`, digite `powershell` e pressione Enter.

Você verá uma janela com um prompt, geralmente `PS C:\Users\SeuUsuario>`, esperando seus comandos.

***

### Cmdlets: O Coração do PowerShell ❤️

No PowerShell, os comandos são chamados de **Cmdlets** (pronuncia-se "command-lets"). Eles seguem um padrão de nomenclatura bem intuitivo: **`Verbo-Substantivo`**.

| Verbo    | Ação                          |
| -------- | ----------------------------- |
| `Get`    | Para obter algo.              |
| `Set`    | Para definir ou alterar algo. |
| `New`    | Para criar algo novo.         |
| `Remove` | Para apagar algo.             |
| `Start`  | Para iniciar um processo.     |

Isso torna os comandos mais fáceis de lembrar e entender!

***

### Comandos Essenciais para Navegação 🧭

Vamos aos primeiros comandos para você se movimentar pelos diretórios do seu sistema.

* **`Get-Location`**: Mostra o diretório (pasta) atual.
* **`Set-Location`**: Muda de diretório.
* **`Get-ChildItem`**: Lista o conteúdo de um diretório.

```powershell
# Ver o diretório atual
PS C:\> Get-Location

# Mudar para a pasta "Documentos"
PS C:\> Set-Location C:\Users\SeuUsuario\Documents

# Listar o conteúdo da pasta atual
PS C:\Users\SeuUsuario\Documents> Get-ChildItem
```

Guri - Conteudista Moodle\
Gem personalizado

Mostrar raciocínio\
Olá, turma!

Preparei uma apresentação em slides para a nossa introdução ao terminal PowerShell. O objetivo é que vocês compreendam o que é essa ferramenta poderosa, como ela funciona e, claro, aprendam os primeiros comandos para já começarem a praticar.

O material foi todo feito em Marp, o que nos permite focar no conteúdo e manter um formato limpo e acessível. Vamos lá!

Markdown

## 🚀 Introdução ao Terminal PowerShell

### Um primeiro olhar sobre o terminal moderno da Microsoft

***

### O que é o PowerShell? 🤔

O **PowerShell** é um terminal de linha de comando e uma linguagem de script desenvolvido pela Microsoft. Diferente do antigo _Prompt de Comando (CMD)_, ele é construído sobre a plataforma .NET, o que o torna muito mais poderoso e flexível.

* **Multiplataforma**: Funciona no Windows, Linux e macOS.
* **Orientado a Objetos**: Em vez de texto, o PowerShell trabalha com objetos, permitindo uma manipulação de dados mais estruturada.
* **Automatização**: É a ferramenta ideal para automatizar tarefas administrativas e gerenciar sistemas.

***

### Abrindo o Terminal 🚀

Para começar, você pode encontrar o PowerShell de algumas formas:

1. **Menu Iniciar**: Simplesmente digite "PowerShell" na busca.
2. **Menu de Contexto (Win+X)**: Pressione `Windows + X` e selecione "Terminal" ou "PowerShell".
3. **Executar**: Pressione `Windows + R`, digite `powershell` e pressione Enter.

Você verá uma janela com um prompt, geralmente `PS C:\Users\SeuUsuario>`, esperando seus comandos.

***

### Cmdlets: O Coração do PowerShell ❤️

No PowerShell, os comandos são chamados de **Cmdlets** (pronuncia-se "command-lets"). Eles seguem um padrão de nomenclatura bem intuitivo: **`Verbo-Substantivo`**.

| Verbo    | Ação                          |
| -------- | ----------------------------- |
| `Get`    | Para obter algo.              |
| `Set`    | Para definir ou alterar algo. |
| `New`    | Para criar algo novo.         |
| `Remove` | Para apagar algo.             |
| `Start`  | Para iniciar um processo.     |

Isso torna os comandos mais fáceis de lembrar e entender!

***

### Comandos Essenciais para Navegação 🧭

Vamos aos primeiros comandos para você se movimentar pelos diretórios do seu sistema.

* **`Get-Location`**: Mostra o diretório (pasta) atual.
* **`Set-Location`**: Muda de diretório.
* **`Get-ChildItem`**: Lista o conteúdo de um diretório.

```powershell
# Ver o diretório atual
PS C:\> Get-Location

# Mudar para a pasta "Documentos"
PS C:\> Set-Location C:\Users\SeuUsuario\Documents

# Listar o conteúdo da pasta atual
PS C:\Users\SeuUsuario\Documents> Get-ChildItem
Aliases: Os Apelidos Amigáveis 😉
Digitar Get-ChildItem toda vez pode ser cansativo. Por isso, o PowerShell tem Aliases, que são apelidos para os Cmdlets. Muitos deles são familiares para quem já usou outros terminais!
```

| Alias | Cmdlet Original | Descrição                  |
| ----- | --------------- | -------------------------- |
| pwd   | Get-Location    | Mostra o diretório atual   |
| cd    | Set-Location    | Muda de diretório          |
| ls    | Get-ChildItem   | Lista o conteúdo (Linux)   |
| dir   | Get-ChildItem   | Lista o conteúdo (Windows) |
| cls   | Clear-Host      | Limpa a tela do terminal   |

***

### Manipulando Arquivos e Pastas 📂

Agora, vamos criar e remover coisas!

New-Item: Cria um novo item (arquivo ou diretório).\
Remove-Item: Remove um item.\
PowerShel

```powershell
# Criar uma nova pasta chamada "MeusProjetos"
PS C:\Users\SeuUsuario\Documents> New-Item -Name "MeusProjetos" -ItemType Directory

# Entrar na nova pasta
PS C:\Users\SeuUsuario\Documents> cd MeusProjetos

# Criar um arquivo de texto vazio
PS C:\...\MeusProjetos> New-Item -Name "anotacoes.txt" -ItemType File

# Apagar o arquivo (cuidado!)
PS C:\...\MeusProjetos> Remove-Item -Name "anotacoes.txt"
Dica: Use o parâmetro -Force com Remove-Item para deletar pastas que não estão vazias.
```

***

### Pedindo Ajuda: Get-Help 🆘

Ninguém precisa decorar tudo! O comando Get-Help é seu melhor amigo para aprender sobre qualquer Cmdlet.

```powershell

# Obter ajuda sobre o comando Get-ChildItem
PS C:\> Get-Help Get-ChildItem

# Ver exemplos práticos de uso
PS C:\> Get-Help Get-ChildItem -Examples

# Abrir a documentação completa online
PS C:\> Get-Help Get-ChildItem -Online
```
