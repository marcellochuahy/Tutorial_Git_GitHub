Tutorial_Git_GitHub
===================

Tutorial em português sobre Git e GitHub

Para ver os principais comandos do Terminal do Mac, acesse:
https://github.com/marcellochuahy/Terminal_macOS

Instalação
---------------------------------------------- 

Copie e cole o link em seu navegador.  

MacOS:  
http://git-scm.com/download/mac  

Windows:  
http://msysgit.github.io/  

Linux:  
http://book.git-scm.com/2_installing_git.html  

Criar uma conexão entre sua máquina e o GitHub
----------------------------------------------
```
git remote add origin https://github.com/usuario/nome_do_repositorio.git
git remote -v    Testa a conexão
```

Configurar o Git em sua máquina 
-------------------------------
```
git config --global user.name  "nome_de_usuario_no_GitHub"
git config --global user.email "email_do_usuario_no_GitHub"
```

Criar e Clonar
--------------
```
git init                                                   Inicia um projeto git na pasta atual
git clone /caminho/da/pasta/destino                        Clona um projeto local para sua pasta atual
git clone git@github.com:usuario/nome_do_repositorio.git   Clona um projeto externo para sua pasta atual
```

Adcionar arquivos alterados (Working Directory -> Stage Area)
-------------------------------------------------------------
```
git add algum_arquivo.html outro_arquivo.html              Adciona os arquivos na Stage Area (INDEX)
git add *                                                  Adciona todos os arquivos modificados na Stage Area (INDEX)
git add .                                                  Adciona todos os arquivos modificados da pasta atual na Stage Area (INDEX)
```

Comitar arquivos (Stage Area -> HEAD)
--------------
```
git commit -m "Descrição da alteração"    Salva as alterações nos arquivos e os envia para a HEAD
git commit -am "Descrição da alteração"   Adciona todos os arquivos modificados da pasta atual na Stage Area e salva as alterações nos arquivos e os envia para a HEAD
```

Sincronizar seus arquivos com o repositório remoto (HEAD -> GitHub)
-----------
```
git push -u origin master    "Empurra" os arquivos da HEAD para o repositório remoto no GitHub na branch master
```

Atualizar seu repositório local com as alterações salvas no GitHub
------------------------------------------------------------------
```
git pull    "Puxa" os arquivos do repositório remoto no GitHub para o Working Directory na sua máquina 
```

Branches
--------
```
git branch nome_da_ramificacao                       Cria uma ramificação
git checkout nome_da_ramificacao                     Altera entre branches (entra na ramificação nome_da_ramificacao)
git checkout -b nome_da_ramificacao                  Cria uma ramificação e entra nela (isso é um atalho para os 2 comandos acima)
git branch                                           Lista todos os branches locais e coloca um asterisco no branch ativo
git push origin nome_da_ramificacao                  "Empurra" o branch local para o GitHub
git push origin :ramificacao_que_sera_deletada       Deleta (no GitHub ) a ramificação ramificacao_que_sera_deletada
git branch -d ramificacao_que_sera_deletada          Deleta (localmente) a ramificação ramificacao_que_sera_deletada
git diff nome_da_ramificacao_A nome_da_ramificacao_B Visualiza as diferenças entre 2 branches
```

Merges
------
```
git merge nome_da_ramificacao_que_sera_importada    Mescla o branche nome_da_ramificacao_que_sera_importada com o branche onde vc está
```

Tags
----
```
git tag nome_da_tag commit_id    Cria uma tag
git log                          Exibe os IDs dos commits
git log --oneline                Exibe os IDs dos commits de forma resumida (one line)
git reset --hard numero-do-hash  Volta o projeto para o estado até esse commit (numero-do-hash)
```

Apagar ou recuperar arquivos
----------------------------
```
git rm algum_arquivo.html              Apaga o arquivo
git checkout -- arquivo_com_erros_html Substitui a versão atual do arquivo na Working Directory pela última versão salva no HEAD
git reset -- hard origin/master        Substitui todos os arquivos locais pelos armazenados no GitHub 
```
