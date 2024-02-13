<h3>CONFIGURAÇÕES</h3>

* Configura o nome do usuário
  
      git config --global user.name "Daniela Neutzling"  
  
* Configura email do usuário
  
      git config --global user.email daneneutzling@gmail.com 
  
* Ativação de cores nas respostas 
  
      git config -–global color.ui true 


<h3>COMANDOS</h3>

* Inicializa o repositório Git 

      git init 

* Mostra o status dos arquivos que estão na branch, podendo OU não estarem preparados para commit 

      git status 

* Prepara todos arquivos OU o arquivo especificado para ser commitado 

      git add . 

    ou 

      git add nome_arquivo.extensao
      
* Commit dos arquivos que foram adicionados (com mensagem) 

      git commit -m "mensagem de commit" 

* Editar mensagem do último commit (abre um editor, edito, salvo, feito!) 

      git commit --amend 
      
* Lista as conexões que o repositório local possui com outros repositórios remotos
  OBS.: nome padrão é origin  

      git remote  

* Lista os repositórios remotos, incluindo a URL de cada conexão (vê se o repositório está amarrado a nuvem) 

      git remote -v 

* Cria conexão para repositório remoto 

      git remote add <nome> <url> 

* Remove a conexão com o repositório remoto 

      git remote rm <nome> 

* Renomeia a conexão no repositório remoto

      git remote rename <antigo> <atual> 

* Busca as atualizações do repositório remoto para o repositório local. Permite visualizar as alterações antes de integrá-las localmente.
  OBS.: Eu uso o git fetch seguido de git status  
        VS Code da fetch automaticamente e avisa
        
      git fetch

* Funde duas branches. Faz com que a a branch que estou seja sobrescrita com a branch que eu chamo 
  OBS.: devo estar na branch que quero que seja alterada 
  
      git merge nome_branch 
  
* Ferramenta para auxiliar no merge quando tiver conflitos 

      git mergetool

* Puxa dados do repositório remoto para o repositório local    
  OBS.: git pull é o mesmo que um git fetch seguido de um git merge.
        Permite visualizar as alterações antes de integrá-las localmente, APENAS se houver conflitos
    
      git pull 
  
* Puxa dados da branch 'nome_branch' do repositório remoto 'origin' e atualiza automaticamente para a branch do repositório local
  OBS.: OBS.: O uso de -u (ou --set-upstream) define a relação entre sua branch local e a branch remota, fazendo com que, nas próximas vezes que usar o comando, não seja necessário especificar as branches.
      git pull -u origin nome_branch 
      
* Empurra os dados do repositório local para o repositório remoto 

      git push 

* Empurra dados da branch local para a remota (atualiza no GitHub)
  OBS.: O uso de -u (ou --set-upstream) define a relação entre sua branch local e a branch remota, fazendo com que, nas próximas vezes que usar o comando, não seja necessário especificar as branches.
       
      git push -u origin nome_branch 

* Mostra todas branches do repositório ( * (asterísco) identifica qual branch estou) 
  OBS.: branch principal = master / main
  
      git branch 

* Cria uma nova branch 
  
      git branch nome_branch

* Muda para a branch especificada 

      git switch nome_branch 

* Mesmo comando do de cima, diferença que esse é o mais antigo (pouco usado)    

      git checkout nome_branch
      
* Mostra o "histórico" de alterações do meu git (commits e configurações realizadas) 

      git log 
      
* Visualização do que mudou por linha de comando
  OBS.: p = patch 
  
      git log -p  

* Volta a última versão do arquivo (rollback) 

      git restore

* Remove arquivos do stage ("palco" - "área de preparação" onde os arquivos são guardados antes de dar commit) 

      git restore --staged
      
* Remove os arquivos do repositório local (remove do stage e do diretório de trabalho)

      git rm

* Remove o arquivo da preparação para commit (remove do stage, mas não do diretório de trabalho)
      
      git rm –cached nome.arquivo 
      
* Clona o repositório remoto para o local 

      git clone <url> 

* Remove arquivos que estão fora do stage (que não foram preparados para commit) 

      git clean


* Para arquivos confidencias ou temporários, pode-se utilizar a extensão .gitignore, que faz com que o Git não realize commit nesse arquivo.
