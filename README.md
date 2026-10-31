# Framework Atlas 🗺️

Notițele mele despre cele mai folosite framework-uri: ce sunt, cum se folosesc, cum se conectează la baze de date, cum se pun online (deploy), cum vorbesc între ele și cum lucrez în ele cu AI.

Fiecare framework are aceeași structură de fișiere și un mic **demo** funcțional.

<p align="left">
  <img src="https://skillicons.dev/icons?i=react,laravel,spring,nextjs" alt="React, Laravel, Spring, Next.js" />
</p>

## Progres

| # | Framework | Limbaj | Tip | Status | Demo |
|---|-----------|--------|-----|--------|------|
| 1 | React | JavaScript / TypeScript | Frontend | ⏳ urmează | – |
| 2 | Laravel | PHP | Backend | ⏳ urmează | – |
| 3 | Spring Boot | Java | Backend | ⏳ urmează | – |
| 4 | Next.js | TypeScript | Full-stack | ⏳ urmează | – |

**Valul 2:** Angular, ASP.NET Core, Django / FastAPI, Jakarta EE
**Valul 3:** Vue, NestJS, Flutter / React Native, Svelte

## Structura repo-ului

```
basics/          ce e un framework, frontend vs backend, API, ORM, deploy
frameworks/      un folder per framework, toate cu aceleași fișiere
  _template/     șablonul de pornire
integrations/    cum se leagă framework-urile (ex: React + Laravel API)
comparisons/     tabele de comparație
til/             „Today I Learned”: notițe scurte, cu dată
```

## Fișierele din fiecare framework

| Fișier | Ce conține |
|--------|-----------|
| `README.md` | ce e, la ce se folosește, când îl alegi |
| `concepts.md` | ideile de bază, funcții și metode importante |
| `commands.md` | comenzile esențiale (cheatsheet) |
| `databases.md` | conectarea la o bază de date |
| `deploy.md` | cum îl pui online |
| `integration.md` | cum comunică cu alte framework-uri |
| `ai-workflow.md` | cum lucrez în el cu AI (fișiere de context, MCP, prompturi) |
| `interview.md` | întrebări de interviu |
| `demo/` | mini-aplicație „todo” cu bază de date |

## Demo-urile sunt legate între ele

Toate backend-urile (Laravel, Spring Boot...) expun **același API** pentru o listă de task-uri, iar frontend-ul React poate vorbi cu oricare dintre ele. Așa se vede concret cum se conectează framework-urile.

## Cum am lucrat

1. Am citit documentația oficială (cu ajutorul AI).
2. Am completat șablonul.
3. Am construit demo-ul împreună cu AI-ul.
4. Am scris secțiunea **„Ce am înțeles eu”** cu propriile cuvinte.
