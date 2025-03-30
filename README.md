# Principais Comandos Git

Este guia rápido apresenta os comandos Git mais utilizados, categorizados para fácil referência.

## Configuração

* `git config user.name`: Define o nome de usuário global para commits.
* `git config --global user.email "seuemail@exemplo.com"`: Define o e-mail global para commits.

## Verificar Configuração

* `git config --global user.name "Seu Nome"`: Para verificar o nome do usuário
* `git config user.email`: Para verificar o e-mail do usuário
* `git config --list`: Para verificar todas as configurações do Git no sistema (incluindo o nome e e-mail)

## Inicialização e Clonagem

* `git init`: Inicializa um novo repositório Git no diretório atual. Com esse comando o git criar a pasta oculta .git
* `git clone <URL_do_repositório>`: Clona um repositório Git existente para um novo diretório.

Qualquer arquivo criado/modificado neste diretório será monitorado pelo Git.

## Alterações e Commits

* `git status`: Exibe o estado das alterações no diretório de trabalho e na área de preparação.
* `git add <arquivo>`: Adiciona um arquivo à área de preparação para o próximo commit.
* `git add .`: Adiciona todas as alterações do diretório atual à área de preparação.
* `git commit -m "Mensagem do commit"`: Cria um novo commit com as alterações da área de preparação.
* `git commit --amend`: Permite editar o último commit.

## Branches

* `git branch`: Lista todos os branches no repositório local.
* `git branch <nome_do_branch>`: Cria um novo branch.
* `git branch -d <nome_do_branch>`: Exclui o branch especificado.
* `git checkout -b <nome_do_branch>`: cria um novo branch (-b) e altera para ele. São dois comandos em 1 (novo branch e checkout).
* `git checkout <nome_do_branch>`: Muda para o branch especificado.

**Branches Principais:**

A comunidade de desenvolvimento de software estabeleceu algumas convenções para nomear branches no Git, visando clareza, organização e facilidade de colaboração. As mais comuns incluem:

* **main/master:**
    * É a branch principal, representando o estado estável e pronto para produção do código.
    * "main" está gradualmente substituindo "master" devido a questões de inclusão.
* **develop:**
    * Usada para integração de novas funcionalidades e correções antes de serem mescladas na "main".
    * Serve como a branch de desenvolvimento principal.

**Branches de Funcionalidades (Feature Branches):**

* Usadas para desenvolver funcionalidades específicas.
    * Nomes descritivos, como "feature/adicionar-login", "feature/nova-interface".
    * A palavra "feature" serve para caracterizar que essa branch é para o desenvolvimento de uma nova funcionalidade.

**Branches de Correções (Bugfix Branches):**

* Criadas para corrigir erros e bugs.
    * Nomes como "bugfix/corrigir-erro-login", "bugfix/ajuste-responsividade".
    * A palavra "bugfix" serve para caracterizar que essa branch é para correção de algum problema.

**Branches de Hotfix:**

* Usadas para correções urgentes em produção.
    * Nomes como "hotfix/correcao-seguranca", "hotfix/ajuste-emergencial".
    * A palavra "hotfix" caracteriza que essa branch é para correção de um problema emergencial, em produção.

**Outras Convenções:**

* Use palavras curtas e descritivas.
* Separe palavras com hífens (-).
* Evite caracteres especiais.
* Mantenha os nomes em letras minúsculas.
  
Seguir essas convenções facilita a compreensão do fluxo de trabalho e a colaboração em projetos Git.

## Merge

* `git merge <nome_do_branch>`: Mescla as alterações do branch especificado no branch atual.  
Obs: se você estiver dentro do `branch master` irá informar o nome do branch aonde ocorreu a alteração. Se estiver dentro de outro branch, por exemplo develop, irá executar o comando `git merge master`

## Checkout

O comando `git checkout` essencialmente permite que você navegue e manipule diferentes versões do seu projeto.

**1. Alternando entre Branches:**

* A função mais comum do `git checkout` é alternar entre diferentes branches. Isso permite que você trabalhe em funcionalidades separadas, corrija bugs ou explore versões antigas do seu código sem afetar a branch principal.
    * Exemplo: `git checkout minha-nova-funcionalidade`

**2. Criando Novas Branches:**

* O `git checkout` também pode ser usado para criar novas branches. Isso é útil para iniciar o desenvolvimento de uma nova funcionalidade ou para isolar correções de bugs. O comando -b indica a criação da branch
    * Exemplo: `git checkout -b nova-branch`

**3. Verificando Commits Antigos:**

* O `git checkout` permite que você navegue para commits específicos no histórico do seu projeto. Isso é útil para inspecionar versões antigas do código ou para depurar problemas.

**Pontos importantes:**

* **HEAD:** O `git checkout` atualiza o HEAD, que é um ponteiro para o commit atual. Isso determina qual versão do seu projeto você está trabalhando.
* **Diretório de trabalho:** o comando git checkout, altera os arquivos no seu diretório de trabalho, para que eles correspondam aos arquivos armazenados na branch que você esta verificando.
* **Cuidado com as alterações não comitadas:** Ao trocar de branch, certifique-se de que suas alterações locais estejam comitadas ou guardadas com `git stash`, caso contrário, elas podem ser perdidas.

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
