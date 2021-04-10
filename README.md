# **Git-Cheat-Sheet**
Git é o sistema de controle de versão distribuído gratuito e de código aberto responsável por tudo o que o GitHub
relacionado que acontece localmente no seu computador. Esta folha de dicas apresenta os mais importantes e comuns comandos Git para fácil referência.
# **INSTALAÇÃO**
Com instaladores específicos de plataforma para Git, o GitHub também fornece o
facilidade de se manter atualizado com os últimos lançamentos do comando
ferramenta de linha ao fornecer uma interface gráfica do usuário para o dia-a-dia
interação, revisão e sincronização de repositório.

**GitHub para Windows**  
https://windows.github.com

**GitHub para Mac**  
https://mac.github.com

Para plataformas Linux e Solaris, a versão mais recente está disponível em o site oficial do Git.

**Git para todas as plataformas**  
http://git-scm.com

# **CONFIGURAR**
## Configurar as informações do usuário usadas em todos os repositórios locais

***git config --global user.name “[firstname lastname]”***  
definir um nome que seja identificável para crédito ao revisar o histórico de versão
***
***git config --global user.email “[valid-email]”***  
defina um endereço de e-mail que será associado a cada marcador de histórico
***
***git config --global color.ui auto***  
definir cores automáticas de linha de comando para Git para facilitar a revisão

# **CONFIGURAÇÃO E INIT**
## Configurando informações do usuário, inicializando e clonando repositórios
***git init***  
inicializar um diretório existente como um repositório Git
***
***clone git [url]***  
recuperar um repositório inteiro de um local hospedado via URL

# **ESTÁGIO E INSTANTÂNEO**
## Trabalhar com instantâneos e a área de teste Git
***git status***  
mostrar arquivos modificados no diretório de trabalho, preparados para seu próximo commit
***
***git add [arquivo]***  
adicione um arquivo como ele aparece agora em seu próximo commit (estágio)
***
***git reset [arquivo]***  
descompactar um arquivo enquanto mantém as mudanças no diretório de trabalho
***
***git diff***  
diferença do que foi alterado, mas não encenado
***
***git diff --staged***  
diferença do que foi encenado, mas ainda não foi confirmado
***
***git commit -m “[mensagem descritiva]”***  
comprometa seu conteúdo encenado como um novo instantâneo de commit

# **RAMIFICAR E FUNDIR**
## Isolando o trabalho nas filiais, mudando o contexto e integrando as mudanças
***branch git***  
liste seus ramos. um * aparecerá ao lado do branch atualmente ativo
***
***git branch [branch-name]***  
crie um novo branch no commit atual
***
***git checkout***  
mude para outro branch e verifique em seu diretório de trabalho
***
***git merge [branch]***  
mesclar o histórico do branch especificado no atual
***
***git log***  
mostra todos os commits no histórico do branch atual

# **INSPECIONE E COMPARE**
## Examinando logs, diffs e informações de objeto
***git log***  
mostra o histórico de commits para o branch atualmente ativo
***
***git log branchB..branchA***  
mostrar os commits no branchA que não estão no branchB
***
***git log --follow [arquivo]***  
mostra os commits que mudaram o arquivo, mesmo entre renomeações
***
***git diff branchB ... branchA***  
mostre a diferença do que está no branchA que não está no branchB
***
***git show [SHA]***  
mostrar qualquer objeto no Git em formato legível por humanos

# **RASTREAMENTO DE ALTERAÇÕES DE CAMINHO**
## O arquivo de controle de versão remove e altera o caminho
***git rm [arquivo]***  
exclua o arquivo do projeto e prepare a remoção para confirmação
***
***git mv [existing-path] [new-path]***  
mudar um caminho de arquivo existente e preparar a movimentação
***
***git log --stat -M***  
mostra todos os logs de commit com indicação de todos os caminhos que se moveram

# **PADRÕES DE IGNORAÇÃO**
## Prevenir preparo ou confirmação não intencional de arquivos 
***Histórico/***  
**_*.notas_**  
***_padronizar*/_** 

Salve um arquivo com os padrões desejados como .gitignore com qualquer string direta correspondências ou globs curinga.
***
***git config --global core.excludesfile [arquivo]***  
ignorar patern em todo o sistema para todos os repositórios locais 

# **COMPARTILHAR E ATUALIZAR**
## Recuperando atualizações de outro repositório e atualizando repositórios locais
***git remote add [alias] [url]***  
adicione um URL git como um alias
***
***git fetch [alias]***  
buscar todos os branches daquele controle remoto Git
***
***git merge [alias] / [branch]***  
mesclar um branch remoto em seu branch atual para atualizá-lo
***
***git push [alias] [branch]***  
Transmita commits de branch local para o branch de repositório remoto
***
***git pull***  
buscar e mesclar quaisquer commits do branch remoto de rastreamento

# **RECORDAR A HISTÓRIA**
## Reescrevendo branches, atualizando commits e limpando histórico
***git rebase [branch]***  
aplique quaisquer commits do branch atual antes do especificado
***
***git reset --hard [commit]***  
limpar a área de teste, reescrever a árvore de trabalho a partir do commit especificado

# **COMPROMISSOS TEMPORÁRIOS**
## Armazene arquivos modificados e rastreados temporariamente para alterar os ramos
***git stash***  
Salvar alterações modificadas e preparadas
***
***git stash list***  
lista ordem de pilha de alterações de arquivos armazenados
***
***git stash pop***  
escrever trabalhando do topo da pilha de estoque
***
***git stash drop***  
descartar as alterações do topo da pilha de estoque