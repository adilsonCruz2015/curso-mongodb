# O que é MongoDb?

# MongoDB é um banco de dados de propósito geral, baseado em documentos, distribuído criado para desenvolvedores de aplicativos modernos e para a nuvem desta era.
# O [MongoDB] trabalha com os estados dos arquivos.


## Melhorias do [Git]

* Velocidade
* Design simples
* Suporte robusto a desenvolvimento não linear (milhares de branchs paralelos)
* Totalmente distribuído
* Capaz de lidar eficientemente com grandes projetos como o kernel do linux

## O que é o [Github]?

# Serviço de web compartilhado para projetos que utilizam o [Git] para versionamento


## Instalando o [Git]

* Ir para o Site (https://git-scm.com/download) escolher a versão conforme o sistema operacional.


## Configurar o [Git]

# o [Git] guarda minhas informações em 3 lugares:

* git config no sistema com um todo 
* git config do usuário (global)
* e o git config do projeto especifico daquele projeto

## Comandos [Git] para configurar as informações dos usuários.

```sh
$ git config --global user.name "meu nome" . Depois apertar a tecla enter.
```

```sh
$ git config --global user.email "meu e-mail" . Depois apertar a tecla enter.
```

## Configurar o editor padrão.

```sh
$ git config --global core.editor "passar o comando do editor sem as aspas dupla" . Depois apertar a tecla enter.
```
Caso vc não defima o editor o padrão é o Vi

## Caso você queira saber o valor que foi definido em alguma chave basta digitar o seguinte(s) comando(s).

## Para saber o nome do usuário:

```sh
$ git config user.name . Depois apertar a tecla enter.
```

## Para saber o e-mail:

```sh
$ git config user.email . Depois apertar a tecla enter.
```

## Para saber todas as informações:

```sh
$ git config --list . Depois apertar a tecla enter.
```

# Inicializar o [Git] nos projetos

* Criar uma pasta para o projeto.

```sh
$ mkdir  "nome do proijeto sem as aspas" . Depois apertar a tecla enter.
```

* entrar na pasta criada

```sh
$ cd  "nome do proijeto sem as aspas" . Depois apertar a tecla enter.
```

* Inicializar o repositório e ele fazr parte do eco sistema do [Git] digite o comando:

```sh
$ git init . Depois apertar a tecla enter.
```

## Ele é responsável por inicializar o respositório e ficar olhando as mudanças que ocorrem dentro do projeto.
 
```sh
$ ls -la . Depois apertar a tecla enter.
```

## Mostra o diretório .git

* entrar no diretório [Git]

```sh
$ cd  .git/ . Depois apertar a tecla enter.
```

## Ele mostra algumas pastas que são responsável por guardar as informações do repositório, qual é a branchs padrão que esta está, quais são as branchs existente no projeto,
descrição hooks que são gatilhos e outras informações de objetos e referencias.

## Voltar para o diretório do projeto

```sh
$ cd .. apertar a tecla enter.
```


# Ciclo de vida dos status dos Arquivos.

o [Git] separa em 4 estados bem definidos como os arquivos vão ser.

* untrackes:
momento em que o arquivo acabou de ser adicionado no repositório, mas inda não foi visto pelo [Git].

* unmodified:
momento em que o arquivo é adicionado no [Git]. Ou seja ele não foi modificado. Ele existe no [Git], mas não houve nehuma alterção.

* modified:
momento em que o arquivo recebe lguma alteração.

* staged:
momento em que o arquivo é alterado e jogado em uma área aonde vai ser criada a versão.

Momento em que o arquivo vai ficar la sendo avisado. No momento em que a versão for fechada leve esses arquivo. E assim que o commit for efetuado, é criado um rash e todos os
arquivos voltam para o estado unmodified.


# Comando para listar arquivos no [Git]

```sh
$ ls  apertar a tecla enter.
```

# Comandos [Git]

```sh
$ git status  apertar a tecla enter.
```

Reporta como esta meu repositório nesse momento.

Adicionar um arquivo no [Git]

```sh
$ git add "nome do arquivo sem as aspas"  apertar a tecla enter.
```

Commit de um arquivo no [Git]

```sh
$ git commit -m  "mensagem"  apertar a tecla enter.
```

Log

```sh
$ git log  apertar a tecla enter.
```

```sh
$ git log --decorate  apertar a tecla enter.
```

```sh
$ git log --author="nome"  apertar a tecla enter.
```

```sh
$ git shortlog  apertar a tecla enter.
```

```sh
$ git shortlog -sn  apertar a tecla enter.
```

```sh
$ git log --graph  apertar a tecla enter.
```

```sh
$ git show "rash sem as aspas"  apertar a tecla enter.
```

```sh
$ git diff  apertar a tecla enter.
```

Mostra a alteração que foi adicionada

```sh
$ git diff --name-only  apertar a tecla enter.
```

Mostra somente o nome do arquivo que foi modificado.


```sh
$ git commit -am "descrição" apertar a tecla enter.
```
Adiciona todos os arquivo adicionado no [Git]


```sh
$ git checkout + nome do arquivo. apertar a tecla enter.
```
Com esse comando ele volta o arquivo para antes da alteração.


```sh
$ git reset HEAD + nome do arquivo apertar a tecla enter.
```

Isso sera usado se o arquivo ja estiver no staged.
HEAD diz ao ponteiro aonde estou. Diz que quer remover do staged.
Com esse comando ele tira do staged.

Depois que o arquivo estiver fora do staged ai sim digitar.

```sh
$ git checkout + nome do arquivo. apertar a tecla enter.
```
Agora sim foi desfeito.

```sh
git clone git@github.com:adilsonCruz2015/curso-git-basico.git + nome de sua preferência.
```

Clonar um repositório.


Caso tenha feito o commit, e queria reverter digite o comando.


O [Git] reset tem 3 comandos:

* --soft vai pegar as minhas modificações  e voltar o commit que foi feito. O arquivo vai para o staged pronto para ser comitado de novo.
* --mixed ele vai matar o commit, vai voltar os arquivos antes do staged ou seja modified.  
* --hard ignora a existencia desse commit e tudo o que foi feito nele.

```sh
$ git reset --soft + a rash. não a rah atual e sim a anterior. 
```

```sh
$ git reset --mixed + a rash. não a rah atual e sim a anterior.
```

```sh
$ git reset --hard + a rash. não a rah atual e sim a anterior.
```

# Criando uma branchs

```sh
$ git checkout -b + nome da branchs
```

```sh
$ git branch -a
```

Lista as branch


```sh
$ git checkout + nome da branch
```

Seleciona a branch

```sh
$ git branch -d + nome da branch
```

Remover uma branch local

```sh
$ git push origin --delete nome da branck
```
Remover uma branch remoto

```sh
$ git merge + nome da branch
```

Merge

```sh
$ git rebase + nome da branch
```

Rebase


```sh
$ git stash
```
Guarda as alterações em um lugar especifico para ser usado depois.


```sh
$ git stash apply
```

Aplica as mudanças que eu tinha guardado.


```sh
$ git stash list
```

Mostra todos os stash que eu estou fazendo.


```sh
$ git stash clear
```

Limpa tudo que eu tiver no stash.


## Criando Alias

```sh
$ git config --global alias.s + o nome do comando por exemplo Status```




## Criando Tags

```sh
$ git tag -a 1.0.0 -m "mensagem"
```

Subir a minha tag

```sh
$ git push origin master --tags
```


```sh
$ git revert + a rash
```

Reverter o commit.

```sh
$ git tag -d + a tag
```

Remove uma tag local

```sh
$ git push origin : + a tag que queira apagar
```
Remove uma tag remote

```sh
$ git push origin : + o nome da branch
```
Remove uma branch remote

# Gitignore

[Git] (https://git-scm.com/docs/gitignore)

[Github] (https://github.com/github/gitignore)


# Criando um repositório no [Github]

Gerando uma nova chave SSH para o [Github]

(https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)


# Gerando a chave SSH

```sh
ssh-keygen -t rsa -b 4096 -C "e-mail do github"
```

# Enviar um repositório existente a partir da linha de comando

```sh
git push -u origin master
```

[MongoDB]: https://www.mongodb.com/pt-br
[Github]: https://github.com/
