<div align="center">
  <a href="https://instagram.com/loyfuss" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:felipepenha32@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/feepenha" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
</div>

<h1 align="center">Oi, sou o Luiz 👋</h1>

<p align="center">
  Desenvolvedor de Software · estudante de Análise e Desenvolvimento de Sistemas
</p>

---

## 🚀 Loyfus — catálogo de leilões brasileiros

Um projeto completo de **três repositórios**: um crawler em Java coleta lotes reais de uma
fonte pública, um backend Spring Boot normaliza e serve, e dois apps nativos — Kotlin/Compose e
SwiftUI — consomem a mesma API.

**20.229 lotes · 1.366 leilões · 19 categorias · 141.304 fotos** — coleta real, verificada numa
rodada completa.

<table>
  <tr>
    <td width="50%" align="center">
      <a href="https://github.com/loyfus/loyfus-android"><img src="https://raw.githubusercontent.com/loyfus/loyfus-android/main/docs/screenshots/01-inicial.png" alt="Loyfus Android"></a><br>
      <sub>Android · Kotlin + Compose</sub>
    </td>
    <td width="50%" align="center">
      <a href="https://github.com/loyfus/loyfus-ios"><img src="https://raw.githubusercontent.com/loyfus/loyfus-ios/main/docs/screenshots/01-inicial.png" alt="Loyfus iOS"></a><br>
      <sub>iOS · SwiftUI, sem dependências</sub>
    </td>
  </tr>
</table>

| Repositório | O que é |
|---|---|
| [**loyfus-backend**](https://github.com/loyfus/loyfus-backend) | crawler + API REST + PostgreSQL · Spring Boot 4 · Java 17 |
| [**loyfus-android**](https://github.com/loyfus/loyfus-android) | app Kotlin + Jetpack Compose · Material 3 · MVVM |
| [**loyfus-ios**](https://github.com/loyfus/loyfus-ios) | app SwiftUI · iOS 17+ · zero dependências externas |

**O que há de interessante no meio dele:**

- As mesmas regras de formatação de preço, contagem regressiva e limpeza de título existem
  **espelhadas em Kotlin e Swift**, testadas contra um golden compartilhado de 1.566 títulos
  reais — uma divergência entre os dois apps vira um teste vermelho, não uma surpresa.
- O crawler é educado: se identifica, limita a taxa, respeita `Retry-After` e faz backoff
  exponencial.
- O app **não simula lance**. Cada lote guarda a URL de origem e o botão leva ao site do
  leiloeiro.

---

## 🛠️ O que eu uso

**Native mobile** — Kotlin · Jetpack Compose · Material 3 · Swift · SwiftUI · MVVM ·
`StateFlow` · Coroutines · Navigation Compose

**Backend** — Java 17 · Spring Boot 4 · PostgreSQL · JPA/Hibernate · Flyway · JUnit · Gradle

**Web** — PHP (Laravel · CodeIgniter) · JavaScript (React · Node)

**Banco** — MySQL · PostgreSQL

**Ferramentas** — Git · Docker · Xcode · XcodeGen · GitHub Actions

---

## 📊 GitHub

<picture>
  <source
    srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact&theme=dark"
    media="(prefers-color-scheme: dark)"
  />
  <source
    srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact"
    media="(prefers-color-scheme: light)"
  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=loyfus&layout=compact" alt="Linguagens mais usadas" />
</picture>

---

<p align="center">
  <sub>Dados de coleção do Loyfus: SuperBid, via endpoints públicos consumidos pela própria vitrine do site.</sub>
</p>
