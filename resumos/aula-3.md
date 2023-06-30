# Desfazendo Alterações no Repositório Local



para desfazer alguma alteração num arquivo:
```
git restore <file>
```

para alterar a mensagem do ultimo commit: 

```
git commit --amend -m"nova mensagem"
```
## O Comando **git reset** e seus Tipos

O comando `git reset` é uma ferramenta poderosa no Git que permite reverter alterações, mover o HEAD e atualizar a árvore de commits. Ele é usado para desfazer commits, atualizar branches e refazer o estado do repositório.

Existem três formas principais de usar o comando `git reset`, cada uma com um efeito diferente:

### 1. Soft Reset
```bash
git reset --soft <commit>
```
O soft reset mantém os arquivos no diretório de trabalho e na área de stage (index) inalterados. Ele desfaz o commit, movendo o HEAD e o branch apontando para um commit anterior, mas mantendo as alterações do commit desfeito na área de stage para que possam ser reutilizadas.

### 2. Mixed Reset
```bash
git reset --mixed <commit>
```
O mixed reset é o comportamento padrão quando nenhum tipo é especificado. Ele desfaz o commit e remove as alterações da área de stage, mas mantém as alterações nos arquivos do diretório de trabalho. Isso permite que você modifique as alterações antes de fazer um novo commit.

### 3. Hard Reset
```bash
git reset --hard <commit>
```
O hard reset é o tipo mais drástico de reset. Ele desfaz completamente o commit e descarta todas as alterações feitas nos arquivos. O diretório de trabalho, a área de stage e o branch são atualizados para o estado do commit especificado.

É importante lembrar que ao usar o `git reset`, os commits desfeitos não são excluídos permanentemente. Eles ainda existem no histórico do Git, mas não são acessíveis diretamente a partir do branch atual. Se você deseja restaurar commits desfeitos, é possível usar o comando `git reflog` para encontrar os hashes dos commits e recuperá-los.

**Dica:** Tenha cuidado ao usar o comando `git reset --hard`, pois ele pode remover permanentemente alterações não salvas nos arquivos. Certifique-se de fazer um backup adequado antes de executar esse tipo de reset.

Para mais informações sobre o comando `git reset` e seus tipos, consulte a [documentação oficial do Git](https://git-scm.com/docs/git-reset).
```

Espero que isso seja útil para você!