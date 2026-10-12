<div>
  <a href="https://instagram.com/loyfuss" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:felipepenha32@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/feepenha" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
</div>

## Oi, sou o Luiz

Desenvolvedor de software. Graduando em Análise e Desenvolvimento de Sistemas.

Trabalho hoje principalmente com **Swift** e **Kotlin** — apps nativos para iOS
e Android — e com **Node/Express** no backend. Antes disso, muito PHP (Laravel e
CodeIgniter), React e MySQL.

## Projeto atual

### [Loyfus · iOS](https://github.com/loyfus/loyfus-ios) · [Android](https://github.com/loyfus/loyfus-android)

Catálogo de leilões brasileiros com dados reais — 20.229 lotes, 1.366 leilões,
19 categorias e 141.304 fotos, coletados e verificados contra a fonte pública.

O mesmo produto em duas plataformas, cada uma com design system próprio:

| | iOS | Android |
| --- | --- | --- |
| Stack | SwiftUI, iOS 17+, zero dependências | Kotlin, Jetpack Compose, MVVM |
| Testes | 54 XCTest | 38 testes de unidade |

O detalhe que sustenta os dois: `docs/design-v3/tidy_title_golden.tsv` é
**byte a byte idêntico** nos dois repositórios. É o contrato de dados
versionado da limpeza de títulos — os mesmos 1.566 casos reais validam as
duas implementações.

## Outros projetos

- [indexadorBackEnd](https://github.com/loyfus/indexadorBackEnd) — API de busca
  vetorial de ferramentas de IA sobre MongoDB Atlas Search, em camadas
  (rotas, controllers, serviços, repositório), com a camada de dados gerada
  pelo [AI-Crowler](https://github.com/loyfus/AI-Crowler).
- [duckSnap](https://github.com/loyfus/duckSnap) — app desktop (Electron +
  SQLite) para snapshots versionados de projetos locais.
- [animeSwift](https://github.com/loyfus/animeSwift) — app macOS em SwiftUI sobre
  a API GraphQL do AniList.
- [LoyfusAnime](https://github.com/loyfus/animeFrontEnd) — front em React para
  uma API de animes.

## Como trabalho

Gosto de comentário explicando **por quê**, não o quê — os READMEs dos dois
apps do Loyfus registram as decisões e o que foi descartado, porque foi
isso que guiou o trabalho. Escrevo testes que vencem por contrato (golden
files) em vez de por valor fixo no código.

<picture>
  <source
    srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact&theme=dark"
    media="(prefers-color-scheme: dark)"
  />
  <source
    srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact"
    media="(prefers-color-scheme: dark), (prefers-color-scheme: no-preference)"
  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact" />
</picture>
