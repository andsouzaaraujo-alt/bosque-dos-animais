# Bosque dos Animais

Jogo educativo e gratuito para crianças de 4 a 12 anos. A criança escolhe um bichinho, responde a um quiz rápido e aprende **Matemática, Ciências, História, Inglês e Artes** com os professores do bosque.

Por **Eduarda Normanha**.

## Como funciona

- **Abertura:** a placa do Bosque dos Animais com o Gabi e a Duda.
- **Avatar:** a criança escolhe entre Krau (gato laranja), Easter (coelho), Gat (gatinho cinza), Pelucinha (sagui), Floquinho (cachorro) e Leozinho (leão).
- **Quiz inicial:**
  - idade (que define a dificuldade), ano escolar e como gosta de aprender;
  - matéria favorita, matéria mais desafiadora e o motivo da dificuldade;
  - o que está aprendendo na escola, com a opção "Nenhuma dessas" e um campo livre;
  - com qual matéria quer começar (só uma);
  - perguntas para os pais, protegidas pela pergunta "6 × 7".
- **Níveis:** cada matéria é um nível com o seu professor. São três faixas de dificuldade:
  - Exploradores, de 4 a 6 anos;
  - Aventureiros, de 7 a 9 anos;
  - Mestres, de 10 a 12 anos.
- **Reforço:** a matéria marcada como mais desafiadora tem o botão de dica 💡 e repete as perguntas que a criança errou.
- **Presente surpresa 🎁:** no meio de cada nível, aparece uma aula curta de uma matéria ainda bloqueada. Se a criança completar a aula, essa matéria fica liberada.
- **Casinha:** os itens que a criança ganha decoram a casa do avatar.
- **Área dos pais:** mostra um resumo do quiz e o progresso da criança.

O progresso fica salvo só no aparelho em que a criança joga, no armazenamento local do navegador.

## Rodar no computador

O jogo é uma página só (`index.html`) e não precisa instalar nada. Para testar localmente:

```bash
python3 -m http.server 8000
```

Depois abra http://localhost:8000 no navegador.

## Estrutura

```
index.html               o jogo inteiro (HTML, CSS e JavaScript)
manifest.webmanifest     permite instalar na tela inicial do celular/tablet
assets/
  splash.webp            imagem de abertura
  logo.webp              marca
  professores/           Duda (Matemática), Gabi (Inglês) e, em breve, Tia Dea (Artes)
  avatares/              bichinhos que a criança pode escolher
  ajudantes/lapis.webp   lápis-unicórnio que ajuda nos campos de escrever
  icone-*.png            ícones do app
  originais/             artes originais, antes do recorte
```

## Como editar

Tudo fica no `<script>` do `index.html`:

- **Novo avatar:** salve a imagem em `assets/avatares/` e acrescente uma linha na lista `AVATARS`.
- **Novo professor:** em `SUBJ`, troque `img:null` pelo caminho da imagem e coloque o nome do professor.
- **Perguntas:** ficam no objeto `Q`, por matéria e por faixa (`p`, `m` e `g`). O formato é `[pergunta, [CERTA, errada, errada], dica, visual?, falaEmInglês?]`. A primeira opção é sempre a certa; o jogo embaralha as opções na tela.
- **Temas da escola** (mostrados no quiz): ficam no objeto `TOPICS`.
- **Voz:** está desligada. Para ligar, troque `VOICE = false` por `true`.
- **Sons:** ficam no objeto `SFX` (sons criados pelo navegador, sem arquivos). A criança liga e desliga no botão 🔊.

## Publicar uma nova versão

Veja o passo a passo em [docs/COMO-PUBLICAR.md](docs/COMO-PUBLICAR.md).

## Direitos

Os personagens, a marca e as ilustrações são de Eduarda Normanha. Todos os direitos reservados.
