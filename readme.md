Para instalar o git no windows
https://git-scm.com/downloads

senha:  S3nha@git

Para chamar o prompt de comando
git bash

verifica a versão do git instalada
git --version

COMANDOS FUNDAMENTAIS

para verificar a pasta
git status

Criar um repositório na máquina local
git init
git add arquivo a adicionar ou add.(adiciona tudo)
git commit -m "primeiro commit"
 se pedir e-mail ou usuário
git config --global user.email "linsmelo@gmail.com"
git branch -M master
git remote add origin https://github.com/Laercio0110/CursoGit1.git

limpar a tela do terminal
clear
verificar projeto 
git status

para atualizar o github
para atualizar um arquivo específico
git commit indext.html -m "enviando o arquivo index.html"
para atualizar vários arquivos
git commit -a -m "enviando a funcionalidade X"

para publicar as alterações no repositório remoto
git push

para receber mudanças feitas no repositório remoto
git pull

para clonar um repositório
git clone https://github.com/Laercio0110/CursoGit1.git .
Obs. o ponto no final indica diretorio atualizar

para remover um arquivo do repositório
git rm index.html

historico de alterações
git log
Obs para sair do log <ctrl c> ou "q"

para renomear um arquivo ou mover de pasta
git mv rodape.css css/rodape.css

para desfazer alterações
git checkout <arquivo>

para ignorar arquivos no projeto
criar o arquivo .gitignore

para desfazer alterações inclisive as comitadas
git reset --hard origin/master
Obs. ficará igual à master

BRANCHES
para listar as  branches
git branch

para criar branch
git branch <nome>

para deletar um branch
git branch -d <nome>  ou
git branch --delete <nome>

para mudar de branch
git checkout <nome>  apenas muda de branch
git checkout -b <nome>  cria nova branch e muda para a nova branch

para unir branches
git merge <nome>

Stash  é como se enviasse as alterações para uma lixeira podendo recuperar se necessário
git stash

para listar
git stash list

para ver alterações
git stash show

para recuperar
git stash apply <id>

para limpar as stash
git stash clear

para limpar uma stash específica
git stash drop <id>

TAGS

para criar a tag
primeiro faz o commit
git tag -a <nome> -m "mensagem"

para listar
git tag

para detalhar a tag
git show <nome da tag>

para mudar de tag
git checkout <nome da tag>

Enviando e Compartilhados TAGS

para enviar uma tag para o repositório
git push origin <nome da tag>

para enviar todas as tags
git push origin --tags

COMPARTILHAMENTO E ATUALIZAÇÃO

para listar todas as branches e tags
git fetch -a

RECEBENDO ALTERAÇÕES
git pull

ENVIANDO ALTERAÇÕES
git push
Obs. não esquecer do add . e commit

Utilizando o Remote
para remover
git remote rm origin
para adicionar
git remote add endereço link
git push --set-upstream origin <nome da branch>

Trabalhando com Submodulos (Para ter dois ou mais projetos nomesmo repositório)
git submodule add <repo> <nome do submodulo>

para verificar
git submodule

para atualizar o submodule
comitar as mudanças e
git push --recurse-submodules=on-demand
Obs. vai atualizar apenas o submodulo

ANÁLISES E INSPEÇÃO

Exibindo informações
git show
para ver tags
git show <tag>

Exibindo Diferenças
Para verificar diferença da branch atual
git diff

Para verificar diferença entre branches
git diff <branch>

Para verificar diferença entre arquivos
git diff <HEAD:arquivo1> <arquivo1>

Log de atividades resumido
git shortlog

ADMINISTRAÇÃO DO REPOSITORIO
Limpando arquivos untracked (arquivos que não foram utilizados o add)
git clean -f
Obs. cuidado com este comando verifique se realmente é para limpar

Otimizando o repositorio
git gc   (garbage collector)

Checando a integridade dos arquivos
git fsck

Reflog
Para mapear todos os passos no repositorio
Obs. Expira a cada 30 dias, mas pode ser configurado

Comprimindo o repositorio
git archive --format zip --output <nome_arquivo.zip>

MELHORANDO OS COMMITS DO PROJETO
Criando branches que não serão compartilhas no repositório
git rebase <func_a> <private_func_a> -i

edita a mensagem gerada e salva (dúvida rever aula 63)

Boas mensagens de commits
Separar assunto no corpo da mensagem com no máximo 50 caracteres e a letra inicial em maiúsculo
Corpo com no máximo 72 caracteres explicando como e porque do commit e não como o código foi escrito
Ex.: git commit -a -m "Criada a função de adição de produtos
A função foi criada para novos clientes conseguirem adicionar produtos ao carrinho antes do login"

Obs.: não fechando a " no final da linha e teclando <enter> permite pular uma linha. na tela aparece ">>"

EXPLORANDO E ENTENDENDO O GITHUB
Criando o repositório
Crtiar um repositório no github verifique se deverá ser púlic ou private e os demais itens (readme, .gitignore,choose licence,etc)
Obs. por default informe MIT licence

Aba code (aula 66)
Verificando licenças (67)
Aba issue (aula 68)
Anotações do que precisa corrigir

Aba pull request (aula 69)

Aba actions (aula 70)
Ci/Cd

Aba projects (aula 71)
Kanban

Aba wiki (aula 72)
documentação mais extensa do projeto

Aba insights (aula 73)
informações sobre o projeto
Obs. Forks quando alguém clona o nosso projeto

Aba settinghs (aula 74)
acesso a diversas configurações do projeto

CRIANDO UM GIST  (aula 75)
Obs. São pequenos códigos guardados no github

ENCONTRANDO REPOSITORIOS (aula 76)
Obs. ir para a home do github e pesquisar , pode demorar um pouco.

MARKDOWN (aula 78)
è uma forma de adicionar estilos a textos
o arquivo README.md aceita MARKDOWN (aula 79)

Cabeçalhos são determinados pelo símbolo # (aula 80)
Obs. # h1, ## h2, ### h3 vai até 6

Ênfase (aula 81)
**texto**  ou __texto__ -> negrito
*texto* ou _texto_ -> itálico
-**texto**_ -> combinado

Listas (aula 82)
Ex. ### linguagens do projeto:
* html
* javascript
* css
* php

### Funcionalidades a desenvolver:
1. Área de membros
    1. Login diferente para grupo de clientes
    2. Desconto para clientes diferentes
    3. CSS para grupo de clientes diferentes
2. Integração com outros pagamentos
3. Sistema de bônus primeira compra
Obs. para subtítulos tem que ter 4 espaços

Imagens (aula 83)
![Tigre](img/images.jpg)

LINKS (aula 84)
[texto do link](link)
Obs. se for do github pode inserir de forma direta https://www.github.com
Ex.:
[google](https://www.google.com)
[https://horadecodar.com.br](https://horadecodar.com.br)
Contribuidor: https://github.com/Laercio0110
para incluir uma imagem
[![Logo do PHP](https://upload.wikimedia.org/wikipedia/commons/2/27/PHP-logo.svg)](https://github.com/Laercio0110)
