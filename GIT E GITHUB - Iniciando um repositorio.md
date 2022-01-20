# GIT E GITHUB - INICIANDO UM REPOSITÓRIO



#### Nomenclatura 

​	1. **Branch**: é o nome dado a uma versão (ramificação) do projeto.  Possibilita o gerenciamento de múltiplas alterações que estão acontecendo simultaneamente.

​	2. **Merge**: para unir as modificações feitas em um branch ao código original, utiliza-se o comando merge. Com esta funcionalidade, todas as alterações feitas em cópias manipuláveis são inseridas, após aprovadas, no código-fonte original sem complicações.

3. **Fork:** quando um profissional desenvolvedor precisa começar a trabalhar em um projeto, seu primeiro passo é copiar este repositório para a sua máquina. Este processo é realizado pelo comando **fork**. O fork também é uma funcionalidade útil quando um membro da equipe precisa pegar um código público para manuseá-lo em um editor de código local ou interno.



#### Criando um repositório

 Cria um novo repositório local com o nome de projeto especificado

* $ git init 

Ver situação dos arquivos no repositório Git

- $ git status



#### Adicionando itens

Adiciona um arquivo à área de de preparação para que possa ser inserido em commits (staged): 

- $ git add [arquivo] 
- $ git add * ou git add . (adiciona todos os arquivos)

Desta forma, informamos ao projeto os arquivos que estão sendo gerenciados pelo Git e que possivelmente vão para nosso servidor.



#### Gravando arquivos no repositório (COMMIT)

Quando executamos um Commit, estamos de fato, nos comprometendo com todas as mudanças que fizemos no código.

- **Comentários**

  Embora alguns lugares permitam que você realize commits sem informar nada, o ideal é que você sempre informe o que foi modificado.

  Desta forma, o primeiro comando de commit ficará assim:

 ```
  git commit -m "Comentário sobre as alterações"
 ```

 		Neste momento, localmente está tudo pronto, e já podemos enviar nossas informações para o servidor.


- **Alterando arquivos**

  Após o commit, quando ocorrem alterações no arquivo e executamos *git status*, pode-se observar que há uma nova mudança para ser rastreada. Sendo necessário, o uso dos comandos novamente.

- **Verificando alterações**

  Para verificar o histórico das alterações gravadas no repositório ou o acesso de uma versão específica podemos executar o comando git log.

- **Desfazendo commits**

  Em alguns momentos talvez seja necessário desfazer algum commit, por exemplo, se você fez um commit de uma coisa errada, que não era pra ter feito. 

  * **$ git log** Esse comando irá mostrar o histórico de commits. Nesse histórico copie o código referente ao commit que quer desfazer. 
  * **$ git revert codigodocommit.** Assim que executar esse comando abrirá um editor  para confirmar que quer reverter o commit e qual mensagem deseja que apareça nessa reversão. Com isso o commit será revertido.
  * **$ git push origin master** Esse comando fará com que o revert apareça no histórico de commits no Github. 



#### Enviando os Arquivos

Primeiramente devemos apontar o repositório local para o GitHub. Estando no diretório desejado, executar o comando *git remote*

```
git remote add origin https://github.com/usergithub/nomedoprojeto.git
```

Os envios pelo Git são sempre feitos pelo comando **push** e devemos sempre especificar uma Branch para origem do mesmo.

Como neste caso estamos trabalhando na Branch Master, vamos especifica-la como padrão no envio, utilizando o seguinte comando.

```
git push -u origin master
```



#### Atualizando os arquivos locais

- **Pull**: ao contrário do push, este comando traz um arquivo do repositório remoto para o repositório local.

  

#### Obtendo projetos do GitHub

Para baixar um projeto disponível no GitHub, utiliza-se o comando *git clone*.

```
git clone [url]
```

