# Aula inicial: Apresentação e GIT

Gravação: https://www.youtube.com/watch?v=d4EyQMg5m-U

## Requisitos
1. O primeiro passo é ter o programa GIT instalado antes da aula link: https://git-scm.com/download/win

2. O segundo passo é criar uma conta no Github link: https://github.com/join

3. Depois de criar a conta no Github, adicione uma chave SSH ao seu perfil.
    
    3.1.  Como criar a chave :https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

    3.2. Como adicionar ao perfil: https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

4. Mandar no Discord no canal #novos-alunos o nome do seu usuário do Github
Exemplo: Olá! Meu nome é Thiago moro em Berlim e atualmente trabalho com X O usuario do githuib é trennepohl. 

## Conteúdo da Aula

### O que é Git?

Git é um sistema de versionamento distribuído criado pelo mesmo criador do Linux o Linus Torvalds e é amplamente utilizado na indústria de desenvolvimento de software.

Mais em [Guia de git da Atlassian](https://www.atlassian.com/br/git/tutorials/what-is-git)

### Abordagem
Então a proposta desta aula é a seguinte, aprender Git com uma abordagem prática.

Eu adicionei vocês como contribuidores deste repositório privado e o exercício é adicionar o nome de vocês no arquivo README.md como contribuidores. 

O fluxo que a gente vai seguir é esse:
- Clonar o repositório
- Criar um novo branch
- Modificar o arquivo
- Fazer um commit
- Fazer o push
- Abrir um pull request

## Conceitos

### Repositório
Repositório é a pasta em que se encontram os arquivos a serem rastreados pelo git.
É possível tranformar quase qualquer pasta em seu computador em um repositório do Git, basta que através do terminal você digite o comando:

```
git init
```

Não se esqueça que é necessário que o comando seja executado dentro da pasta em que você quer transformar em um repositório.

Exemplo:

```
mkdir exemplo-repositorio
cd exemplo-repositorio
git init
```

Os comando acima irão realizar as seguintes operações:
- Criar uma pasta chamada exemplo-repositorio
- Mudar o diretório atual para `exemplo-repositorio`
- Initializar o git

### Branch

Um repositório Git possuí `branches` ou em pt-br ramificações, quando o repositório é criado pela primeira vez o branch inicial é o `main`. De forma resumida um `branch` armazena a linha do tempo de modificações feitas, sendo a branch `main` a principal linha do tempo.

Branches é uma das melhores funcionalidades do Git em termos de colaboração e isolamento, pois permite ao desenvolvedor(a) modificar o código fonte em paralelo com a main branch e mais tarde realizar uma operação de `merge` das modificações feitas na branch paralela para a branch principal.

Para criar uma nova banch a partir da `main` branch basta executar:

```
git checkout -b nome-da-branch
```

Consulte este [link](https://git-scm.com/book/pt-br/v2/Branches-no-Git-Branches-em-poucas-palavras) para mais informações sobre branches

### Commit

Ao adicionar um novo arquivo ou realizar modificações em arquivos já rastreados pelo Git é o suficiente para "Gravar" suas alterações na arvore de mudanças. Por isso é necessário realizar um commit.

Exemplo:
```
touch novo-arquivo.txt
git status
```

Os comandos acima realizam as seguintes ações:
- Cria um novo arquivo chamado `novo-arquivo.txt`
- Mostra o status de alterações do repositório

Após executar os comando acima, o Git provavelmente deverá lhe mostrar algo assim:

```
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        novo-arquivo.txt
```

A saída do terminal acima, indica que há um arquivo não rastreado e que é necessário usar o comando `git add <arquivo>` para incluir às mudanças a serem gravadas no Git.

Então usando o comando abaixo, nós instruímos o git a rastrear este arquivo

```
git add novo-arquivo.txt
git status
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   novo-arquivo.txt
```

Agora que todos os arquivos modificados, ou novos que antes não estavam rastreados, agora estão prontos para serem persistidos na árvore de mudanças.

Para finalizar o commit, o comando abaixo pode ser executado
```
git commit -m "Adicionado um arquivo novo para a funcionalidade X"
```

A partir de agora a mudança está salva em seu branch local e pronta para ser enviada ao servidor remoto, no caso o Github.

Mais detalhes sobre commits [aqui](https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio)

[Boas práticas de mensagens de commits](https://github.com/Paiusco/commit-message-rules)

### Push

O comando push envia as mudanças locais para o Github ou outra plataforma que você esteja utilizando.

```
git push origin <nome-do-seu-branch>
```


### Pull request

https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests


## Exercícios
Cada aluno deverá criar um pull request com:
- Uma pasta com seu nome, a qual os exercícios serão salvos semana a semana
- Uma proposta de sistema a ser desenvolvido durante o curso.

### Template proposta

**Nome**: Sistema de video aulas

**Breve descrição**: Um sistema colaborativo de EAD para o ensino de T.I

**Funcionalidades**:
  - Cadastro de usuário
  - Upload de vídeos
  - Contabilizador de visualizações
  - Sistema de "Achievements" para cursos finalizados






 


