# Git, GitHub e linha de comando

* [Git?](#git)
* [GitHub?](#github)
* [O que é linha de comando?](#o-que-é-linha-de-comando)
* [Começando com o Git](#comecando-com-o-git)
* [Instalando/verificando se o Git está instalado](#instalandoverificando-se-o-git-está-instalado)
* [Pra não esquecer:](#pra-nao-esquecer)
* [Branch](#branch)
* [Fork](#fork)
* [Pull request](#pull-request)

***

## Git

### O que é Git?

Git é uma ferramenta de controle de versão com foco em velocidade e integridade de dados. Com ele, podemos desenvolver projetos colaborativos, em que outras pessoas podem trabalhar simultaneamente no mesmo código sem riscos de perdas.

Conseguimos ter um histórico de tudo que foi alterado nos arquivos ao longo do tempo, além de mostrar quem foi o autor da mudança.

Em linhas gerais, o Git promove:

* **Organização**: O Git cria uma linha do tempo com tudo que aconteceu desde o início do projeto. Tudo que foi adicionado, removido, e quem foi o autor.
* **Colaboração**: Facilita o trabalho em equipe (entender o que foi feito, onde parou, quem fez o que).
* **Segurança**:  Se algo der errado, você pode resgatar uma versão anterior, além  de ter o seu projeto salvo em um lugar seguro.

***

## Github

### O que é GitHub?

Github é um site que permite que você hospede seus repositórios (projetos). Ele integra a ferramenta de versionamento Git.

Outras pessoas podem ver seus projetos, baixá-los e consultar o seu código. E você também pode ver o código dos outros, participar de projetos e seguir outros desenvolvedores.

Funciona como uma espécie de rede social muito utilizada principalmente por desenvolvedores, onde você pode publicar e compartilhar todos os seus projetos pessoais e particulares, além de colaborar com projetos de pessoas e empresas de todo o mundo.

Existem outros exemplos, como GitLab e Bitbucket.

Ou seja, o Github ajuda em:

* **Portfólio** - É um site seguro para guardar e mostrar seus projetos. É comum as empresas pedirem apenas seu GitHub antes de uma entrevista de emprego.
* **Organização** - Permite que todo mundo trabalhe no mesmo projeto (seja um projeto da sua empresa ou um Open Source).
* **Ferramentas** - Porque oferece funcionalidades extras ao git, como interface visual, documentação, bug tracking, feature requests, pull requests, etc.

***

## Linha de comando (cmd)
### O que é linha de comando?

É aquela tela preta que aparece nos filmes, normalmente com alguém hackeando algum sistema.
Mexer com o terminal assusta um pouco porque ele é abstrato.

Sabe quando a gente arrasta arquivos para uma pasta ou cria uma pasta nova? No terminal você faz tudo isso também, mas sem interface gráfica. Inserimos comandos, e ele executa.

***

### Comandos básicos do terminal

Esses comandos servem para para listar arquivos e navegar entre pastas dentro do computador.

No Windows:

```
dir - lista (ele traz uma lista de tudo o que está naquela pasta - documentos, outras pastas, etc) 
cd nome-da-pasta - change directory (use para se locomover entre as pastas)
cd .. - volta uma pasta acima
mkdir nome-do-diretorio - cria diretório/pasta 
dir > nome.txt nome-do-arquivo.extensão - criar arquivo 
cls – limpa o terminal

```

No Linux:

```
ls – lista arquivos e diretórios
cd .. - volta uma pasta acima
cd nome-da-pasta - para entrar em uma pasta (você precisa conseguir enxergar ela quando listar os arquivos)
pwd – mostra qual é o diretório atual
mkdir nome-do-diretorio – cria um diretório
clear – limpa a tela

```

***

### Começando com o Git

Algumas palavras novas que vamos usar com o Git/GitHub

* Repositório: É um espaço digital aonde o seu projeto vai ser salvo. No seu computador ele é a pasta onde o seu projeto está salvo.

* Controle de versão: É a proposta básica do Git, um histórico de tudo o que aconteceu com o(s) arquivo(s) que você está trabalhando. Por exemplo, quando você salva um arquivo do Word no seu computador, você perde todas as versões anteriores, ficando somente com o conteúdo atual. Com o Git você tem todas as versões antigas dos arquivos.

* Commit: Quando você faz um commit com o Git, você está criando um controle de versão (histórico) daquele arquivo e criando uma etiqueta para facilitar o entendimento do que foi salvo naquele momento.

* Push: O push também serve para se comunicar entre a sua máquina e o repositório remoto. Esse comando faz uma cópia do repositório local e envia ele para o repositório remoto.

* Log - Este comando retornará uma listagem dos últimos commits com o hash de identificação, a data e também o usuário que foi responsável pelo commit.

***

### Instalando/verificando se o Git está instalado

Digite git status na linha de comando, e várias instruções e sugestões do git devem aparecer.
Comandos para usar uma vez na vida: (assim o git sabe quem está fazendo as alterações)

```
git config --global user.name “Maria Rita Casagrande"
git config --global user.email “mariarita@gmail.com”
```

Para remover o usuário
```
git config --global --unset-all user.name "Maria Rita Casagrande"
git config --global --unset-all user.email “mariarita@gmail.com”
```

***

#### Baixar um projeto que está hospedado no GitHub para a nossa máquina

1) Acessar o GitHub e criar uma conta gratuita.
**Importante:** utilizar um nome de usuário fácil de usar, pois essa url vai ser muito utilizada durante a vida profissional.

2) Acessar https://github.com/reprograma
3) Acessar o repositório `github`
4) Clicar no botão `Clone or download` e copiar a url https
4) Navegar até a pasta aonde você vai fazer o clone do projeto
5) `git clone url-que-vocês-copiaram`

***

#### Iniciar um projeto local e subir pro GitHub

1) Navegar pela linha de comando até a pasta desejada
2) Rodar o comando  git status. Provavelmente o Git não vai estar iniciado nessa pasta, então vamos rodar um comando para avisar para o Git começar a versionar essa pasta: `git init`
4) Criar um repositório no GitHub (colocar o nome do projeto de vocês)
5) Copiar a url do repositório (igual vocês fizeram no exemplo anterior)
6) `git add .` (para adicionar todos os arquivos de uma vez) ou `git add caminho-do-arquivo`
git `commit -m "Aqui você escreve uma mensagem que ajude quem estiver lendo a saber o que você adicionou/modificou nos arquivos"`
7) `git remote add origin url-que-voces-copiaram-do-github`
8) `git remote -v` (vai mostrar as urls, provavelmente duas)
9) `git push origin master`

