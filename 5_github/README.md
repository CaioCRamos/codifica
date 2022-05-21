# Git e Github

O **Git** é uma ferramenta de versionamento de código gratuíta e Open Source utilizada mundialmente. Funciona originalmente através de linhas de comando no terminal, porém pode ser utilizada de outras formas. 

Já o **GitHub** é uma plataforma Online bastante completa e que faz de tudo um pouco, desde o armazenamento do nosso código, automatização de tarefas, permissionamento de acesso, rede social para interação entre desenvolvedores e projetos, etc ([saiba mais](https://github.com/about)).

Os dois funcionam muito bem em conjunto pois utilizamos todo a mecânica e comandos disponíveis no **Git** e armazenamos e disponibilizamos nossos código no **Github**.

Então, para começar a utilizar primeiro você precisa seguir 2 passos:
1. Criar uma conta no [Github](https://github.com/signup)
1. [Baixar](https://git-scm.com/download) e instalar o Git na sua máquina de trabalho, pode ser: **Windows**, **Linux** ou **Mac**.

## Primeiros passos
Após instalar o Git em sua máquina, confira se a instalação foi bem sucedida abrindo o terminal ou prompt de comandos da sua máquina e executando o seguinte:
```
git --version
```
O comando acima consulta qual a versão do Git está instalada atualmente e como resultado é esperado um retorno similar o descrito abaixo, porém com valores diferentes dependendo de quando você está executando este passo, qual versão instalou e em qual sistema.
```
git version 2.36.1.windows.1
```
Se não houver nenhuma versão do Git instalada na sua máquina, um erro será mostrado.

## Configuração inicial
Ainda com o terminal aberto, é necessário realizar duas configurações iniciais:

A primeira é o nome do seu usuário, apenas um texto para identificar as ações que serão desempenhadas no futuro
```
git config --global user.name "Seu Nome aqui"

```
O segundo é o seu e-mail, deve ser o mesmo utilizado para criar a conta no Github:
```
git config --global user.email "seuemail@email.com"
```
Para verificar se tudo foi configurado corretamente, você pode executar o comando `git config --list`, como resultado, você verá uma listagem de configurações do Git, muitas delas já vem configuradas por padrão. O importante aqui é identificar se as configurações `user.name` e `user.email` estão com os valores que você informou:
```
...
user.name=Seu Nome aqui
user.email=seuemail@email.com
...
```

## Usando de verdade
Agora que tudo está configurado e pronto, você pode começar a utilizar o Git e o Github de fato.

Existem inúmeras maneira de fazer isso, no entanto aqui mostrarei duas: 
- [Usando por linhas de comando](command_line.md)
- [Usando no VSCode](vscode.md)