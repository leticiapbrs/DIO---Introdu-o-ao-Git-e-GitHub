# Boas práticas ao escrever commits

[TOC]

##  Porque utilizar Conventional Commits

- Criação automatizada de CHANGELOGs.
- Determinar automaticamente um aumento de versionamento semântico.
- Comunicar a natureza das mudanças para colegas de equipe, o público e outras partes interessadas.
- Facilitar a contribuição de outras pessoas em seus projetos, permitindo que explorem um histórico de commits mais estruturado.



## A mensagem do commit deve ser estruturada da seguinte forma:

```
<tipo>[escopo opcional]: <descrição>

[corpo opcional]

[rodapé opcional]
```



## Tipo:

1. **fix:** um commit do *tipo* `fix` soluciona um problema na sua base de código.

2. **feat:** um commit do *tipo* `feat` inclui um novo recurso na sua base de código.

3. **BREAKING CHANGE:** um commit que contém o texto `BREAKING CHANGE:`, no começo do texto do corpo opcional ou do rodapé opcional, inclui uma modificação que quebra a compatibilidade da API. Uma BREAKING CHANGE pode fazer parte de commits de qualquer *tipo*. 

   

   Outros tipos além do *fix:* e *feat:* são permitidos, como, por exemplo: ⁣

   - **chore:** Mudanças de configuração ou de código que não entra em produção;
   - **ci:** Alteração em algum arquivo de CI do projeto;
   - **docs:** Mudanças na documentação;
   - **style:** Alteração apenas no estilo do código, sem mudança de algoritmo;
   - **refactor:** Refatoração de determinado bloco de código;
   - **perf:** Alterações que impactam o desempenho da aplicação;
   - **test**: Mudanças na estrutura ou na forma de testar o projeto.
   - **improvement**: para commits que melhoram uma implementação atual sem adicionar um novo recurso ou consertar um bug. 

   

## Escopo opcional:

​	Um escopo pode ser adicionado ao tipo do commit, devendo consistir em um substantivo que forneça informações contextuais adicionais e está contido entre parênteses, por exemplo `feat(parser): adiciona capacidade de interpretar arrays`.  



## Descrição:

​	Uma descrição deve existir após o prefixo tipo/escopo. 

​	A descrição é um breve resumo das alterações de código, por exemplo, *fix: problema na interpretação do array quando uma string tem vários espaços.*



## Corpo opcional: 

​	Um corpo de mensagem de commit mais longo pode ser fornecido após a descrição curta, explicando em mais detalhes e  apresentando mais contexto sobre o
problema  tratado, devendo começar depois de uma linha em branco após a descrição. 

​	No corpo deve ser escrito o porquê daquela alteração, sua motivação e contexto. Não é necessário dizer como o problema foi corrigido, qual arquivo foi alterado, etc.

​	Além disso, o corpo pode ser utilizado para explicar como a alteração funcionava antes, e como ele irá funcionar a partir de agora, sempre focando no porquê aquela alteração foi realizada, não como ela foi feita, pois as alterações de código que podem ser consultadas.


## Rodapé opcional:

​	Um rodapé de uma ou mais linhas pode ser fornecido depois de uma linha em branco após o corpo. 

​	O rodapé deve conter informações adicionais sobre o commit, por exemplo, pull-requests, revisores, modificações que quebram a compatibilidade, com uma informação adicional por linha.



## Extras

1. Um `!` PODE ser acrescentado antes do `:` no prefixo tipo/escopo, para chamar a atenção para modificações que quebram a compatibilidade. `BREAKING CHANGE: description` também DEVE ser incluído no corpo ou no rodapé, junto com o `!` no prefixo.

Exemplo:

```text
chore!: remove suporte ao Node 14

Para suportar novas funcionalidades que vão
agregar mais desempenho a aplicação como o
`Promises.any` estamos subindo o requerimento
mínimo do projeto.

BREAKING CHANGE: a versão minima do Node agora é a 16.
```

3. O corpo do commit, deve se limitar a no máximo de 72 caracteres por linha.
3. Limite o resumo do commit a 50 caracteres.
3. Não termine o resumo com um ponto final.
3. Separe o resumo e o corpo do commit com uma linha em branco.
7. Use linguagem imperativa no resumo do commit.  Como dica, a mensagem de commit deve se encaixar na seguinte frase: *“Quando aplicado, o que esse commit faz?”*



## Referências:

- [Boas práticas ao escrever commits no Git](https://instruct.com.br/publicacoes/boas-praticas-ao-escrever-commits-no-git/)
- ["Conventional Commits"](https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/)
- [Escrevendo commits melhores no Git](https://blog.lfrigodesouza.net/2020/12/09/escrevendo-commits-melhores-no-git/) 



