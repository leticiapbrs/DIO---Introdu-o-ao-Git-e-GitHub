# GIT E GITHUB - INSTALAÇÃO



#### O que é versionamento de código?

Relacionado com a criação de algo novo ou alterações em algo que já existe. Durante o versionamento de códigos é possível a gestão de mudanças, registro de quaisquer alterações feitas em um código e a possibilidade de retorno a versões anteriores. 

#### O que é Git?

O Git é um sistema de controle de versão criado pelo ***Linus Torvalds***, criador do Linux, durante a construção do mesmo. O Git é um *Sistema de Controle de Versões Distribuído* — ou DVCS.



#### O que é GitHub?

O [GitHub](https://github.com/) é a plataforma que torna possível armazenarmos online nossos códigos, criar repositórios, colaborar com softwares *open source*. Além disso, o GitHub é conhecido por ser um portfólio para desenvolvedores.



### Instalação do Git

Embora possamos realizar todas as tarefas que precisamos diretamente pelo GitHub, com sua interface visual, é muito comum utilizarmos a famosa interface de linha de comando (CLI), sendo esta muito completa no Git.

Página oficial do Git para download: https://git-scm.com

​	Serão instalados alguns programas sendo o mais importante o Git Bash.

*Windows* - instalação simples, escolha das opções padrão.

_Linux - comandos necessários no terminal para instalação_

```
 Debian/Ubuntu
$ sudo apt-get install git-all

 Fedora
$ sudo yum install git-all
```

Para verificar qual a versão instalada: _git --version_.



#### Configuração

Necessário configurar nossa conta para trabalhar com o Git, isso é feito utilizando o comando **git config**, onde informamos nosso user e email.

Configurações globais

```
git config --global user.name "Digite seu nome"
git config --global user.email "Digite seu email"
```

** ideal serem os mesmos usados no GitHub.







