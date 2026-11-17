# Como publicar uma nova versão do Bosque dos Animais

Guia para quem está aprendendo GitHub e Claude Code com este jogo.

## As palavras que você vai ver

| Palavra | O que é | Comparação |
|---|---|---|
| **Repositório** (repo) | A pasta do projeto no GitHub, com todo o histórico | Uma pasta compartilhada que lembra de todas as versões |
| **Commit** | Uma "foto salva" do projeto, com um recado dizendo o que mudou | "Salvar como v2: capa nova" |
| **Branch** (ramo) | Uma cópia paralela do projeto para testar mudanças sem mexer na versão oficial | Um rascunho ao lado do documento final |
| **main** | O ramo oficial. É ele que está no ar | O documento final |
| **Push** | Enviar os commits do computador para o GitHub | Sincronizar com a nuvem |
| **Pull Request** (PR) | Um pedido para juntar um ramo ao `main`. Lá você vê o que mudou, comenta e aprova | "Pode revisar antes de eu colocar na versão final?" |
| **Merge** | Aceitar o PR e juntar as mudanças ao `main` | Aceitar as alterações sugeridas |
| **GitHub Pages** | O serviço gratuito do GitHub que coloca o `main` no ar | A gráfica que imprime toda vez que o original muda |
| **Claude Code** | O Claude trabalhando direto nos arquivos do projeto: ele edita, testa, faz os commits e abre o PR | Um colega que mexe no projeto junto com você |

## O caminho de uma mudança

```
você pede ──► Claude cria um branch ──► faz commits ──► push ──► abre o Pull Request
                                                                       │
                                     você revisa no GitHub ◄───────────┘
                                                │
                                     você clica em "Merge"
                                                │
                       GitHub Pages publica sozinho (1 a 2 minutos)
                                                │
              https://andsouzaaraujo-alt.github.io/bosque-dos-animais/
```

## Passo a passo para revisar e publicar

1. **Abra o Pull Request** pelo link que o Claude mandar, ou pela aba **Pull requests** do repositório.
2. Na aba **Commits**, veja a lista de mudanças. Cada commit tem um título que diz o que mudou.
3. Na aba **Files changed**, veja as linhas alteradas: o que saiu fica em vermelho e o que entrou fica em verde.
4. Quer pedir um ajuste? Escreva um comentário no PR, ou peça direto aqui no Claude.
5. Gostou? Clique no botão verde **Merge pull request** e depois em **Confirm merge**.
6. Abra a aba **Actions**. Vai aparecer a tarefa **pages build and deployment**. Quando ela ficar com um ✓ verde, a versão nova está no ar.
7. Abra o site. Se ainda aparecer a versão antiga, recarregue com `Cmd + Shift + R` (Mac) ou `Ctrl + Shift + R` (Windows).

## Como pedir mudanças ao Claude Code

Peça em linguagem normal, como você já faz. Por exemplo:

- "Troca a cor do botão Começar para verde"
- "Adiciona o personagem X (imagem anexada) como avatar"
- "Abre um Pull Request com isso que eu reviso"

Se quiser treinar os comandos do git, peça: "me mostra os comandos que você está rodando e o que cada um faz".

## Desfazer uma mudança

No PR que já foi aceito, clique no botão **Revert**. O GitHub cria um novo PR que desfaz aquela mudança, e o histórico continua guardado. Você também pode pedir ao Claude: "desfaz o commit que trocou a fonte".

## Mudanças pequenas direto no GitHub (sem Claude)

1. Abra o arquivo no GitHub, por exemplo o `index.html`.
2. Clique no lápis ✏️ (**Edit this file**).
3. Faça a alteração, por exemplo corrigir um texto.
4. Clique em **Commit changes**. Escreva o que mudou e escolha **Create a new branch… and start a pull request**.
5. Revise o PR e faça o merge, como no passo a passo acima.
