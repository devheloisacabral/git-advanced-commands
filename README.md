# Git by devheloisacabral

## Iniciando

Inicializa um repositório git
```
git init
```
<br>

Clona um repositório git pela  url
```
git clone [url]
```
<br>

Mostra as alterações feitas e outras informações
```
git status
```
<br>

Adiciona todas as alterações para o staged
```
git add .
```
<br>

Adiciona só o arquivo referenciado para staged
```
git add [nome]
```
<br>

Reverte o git add . 
```
git restore ^-staged
```
<br>

Volta o que você referenciou para o estado que estava no commit que você indicou
```
git restore ^-source=hash_do_commit [nome ou .]
```
<br>

## Commits e branches

Commitar as atualizações
```
git commit -m "- commit com uma mensagem entre "
```
<br>

Diferença entre o último commit e o da sua máquina
```
git dif
```
<br>

Diferença entre intervalos de commit
```
git diff hash1^.hash2 
```
<br>

Reaproveitando um commit de uma branch em outra
```
git cherry-pick [hash]
```
<br>

Devolve o autor e a data dos commits
```
git blame 
```
<br>

Lista todas as branches e mostra em qual você está
```
git branch 
```
<br>

Cria branch em cima do atual commit
```
git branch [nome] 
```
<br>

Muda o nome de branch1 para branch2
```
git branch -m branch1 branch2
```
<br>

Apaga a branch2
```
git branch -d branch2
```
<br>

Troca de branch criando uma nova
```
git switch -c [nome]
```
<br>

Troca de branch criando uma nova
```
git checkout -b [nome]
```
<br>

Mescla uma branch com as alterações de outra
```
git merge [nome]
```
<br>

Aborta uma operação de merge em andamento
```
git merge ^-abort
```
<br>

Deleta uma branch em seu repositório remoto
```
git push origin:branch
```
<br>

Atualizar sua branch em cima de novas funcionalidades
feitas em um commit de outra branch sem precisar dar merge
```
git rebase [nome]
```
<br>

Histórico de commits que contenham
uma palavra-chave específica
```
git log ^-grep="<palavra-chave>"
```
<br>

Exibe o histórico de commits
feitos por um autor específico
```
git log ^-author="<nome_do_autor>"
```
<br>

Exibe o histórico de commits desde
o momento especificado
```
git log ^-since="2 weeks ago"
```
<br>

Remove as branches remotas que
foram excluídas no repositório remoto
```
git remote prune origin
```
<br>

Volta seu código para o último commit, ignorando suas
alterações, commitadas ou não
```
git restore
```
<br>

Atualiza seu repositório com as alterações do repositório remoto
```
git pull
```
<br>

Envia suas alterações locais para o repositório remoto
```
git push
```
<br>

Pega as alterações do repositório mas não mescla automaticamente
```
git fetch
```
<br>

## Visualização

Histórico de commits dentro de uma branch
```
git log
```
<br>

Histórico de commits dentro de uma branch + dif
```
git log -p
```
<br>

Histórico de commits um em cada linha e mais informação
```
git log ^-oneline
```
<br>

Histórico de commits em gráfico
```
git log ^-graph
```
<br>

Personalize (mostra a hash do commit e seu autor)
```
git log ^-format=’%H%an’
```
<br>

Git log -p mas do último commit (HEAD)
```
git show
```
<br>

Git log -p mas de um commit em específico
```
git show [hash]
```
<br>

## Guardando o código

Guarda suas alterações para mais tarde
```
git stash
```
<br>

Reverte o git stash em forma de pilha
```
git stash pop
```
<br>

Mostra o armazenamento do git stash
```
git stash list
```
<br>

Stash pop para o indície do git stash list desejado
```
git stash apply [i] 
```
<br>

Limpa o histórico do git stash list
```
git stash clear 
```
<br>

## Tags

Cria uma tag apontando para um commit
```
git tag [nome] 
```
<br>

Cria uma tag apontando para um commit com uma mensagem
```
git tag -a -m "" 
```
<br>

Informações da tag
```
git tag -V
```
<br>

## Outros

Remove as branches que foram excluídas no
repositório remoto.
```
git remote prune origin
```
<br>

Renomeia um repositório remoto
```
git remote rename [nomeantigo] [nomenovo]
```
<br>

Adiciona um novo repositório remoto com um
nome especificado
```
git remote add [nome] <URL^
```
<br>

Remove um repositório remoto.
```
git remote remove [nome]
```
<br>

Mostra os repositórios remotos associados ao seu repositório
```
git remote -v
```
<br>

Exibe informações sobre um repositório remoto,
incluindo branches remotas e URLs.
```
git remote show [nome]
```
<br>

Remove arquivos não rastreados no diretório de trabalho
```
git clean -fd
```
<br>

Lista arquivos que seriam removidos com git clean
```
git clean -n
```
<br>

Simula a remoção de branches remotas
sem realmente removê-las
```
git remote prune ^-dry-run origin
```
<br>

Cria um arquivo zip
com o conteúdo da branch especificada
```
git archive ^-format=zip ^-output=nome.zip <branch^
```
<br>
