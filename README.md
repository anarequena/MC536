#[MC356] (https://github.com/anarequena/MC536.git)

Um mini-tutorial está em baixo, mas tem um guia básico que parece interessante de se ler: [Git - The Simple Guide] (http://rogerdudler.github.io/git-guide/).

Um outro blog legal de se ler é o blog do Git.

##Começar a trabalhar:

Legenda: recomendável, comando.

Inicializar o git : $ git init
Criar uma pasta git caso não tenha
Realizar o pull request: $ git pull https://github.com/gufernandez/Projeto1MC504
Clonar: $ git clone https://github.com/gufernandez/Projeto1MC504
Ir até a pasta e criar um branch pra você: $ git checkout -b Eu
Dar push no branch: $ git push origin Eu
Codar hardmente
##Comandos

###Coisas básicas

Adicionar arquivos no repositório: $ git add <arquivos>
Registrar suas mudanças: $ git commit -m "Sua mensagem aqui"
Fazer upload: $ git push origin <branch> (De preferência, no seu branch)
Verificar status: $ git status
##Lidar com branches

Ver os branches existentes e em qual está: $ git branch
Criar novo branch: $ git branch <nome>
Mudar de branch: $ git checkout <nome>
###Atualizar o arquivo compartilhado Mesmo se você não quiser colocar os seus arquivos no git, tem de usar o seu branch para gerenciar melhor a mudança do arquivo principal.

Achei uma solução bem simples pro nosso problema: How to merge changes to a single file

Basicamente,você está no branch Eu e mudou certo arquivo que precisa ser atualizado no master. Faça o seguinte:

Mude para o branch master: $ git checkout master

Una os dois arquivos: $ git checkout --patch Eu <arquivo>

Gerencie as mudanças (pode aceitar parte por parte com 'y' ou tudo com 'a' ou editar o arquivo final com 'e')

Atualize a tag: $ git tag -a vx.y.z -m "Mudança"

Sendo: x = 0 ou 1 (projeto completo ou não), y += 1 a cada função adicionada e z += 1 quando bugs são corrigidos
Registre as mudanças com commit: $ git commit -m "Texto aqui"

Dê o upload dos arquivos: $ git push

Dê o upload das tags: $ git push --tags
