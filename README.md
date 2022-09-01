<h3>CONFIGURAÇÕES</h3>

* Configura o nome do usuário
  
      git config --global user.name "Daniela Neutzling"  
  
* Configura email do usuário
  
      git config --global user.email daneneutzling@gmail.com 
  
* Ativação de cores nas respostas 
  
      git config –global color.ui true 

<h3>COMANDOS</h3>

* Inicializa o repositório Git 

      git init 

* Mostra o status dos arquivos que estão na branch, podendo OU não estarem preparados para commit 

      git status 

* Prepara todos arquivos OU o arquivo especificado para ser commitado 

      git add . 

    ou 

      git add nome.arquivo 
      
* Commit dos arquivos que foram adicionados (com mensagem) 

      git commit -m "mensagem" 

* Edição da mensagem do último commit (abre um editor, edito, salvo, feito!) 

      git commit --amend 
      
* Lista as conexões remotas que se tem com outros repositórios   
  OBS.: nome padrão é origin  

      git remote  

      git remote origin 

* Mesmo comando acima, incluindo URL de cada conexão (vê se o repositório está amarrado a nuvem) 

      git remote -v 

* Cria conexão para repositório remoto 

      git remote add <nome> <url> 

* Remove a conexão com o repositório remoto 

      git remote rm <nome> 

* Renomear a conexão 

      git remote rename <antigo> <atual> 

* Busca no meu repositório local e verifica se está tudo igual no repositório remoto e local 
  OBS.: Uso o git fetch seguido de git status  
        VS Code da fetch automaticamente e avisa
        
      git fetch  

* Puxa dados do remoto para o repositório local    
  OBS.: git pull é o mesmo que um git fetch seguido de um git merge 
    
      git pull 
  
* Puxa tudo da branch remota para a local (atualiza local) 

      git pull origin nome_branch 
      
* Empurra os dados locais para o remoto 

      git push 

* Empurra tudo da branch local para a remota (atualiza no GitHub) 
       
      git push -u origin nome_branch 

* Mostra todas branches do repositório ( * mostra qual branch eu estou) 
  OBS.: branch principal = master / main
  
      git branch 

* Cria uma nova branch 
  
      git branch nome_branch

* Mudança de branches 

      git switch nome_branch 

* Mesmo comando do de cima, diferença que esse é o mais antigo (pouco usado)    

      git checkout nome_branch
      
* Funde duas branches. Faz com que a a branch que estou seja sobrescrita com a branch que eu chamo 
  OBS.: devo estar na branch que quero que seja alterada 
  
      git merge nome_branch 
  
* Ferramenta para auxiliar no merge quando tiver conflitos 

      git mergetool
      
* Puxa do servidor e joga direto para o local 
  OBS.: pode matar tudo que está local 

      git checkout 

      git checkout nome_branch 

* Mostra o "histórico" de alterações do meu git (commits e configurações realizadas) 

      git log 
      
* Visualização do que mudou por linha de comando
  OBS.: p = patch 
  
      git log -p  

* Volta a última versão do arquivo (rollback) 

      git restore

* Remove arquivos do stage ("palco" - como se fosse uma sala onde são guardados os arquivos antes de dar commit) 

      git restore --staged
      
* Removo do repositório, sem deletar ele (removo arquivo do stage e deleto do scm) 

      git rm

* Remove o arquivo da preparação para commit       
      
      git rm –cached nome.arquivo 
      
* Serve para ignorar determinado arquivo para não ser commitado (arquivos com informações confidenciais) 

      git ignore 

* Adiciono arquivo git ignore no meu repositório 

      git add .gitignore 
      
* Clona o repositório remoto para o local 

      git clone <url> 

* Exclui arquivos não monitorados (que não foram preparados para commit) 

      git clean 
