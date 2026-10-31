# framework-atlas: instrucțiuni pentru AI

Repo PUBLIC de notițe și demo-uri despre framework-uri. Explicațiile sunt în română, simple; codul, comenzile și numele de fișiere sunt în engleză.

## Ordinea
- Valul 1: React → Spring Boot → Angular → Laravel
- Valul 2: ASP.NET Core, Next.js, Django / FastAPI, Jakarta EE
- Valul 3: Vue, NestJS, Flutter / React Native, Svelte

## Structură
- Fiecare framework stă în `frameworks/<nume>/` și pornește din `frameworks/_template/`: `README.md`, `cheatsheet.md`, `ai-workflow.md`, `demo/` (cu `demo/CLAUDE.md` propriu). Nu schimba structura fără să întrebi.
- Demo-urile respectă `integrations/todo-api.md`: v1 la început, v2 (login + useri) după primele două framework-uri.

## Reguli
- Versiunile și comenzile se iau din documentația oficială actuală (context7 sau site-ul oficial), nu din memorie. Scrie versiunea și data în `README.md`-ul framework-ului. Versiuni fixate, fără `@latest`.
- Secțiunea „Ce a crăpat și ce am învățat” o scrie doar Iosua. Tu notezi erorile pe parcurs, ca să aibă din ce scrie, dar nu completezi tabelul.
- Fiecare backend are cel puțin testele minime din `todo-api.md` și le rulează în GitHub Actions.
- Commit-uri mici, cu prefix (`feat:`, `fix:`, `test:`, `docs:`, `refactor:`), câte o idee pe commit.
- Folosirea AI-ului rămâne la vedere (atribuirea din commit-uri, `CLAUDE.md` în fiecare demo). Nu o ascunde.
- Unelte AI (MCP etc.): doar oficiale, verificate înainte (autor, licență, cod, permisiuni) și instalate numai după „da” de la Iosua.
- Fără chei, parole sau `.env` în repo; doar `.env.example`.
- După fiecare framework: actualizează tabelul de progres și diagrama din `README.md`.
