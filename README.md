# Meu primeiro projeto em Django 🦄

Este projeto foi desenvolvido seguindo o [tutorial Django Girls](https://legacy.gitbook.com/@djangogirls)

>Este documento não tem a intenção de demonstrar o passo-a-passo do desenvolvimento do projeto, caso tenha interesse em desenvolver sua própria aplicação, clique no link referenciado em 'tutorial Django Girls' acima. :wink:

## <a name="section0"></a> <h3>Ferramentas utilizadas no desenvolvimento do projeto</h3>

Nesta seção eu cito as ferramentas e plataformas que utilizei para o desenvolvimento das etapas do projeto:

#### Editor de Texto

O editor que você for utilizar vai de seu gosto, o que eu utilizei neste projeto foi o [Atom](https://atom.io/), mas existem muitos editores por ai que podem te agradar tanto quanto e te auxiliar no que for fazer.

>Atom: é um editor de código aberto desenvolvido pelo Github sob a licença do MIT, disponivel para os sistemas Linux, MacOs e Windows.

#### Controle de versões OpenSource

O [Git](https://git-scm.com/) é um pré requisito a ser instalado no seu computador para realizar todas as etapas do tutorial, mas você pode utilizar qualquer outro versionador de arquivo, isso não vai ter problema.

>Git: é um sistema de controle de versões distribuído, usado principalmente no desenvolvimento de software, mas pode ser usado para registrar o histórico de edições de qualquer tipo de arquivo.

#### Linguagem de Programação

O tutorial segue as origens do framework Django, utilizando a linguagem [Python](https://www.python.org/) em sua versão mais atual para que tudo saia como planejado.

>Python é uma linguagem de programação de alto nível, interpretada, de script, imperativa, orientada a objetos, funcional, de tipagem dinâmica e forte.

## <a name="section4-1"></a> <h4> :memo: Erros e Correções</h4>

Durante a criação do repósitório eu alterei o nome do projeto e isso afetou o espelhamento dos arquivos que estavam no meu computador para o repositório `my-first-blog`, os erros e as correções que eu realizei foram as seguintes..

Apesar de confirmar a existencia do repositório no meu github, o git não executava o comando `git push -u origin master`que permite alterar o master para qualquer ramo (branch) desejado, enviando suas alterações para ele.

  ###### Confirmação do prompt a respeito da existência do repositório
  ```
  User@User MINGW64 ~/djangogirls (master)
  $ git remote add origin https://github.com/user-example/my-first-blog.git
  fatal: remote origin already exists.
  ```
  ###### Erro para alterar o branch no repositório informado
  ```
  User@User MINGW64 ~/djangogirls (master)
  $ git push -u origin master
  remote: Repository not found.
  fatal: repository 'https://github.com/user-example/my-first-blog.git/' not found
  ```
  ###### Continuação do erro ao executar o comando `git push -u origin master` novamente
  ```
  User@User MINGW64 ~/djangogirls (master)
  $ git push -u origin master
  To https://github.com/user-example/my-first-blog.git
   ! [rejected]        master -> master (fetch first)
  error: failed to push some refs to 'https://github.com/user-example/my-first-blog.git'
  hint: Updates were rejected because the remote contains work that you do
  hint: not have locally. This is usually caused by another repository pushing
  hint: to the same ref. You may want to first integrate the remote changes
  hint: (e.g., 'git pull ...') before pushing again.
  hint: See the 'Note about fast-forwards' in 'git push --help' for details.

  ```
  Caso tenha esbarrado neste mesmo erro execute os seguintes comandos, que me ajudaram a resolver o problema:
  >Antes de executar cada comando aguarde a aparição do cifrão `$`, a ausência dele mostra que o comando informado ainda esta sendo executado pelo prompt.
  ```
  $ git fetch origin master:tmp
  $ git rebase tmp
  $ git push origin HEAD:master
  $ git branch -D tmp
  ```

