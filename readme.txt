CURSO GIT

1) Instalação

- Atualizar pacotes do Sistema 
# apt-get update

- Instalar Git
# apt-get install git

- Checar Versão isntalada
# git -v

2) Configuração de Usuário 

- Configurando nome do usuário
# git config --global user.name "Cleiton Xavier"
- Configurando email usuário
# git config --global user.email "cxdossantos@gmail.com"
- Listando as configurações
# git config --list

3) Criação de Repositorio Local
~ considerando repositorio 'gitcourse'

git init

4) Versionando - Adicionando Alterações

- Apresenta o estado do arquivo
# git status

- Adicionar arquivo no rastreio
# git add <nome_arquivo>

- Adicionar todos os arquivos no rastreio
# git --all
# git add -A 
# git add .

5) Salvando Alterações
- Salvando alterações rastreadas
# git commit -m "Mensagem de resgistro"

6) Funcionamento do Git
- Not Staged (Alterada)
- Untracked (Não Salva)
- To be commited (Pronta para Salvar )

7) Vizualizar alerações
- Diferenças ultima versão antes do commit  com as mdificações atuais
# git diff
# git diff --cached
- Diferença na area de preparação
# git diff --chached 
# git diff --staged

8) Histórico de Alterações
- Visualizar Histórico
# git log
- Todas as modicifações em uma unica linha cada
# git log --oneline

Conceitos:
- Sempre listada das mais recentes pras mais antigas
- CHA: Id unico de identificação dos commit
- HEAD: Ultima modificação presente na branch

9) Usando commits anteriores 
- Acessa um commit da branch
# git checkout <cha_commit>
- Volta as HEAD da branch
# git chackout master

10) Desfazendo Alterações
- Volta as Head do Arquivo (somente para arquivos commitados)
# git checkout <nome_arquivo>
- Voltar ao estado incial da branch
# git reset --hard

11) Desfazendo alerações não rastreadas
- Remover arquivos adionados
# git clean -f 

12) Ignorando arquivos
- Site com informações do gitignore:
# https://github.com/github/gitignore

13) Clonando Repositorio
- Clonando um projeto
# git clona <url_projeto>

14) Versionar alteração no servidor
- Enviar alterações commitadas ao servidor
# git push
- Baixar ultimas atualizações da branch
# git pull 

- Commits também podem ser feitos direto pelo GitHUb

15) GitHub: Star, fork e pull request
- Star: Basicamente, favorita o projeto
- Fork: Basicamente, clona um projeto para o seu perfil
- Pull request: Envio de sugestão de melhoria para o repositório

16) Issues, Milestones, Labels
Issues: Problemas/Pendencias encontrados no código para correção
Labels: Sinalizados para as Issues criadas
Milestones: Basicamente uma "nova release" no repositório (Em qual versão Issue vai/foi resolvido) 

- Para ajudar criar um README apresentavel, use o site:
dillinger

17) BitBucket: Para configuração de chave ssh, existe um ink tutorial no proprio BitBucket
- Para alternar users com ssh diferentes 
# eval $(sh-agent)
# ssh-add ~/.ssh/arquivo_chave_SSH

18) Conceitos de branch
- Ramificação do Projeto, que permite que funcionalidades 
sejam desenvolvidas separadamente sem impactar funcionalidades estaveis do Projeto

19) Alterações não versionadas
- Resetar alteração e perder mudanças 
# git reset -HARD

20) Criação e Branch
- Lista branchs locais
# git branch

- Criar nova branch Local
# git branch nome_desejado

- Trocar de branch
# git checkout nome_branch

- Criar e Trocar branch
#git checkout -b nome_desejado

21) Enviando branch para o repositório
- Criando Branch Local no Repositório:
# git push --set-upstream origin nome_branch_repositorio
- Enviar informações commitadas ao repositório
# git push

- 'git pull' nao atualiza somente a branch acessada, e sim todo repositório

22) Removendo branchs locais
- Remover branch Local
# git branch -D nome_branch_local

23) Remover Branch remotas
- Remover branch Local e Repositório
# git push --delete origin name_branch

24) Renomear Branch (Local e Remota)
- Local:
# git branch -m nome_branch_branch_atual nome_branch_branch_desejado 

25) Mesclano Alterações
- Merge é sempre na branch que estamos
- Mescle com a branch origem 
# git merge branch_com_ateracoes
- Enviar as alterações
# git push 

- Utilize as IDE's para resoler conflitos

26) TAG
- Basicamente uma nova release do projeto 
- Adicionar TAG
# git tag -a nome_tag -m "Mensagem da Tag"
- Visualizar Tags
# git tag
- Enviar tag para  servidor
# git push origin tag_name
- Remover Tag Local
# git tag -d tag_name
- Remover tag Repositorio
# git push --delete origin tag_name 
- Tag podem ser criadas em commits antigos
# git checkout cha_commit
# git tag -a name_tag -m "Mensagem commit"
# git tag