Abrir o repositório no GitHub. Os arquivos que estavam na máquina de vocês agora devem estar salvos no GitHub 🎉
Agora uma cópia do trabalho de vocês até agora está salvo no GitHub, e o Git está monitorando essa pasta.
A partir de agora, sempre que vocês modficarem/adicionarem/removerem arquivos nessa pasta, o Git vai saber e  vai mostrar tudo o que foi modificado/adicionado/removido.

***

### Pra não esquecer:
* `git status` (para ver a lista de arquivos modificados)
* `git add .` (para adicionar todos os arquivos de uma vez) ou git add caminho-do-arquivo
* `git commit -m "Mensagem"` (cria um histórico daquele arquivo com uma etiqueta explicando o que foi feito)
* `git pull origin master` (o comando PULL pega a versão do arquivo que está no repositório remoto e baixa para sua máquina.
* `git push origin master` (envia as modificações para o repositório remoto)

***

### Branch
O git tem uma linha do tempo principal chamada master, que é branch base criada junto com cada repositório. Quando trabalhamos sozinhas em um repositório não tem problema trabalharmos sempre no master, mas quando começamos a trabalhar com outras pessoas em um projeto, surge a necessidade de ter uma cópia do projeto que seja livre de bugs e que esteja funcionando 100%. Essa cópia é o master.

A partir do código que está no master podemos gerar outras cópias para serem modificadas e depois devolvidas para o master.

Essas cópias são chamadas de branch.

Comando para criar um novo branch:
`git checkout -b nome-do-branch`

Comando para trocar de branch:
`git checkout nome-do-branch`

Comando para listar todos os branches locais:
`git branch`

***

### Fork

Um fork é uma cópia de um projeto de outra pessoa dentro do seu GitHub.

Normalmente você faz um fork de um projeto para fazer melhorias no código. Depois das melhorias feitas, você vai abrir um pull request para o dono do repositório, e se suas modificações forem aceitas, seu código vai ser 'mergeado' no código original.

***

### Pull request

Quando você faz um fork de um projeto, ou quando você trabalha em uma empresa com mais desenvolvedores, é normal que as demais pessoas envolvidas no projeto façam um review do seu código antes de ele ir pro master, afinal você pode ter cometido algum erro no desenvolvimento, ou alguma parte do seu código pode ser melhorada.

Um pull request é quando você quer fazer merge do seu código em outro branch, mas você precisa da autorização das outras pessoas envolvidas no projeto.

***