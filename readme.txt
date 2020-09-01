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

13)Mesclando informações
- Sempre você está na branch que será atualizada
# git merge branch_origem_atualizacao
- Enviar depois de mergeado
# git push

14) Conflitos
- Utilize IDES para comparar e resolver conflitos com mais praticidade
-> Como configurar kdiff3 no linux? 

