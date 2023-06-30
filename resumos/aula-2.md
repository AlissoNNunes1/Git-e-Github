# Salvando Alterações no Repositório Local 

**Adição de Arquivos**
 - adicionar arquivos ao controle de versão do Git

 ```
 git add <arquivo> ou git add . para adicionar todos os arquivos do diretório.
 ```

 **Criação de um Commit**
- commit no Git representa uma versão específica do seu projeto. 

```
git commit -m"Mensagem do commit"
```

**Gerenciamento de branches**
-  O Git permite a criação de branches para desenvolver recursos separadamente ou realizar experimentos sem afetar a versão principal.

para criar uma nova branch:
```
git branch <nome_branch>
```
 para alternar entre branches existente:
```
git checkout <nome_branch>
```

**Sincronização com o repositório remoto**

- Para sincronizar seu repositório local com um repositório remoto no GitHub, é necessário adicionar o link remoto usando o comando :

```
git remote add origin <url_repositorio>
```

e, em seguida, utilizar o comando para enviar suas alterações:

```
git push origin <nome_branch>
```