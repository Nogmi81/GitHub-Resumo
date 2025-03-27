# Principais Comandos Git

Este guia rápido apresenta os comandos Git mais utilizados, categorizados para fácil referência.

## Configuração

* `git config user.name`: Define o nome de usuário global para commits.
* `git config --global user.email "seuemail@exemplo.com"`: Define o e-mail global para commits.

## Verificar Usuário

* `git config --global user.name "Seu Nome"`: Para verificar o nome do usuário
* `git config user.email`: Para verificar o e-mail do usuário
* `git config --list`: Para verificar todas as configurações do Git no sistema (incluindo o nome e e-mail)

## Inicialização e Clonagem

* `git init`: Inicializa um novo repositório Git no diretório atual.
* `git clone <URL_do_repositório>`: Clona um repositório Git existente para um novo diretório.

## Alterações e Commits

* `git status`: Exibe o estado das alterações no diretório de trabalho e na área de preparação.
* `git add <arquivo>`: Adiciona um arquivo à área de preparação para o próximo commit.
* `git add .`: Adiciona todas as alterações do diretório atual à área de preparação.
* `git commit -m "Mensagem do commit"`: Cria um novo commit com as alterações da área de preparação.
* `git commit --amend`: Permite editar o último commit.

## Branches

* `git branch`: Lista todos os branches no repositório local.
* `git branch <nome_do_branch>`: Cria um novo branch.
* `git checkout <nome_do_branch>`: Muda para o branch especificado.
* `git merge <nome_do_branch>`: Mescla as alterações do branch especificado no branch atual.
* `git branch -d <nome_do_branch>`: Exclui o branch especificado.

## Remotos

* `git remote add origin <URL_do_repositório>`: Adiciona um repositório remoto chamado "origin".
* `git push origin <nome_do_branch>`: Envia os commits locais para o branch especificado no repositório remoto.
* `git pull origin <nome_do_branch>`: Obtém as alterações do branch especificado no repositório remoto e mescla no branch local.
* `git fetch`: Baixa todos os históricos do repositório remoto, mas não mescla as alterações.

## Histórico e Inspeção

* `git log`: Exibe o histórico de commits.
* `git diff`: Mostra as diferenças entre o diretório de trabalho e a área de preparação.
* `git diff --cached`: Mostra as diferenças entre a área de preparação e o último commit.

## Desfazendo Alterações

* `git reset --hard <commit>`: Retorna o repositório para o estado do commit especificado, descartando todas as alterações posteriores.
* `git revert <commit>`: Cria um novo commit que desfaz as alterações do commit especificado.
* `git stash`: Salva temporariamente as alterações não commitadas.
* `git stash pop`: Aplica as alterações salvas pelo `git stash` e remove-as da lista de stashes.

## Outros Comandos Úteis

* `git rm <arquivo>`: Remove um arquivo do diretório de trabalho e da área de preparação.
* `git mv <arquivo_antigo> <arquivo_novo>`: Renomeia um arquivo.

## Recursos Adicionais

* Documentação oficial do Git: https://git-scm.com/


Este README fornece uma visão geral dos comandos Git mais comuns. Para informações mais detalhadas e comandos avançados, consulte a documentação oficial do Git.
