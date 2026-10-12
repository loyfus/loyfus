<div align="center">
  <a href="https://www.linkedin.com/in/loyfus" target="_blank">
    <img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://www.instagram.com/luizzzpenha" target="_blank">
    <img src="https://img.shields.io/badge/-Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" />
  </a>
  <a href="mailto:oi@loyfus.com.br">
    <img src="https://img.shields.io/badge/-Email-333333?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</div>

# Oi, eu sou o Luiz

Desenvolvedor de software, cursando Análise e Desenvolvimento de Sistemas.

Hoje é muito **Swift** e **Kotlin** — app nativo dos dois lados, o mesmo
produto rodando em iOS e Android. Antes disso foram anos de PHP (Laravel e
CodeIgniter), React e MySQL. Vim pelo backend e fui ficando com vontade de
testar as coisa na mão antes de entregar.

## Loyfus

O projeto em que estou mais fundo agora. Catálogo de leilões brasileiros com
dado de verdade: **20.229 lotes**, 1.366 leilões, 19 categorias e 141.304
fotos.

**[iOS](https://github.com/loyfus/loyfus-ios)** · **[Android](https://github.com/loyfus/loyfus-android)**

| | iOS | Android |
| --- | --- | --- |
| Stack | SwiftUI · iOS 17+ · zero dependência | Kotlin · Compose · MVVM |
| Testes | 54 XCTest | 38 de unidade |

O problema é do domínio, não da tela: no Brasil o preço de um lote está
espalhado em dezenas de portal, o título vem em CAIXA ALTA com código de
anúncio no meio — `CHEVROLET CLASSIC LS 2010 2011 CINZA` — e o prazo fica
escondido. A regra que limpa esse título é a mesma nos dois clientes, e os
dois são testados contra o **mesmo arquivo golden**, byte a byte idêntico nos
dois repositórios. São 1.566 títulos reais.

Escolhi golden file em vez de valor fixo no teste porque foi o jeito que
achei de transformar "os dois têm que concordar" em algo que a máquina
confere, e não em uma intenção minha.

##Outras coisas

- **[ai-tools-api](https://github.com/loyfus/ai-tools-api)** — busca vetorial de
  ferramenta de IA sobre MongoDB Atlas Search, em camadas. O dado é coletado
  pelo [ai-crawler](https://github.com/loyfus/ai-crawler).
- **[ducksnap](https://github.com/loyfus/ducksnap)** — app desktop pra versionar
  uma pasta antes de decidir versionar.
- **[anime-macos](https://github.com/loyfus/anime-macos)** — app macOS em SwiftUI em
  cima da GraphQL do AniList.
- **[anime-api](https://github.com/loyfus/anime-api)** e
  **[anime-web](https://github.com/loyfus/anime-web)** — API e front de animes.

## Como eu trabalho

Prefiro comentário explicando **por quê** e o que foi descartado, em vez de
repetir o que o código já diz. Foi por isso que os READMEs do Loyfus são
longos: registram decisão, não só resultado.

Uso agente de código no fluxo — dá pra ver nos nomes das branch
(`codex/...`) e num `AGENTS.md` que obliga a documentar rota nova no README.
Subir branch, revisar o diff, mergear. Não é o agente decidindo sozinho, é
eu conferindo cada linha — mas economiza a parte mecânica.

Uma coisa que困扰a: mantenho este perfil mais ou menos atualizado e ainda
assim tem projeto antigo parado aqui. Faz parte.

---

Estes são projetos de estudo — nenhum está em produção.

<p align="center">
  <picture>
    <source srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact&theme=dark" media="(prefers-color-scheme: dark)" />
    <source srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact" media="(prefers-color-scheme: light)" />
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact" alt="Linguagens mais usadas" />
  </picture>
</p>
