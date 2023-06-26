## Configurações Iniciais
```
git config --global user.name "Filipe Reis"
git config --global user.email "filipe.reis17@live.com"
git config --global core.editor 'code --wait' //Editor default: VS Code
```

## Iniciando repositório
```
git init //Iniciar repositório
git status //status do repositório
git add Readme.md //Adiciona um arquivo ao repositório
```
```
git commit -m "Readme" //Comita com uma mensagem
git commit -am "Edit Readme" //Arquivo que já existe
git show d93038f8c709e5b53152a6ac99e1aa7012b667f1 //Ver modificação do commit
```

## Diff
```
git diff
git diff --name-only
```

## Log
```
git log //histórico de modificações
git log author="Filipe" //Procura por autor
git shortlog
git shortlog -sn //Somente nome da pessoa
git log --graph
git log -p meus-arquivos //Histórico de um arquivo
git log --after="MMM DD YYYY" //Histórico de commits
git log --before="MMM DD YYYY"
```

## Desfazendo alterações
```
git checkout Readme.md //Desfazer alterações antes do commit
git reset HEAD Readme.md
git reset --soft //Apaga a hash sem modificar arquivo
	    --mixed //
	    --hard //Apaga hash e modificações
```
Obs: Deve ser usado com bastante cuidado

## Criando uma SSH
```
ssh-keygen -t rsa -b 4096 -C "filipe.reis17@live.com"
~/.ssh //Entra na pasta das chaves
cat id_rsa.pub //Mostra a chave
```

## Ligando repositório local ao remoto
```
git remote add origin https://github.com/filipereis17/Teste.git
git remote //consulta
git remote -v //Mais informações
git push -u origin master //Envia os arquivos para o repositório
git pull // atualizar / baixar branch
```

## Clone
```
git clone git@github.com:filipereis17/github-course.git [diretório]
```

## Branch
```
git checkout stage //Muda para a branch 'stage'
git checkout -b testing //Cria um branch com nome 'testing'
git branch -D testing //Exlui branch
git branch -m novo-nome-da-branch //Renomeia branch
git checkout --orphan minha-branch-orfa //Branch sem conexão à principal
```

## Merge vs Rebase
```
git merge test //Adiciona o merge test no branch "master"
git rebase rebase-branch //Adiciona no topo a branch "rebase-branch"
```

## Stash
### Guarda arquivos em pasta separada antes de comitar
```
git stash //Armazena as alterações
git stash list //Lista os stashes
git stash clear //Limpa os stashes
```

## Alias
### Facilita os comandos por atalhos
`git config --global alias.s status //Configura 's' para o comando status`

## Tags
### Versiona o software
```
git tag -a 1.0.1 -m "Readme Finish"
get push origin master --tags //Envia tags para o remoto
git tag -d 1.0.0 //Apaga a tag 1.0.0
git push origin :1.0.0
```

## Revert
### Volta sem apagar do histórico
`git revert 56c455c348511943ccab9d8d5e9614a3084a81f`

## Correção de erros
### Filename too long
git config --system core.longpaths true

## Links de sites
[TreinaWeb - Comandos](https://www.treinaweb.com.br/blog/comandos-do-git-que-voce-precisa-conhecer-parte-1#:~:text=Para%20mudar%20para%20uma%20outra,passando%20o%20nome%20da%20branch.&text=Se%20voc%C3%AA%20adicionar%20%2Db%20%2C%20uma%20nova%20branch%20ser%C3%A1%20criada.) 

## Comandos terminal
```
mkdir NomeDaPasta
ls  //listar arquivos
ls -la //listar ocultos
cd ..
clear // limpa a tela
```

## Editor vi
```
vi Readme.md //Editor texto
	i //inserir texto
	Esc, :wq //Escrever e salva
```
