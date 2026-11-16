# O teu site: guia completo

O site fica alojado no GitHub Pages, que é gratuito. Só pagas se quiseres um domínio teu (cerca de 10 a 15 € por ano).

**Do que precisas:**
- o ficheiro `meu-site.zip`
- o teu CV em PDF (opcional, para o botão "Download CV (PDF)")
- um computador com Chrome ou Edge
- uns 10 a 15 minutos

---

## 1. Pôr o site online (só uma vez)

**Passo 1: Conta no GitHub**
Vai a github.com e cria uma conta gratuita. O nome de utilizador vai aparecer no endereço do site: com o utilizador `lidiadias`, por exemplo, o site fica em `lidiadias.github.io`.

**Passo 2: Criar o repositório**
1. Carrega no **+** no canto superior direito e escolhe **New repository**.
2. Em **Repository name**, escreve exatamente `o-teu-utilizador.github.io` (por exemplo, `lidiadias.github.io`).
3. Escolhe **Public**.
4. Carrega em **Create repository**.

**Passo 3: Descompactar o ZIP**
Faz duplo clique em `meu-site.zip`. Fica uma pasta com isto lá dentro:

```
_config.yml      index.html      blog.html      portfolio.html
about.html       LEIA-ME.md      _data/         _includes/
_layouts/        _posts/         _projects/     assets/
```

**Passo 4: Carregar os ficheiros**
1. Na página do repositório, clica em **uploading an existing file**.
2. Abre a pasta descompactada, seleciona **tudo o que está lá dentro** (ficheiros e pastas) e arrasta para o navegador. Arrasta o conteúdo, não a pasta.
3. Espera até a lista acabar de carregar.
4. Carrega em **Commit changes**.

**Passo 5: Ativar o GitHub Pages**
1. Vai a **Settings → Pages**.
2. Em **Source**, escolhe **Deploy from a branch**.
3. Escolhe o branch `main` e a pasta `/ (root)`, e carrega em **Save**.

**Passo 6: Abrir o site**
Espera 1 ou 2 minutos e abre `https://o-teu-utilizador.github.io`. Se ainda não aparecer, espera mais um pouco e recarrega a página.

**Passo 7: CV em PDF**
No repositório, entra na pasta `assets`, escolhe **Add file → Upload files** e carrega o teu CV com o nome exato `cv.pdf`.

---

## 2. Editar o site

Podes editar qualquer ficheiro diretamente no GitHub: abre-o, clica no lápis ✏️, faz a alteração e carrega em **Commit changes**. O site atualiza sozinho em cerca de 1 minuto.

| Queres mudar… | Edita este ficheiro |
|---|---|
| Nome, email, LinkedIn, frase grande e subtítulo da Home | `_config.yml` |
| Toda a página About Me (abertura, experiência, crenças, competências, testemunhos) | `_data/cv.yml` |
| Os case studies da secção Work | ficheiros na pasta `_projects/` |
| Os artigos do blog | ficheiros na pasta `_posts/` |
| Cores | `assets/css/style.css` (as primeiras linhas) |

**Atenção nos ficheiros `.yml`:** mantém as aspas à volta dos textos e o alinhamento dos espaços. Se o site deixar de atualizar depois de uma alteração, o mais provável é faltar uma aspa ou haver um espaço fora do sítio.

---

## 3. Publicar um artigo novo no blog

1. Entra na pasta `_posts` e escolhe **Add file → Create new file**.
2. Dá-lhe um nome neste formato: `2026-11-20-titulo-do-artigo.md`. A data no início do nome é a data que aparece no site.
3. Escreve:

```
---
title: "O título do artigo"
resumo: "Uma ou duas frases que aparecem na lista de artigos."
---

O texto começa aqui. Usa ## para subtítulos, *itálico* e [links](https://exemplo.com).
```

4. Carrega em **Commit changes**. A Home mostra sempre os 3 artigos mais recentes.

---

## 4. Acrescentar um case study à secção Work

1. Abre um dos ficheiros em `_projects/`, copia o conteúdo todo e cria um ficheiro novo na mesma pasta (por exemplo, `novo-caso.md`).
2. Muda os campos do topo:
   - `title`, `resumo`, `cliente`, `tipo`, `year`
   - `ordem`: a posição na lista (1 aparece primeiro)
   - `numeros`: os números do painel escuro dos Results
3. Escreve o texto por baixo. A linha `{% include numeros.html %}` mostra o painel com os números: deixa-a na secção Results.

A Home mostra os 4 primeiros casos, pela `ordem`.

---

## 5. Usar um domínio teu (opcional)

1. Compra o domínio (por exemplo, em Cloudflare, Namecheap ou num registador .pt).
2. No GitHub, vai a **Settings → Pages → Custom domain**, escreve o domínio e carrega em **Save**.
3. No sítio onde compraste o domínio, configura o DNS como o GitHub indica (pesquisa "GitHub Pages custom domain").
4. Quando ficar ativo, liga a opção **Enforce HTTPS**.
