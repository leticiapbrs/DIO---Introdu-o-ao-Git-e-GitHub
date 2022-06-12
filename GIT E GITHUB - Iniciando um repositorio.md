# GIT E GITHUB - INICIANDO UM REPOSITÓRIO



#### Nomenclatura 

​	1. **Branch**: é o nome dado a uma versão (ramificação) do projeto.  Possibilita o gerenciamento de múltiplas alterações que estão acontecendo simultaneamente.

​	2. **Merge**: para unir as modificações feitas em um branch ao código original, utiliza-se o comando merge. Com esta funcionalidade, todas as alterações feitas em cópias manipuláveis são inseridas, após aprovadas, no código-fonte original sem complicações.

3. **Fork:** quando um profissional desenvolvedor precisa começar a trabalhar em um projeto, seu primeiro passo é copiar este repositório para a sua máquina. Este processo é realizado pelo comando **fork**. O fork também é uma funcionalidade útil quando um membro da equipe precisa pegar um código público para manuseá-lo em um editor de código local ou interno.

------



#### Criando um repositório

 Cria um novo repositório local com o nome de projeto especificado

* $ git init 

Ver situação dos arquivos no repositório Git

- $ git status

------



#### Adicionando itens

Adiciona um arquivo à área de de preparação para que possa ser inserido em commits (staged): 

- $ git add [arquivo] 
- $ git add * ou git add . (adiciona todos os arquivos)

Desta forma, informamos ao projeto os arquivos que estão sendo gerenciados pelo Git e que possivelmente vão para nosso servidor.

------



#### Gravando arquivos no repositório (COMMIT)

Quando executamos um Commit, estamos de fato, nos comprometendo com todas as mudanças que fizemos no código.

- **Comentários**

  Embora alguns lugares permitam que você realize commits sem informar nada, o ideal é que você sempre informe o que foi modificado.

  Desta forma, o primeiro comando de commit ficará assim:

 ```
  git commit -m "Comentário sobre as alterações"
 ```

 		Neste momento, localmente está tudo pronto, e já podemos enviar nossas informações para o servidor.

------



#### **Alterando arquivos**

Após o commit, quando ocorrem alterações no arquivo e executamos *git status*, pode-se observar que há uma nova mudança para ser rastreada. Sendo necessário, o uso dos comandos novamente.

**Verificando alterações**

Para verificar o histórico das alterações gravadas no repositório ou o acesso de uma versão específica podemos executar o comando *git log*.

#### **Desfazendo commits **

**Git revert**

Em alguns momentos talvez seja necessário desfazer algum commit, para isso podemos utilizar o comando git revert. 

* **$ git log** Esse comando irá mostrar o histórico de commits. Nesse histórico copie o código referente ao commit que quer desfazer. 
* **$ git revert codigo_commit.** Assim que executar esse comando abrirá um editor  para confirmar que quer reverter o commit e qual mensagem deseja que apareça nessa reversão. Com isso o commit será revertido mantendo o histórico.
* **$ git push origin master** Esse comando fará com que este revert apareça no histórico de commits no Github. 

**Git reset**

Para voltar arquivos que já estão em um commit utilizamos o comando.

- git reset --**soft** id_commit_anterior - volta ao commit anterior mantendo as alterações em *staged* - antes do commit.

- git reset --**mixed** id_commit_anterior - volta ao commit anterior em *modified*.
- git reset --**hard** id_commit_anterior - remove todas as alterações, *unmodified*. todas as alterações são descartadas.



#### **Diferença entre git revert e git reset**

O **git revert** reverte as alterações de um commit antigo e cria um commit novo com os dados revertidos, ou seja, ele não modifica nenhum dos commits anteriores. O **git reset** modifica o histórico de commits, a fingir que um commit nunca aconteceu.



**Outros códigos:**

Para ver as modificações em um arquivo utilizamos o comando

```
git diff nome_arquivo
```

Para voltar arquivos staged utilizamos o comando

```
git reset HEAD nome_arquivo
```

------



#### Enviando os Arquivos

Primeiramente devemos apontar o repositório local para o GitHub. Estando no diretório desejado, executar o comando *git remote*

```
git remote add origin https://github.com/usergithub/nomedoprojeto.git
```

Os envios pelo Git são sempre feitos pelo comando **push** e devemos sempre especificar uma Branch para origem do mesmo.

Como neste caso estamos trabalhando na Branch Master, vamos especifica-la como padrão no envio, utilizando o seguinte comando.

```
git push -u origin master
ou
git push origin main
```



#### Atualizando os arquivos locais

- **Pull**: ao contrário do push, este comando traz um arquivo do repositório remoto para o repositório local.

  

#### Obtendo projetos do GitHub

Para baixar um projeto disponível no GitHub, utiliza-se o comando *git clone*.

```
git clone [url]
```



------

#### Branches

Branches criam uma linha alternativa para trabalharmos em um projeto paralelamente a sua linha original.

- Para **criar uma nova branch** 

```
git branch nome_branch
```

- Para **alterar de branch** 

```
git checkout nome_branch
```

- Para **listar branches** existentes

```
git branch 
```

- Para **unir duas branches** 

```
git merge nome_branch
```

- Para **deletar uma branch**

```
git branch -d nome_branch
```

- Para **consultar commits** visualizando as ramificações

```
git log --graph
```



#### Diferenças entre git merge e git rebase

O git merge e o git rebase possuem a mesma função: mesclar alterações de duas branches diferentes.

O merge, na maioria das vezes, gera um novo commit, o que pode tornar o histórico mais confuso, mas nunca o reescreve.

```
git merge nome_branch
```

 Já o rebase, torna o histórico linear e simples, porém alguns commits são reescritos - função mais destrutiva. Modifica o histórico, coloca os commits em ordem cronológica, a alteração da estrutura impede a realizacao de um push, sendo possivel apenas forçadamente --force (não recomendado).

```
git rebase nome_branch
```

------



#### Git checkout

git checkout é uma forma de alternar entre versões de arquivos, commits ou branches. Existem diferentes formas de usar, mas seus dois principais usos são: trocar de branch ou restaurar arquivos.

- Para **restaurar arquivos**

```
git checkout nome_arquivo
```

- Para **trocar de branch**

```
git checkout nome_branch
```

------



#### Git stash

O git stash arquiva as alterações feitas durante um determinado período, para que se possa trabalhar em outra coisa, depois voltar e fazer a alteração mais tarde. O stashing é útil quando é necessário alternar com rapidez o contexto e trabalhar em outra coisa, mas está no meio da alteração de código e não está pronto para fazer commit.

- **Armazenar** uma alteração temporária

```
git stash
git stash --include-untracked
```

- **Aplicar** uma alteração temporária

```
git stash apply
```

- **Listar** alterações temporárias

```
git stash list
```

- **Limpar** uma alteração temporária

```
git stash clear
```



#### .gitignore

Nem todos os arquivos precisam ser enviados para o repositório remoto.


#### Pull Request (ou PR)

Utilizado para solicitar o merge de uma branch em outra branch no nosso repositório remoto.

