# Contractul comun: Todo API

Toate backend-urile demo implementează aceste rute, ca frontend-ul React să poată vorbi cu oricare.

**Base URL:** `http://localhost:<port>/api`
**Reguli comune:** răspunsuri JSON, CORS permis pentru `http://localhost:5173` (frontend-ul React), erori de validare → `422`.

---

## v1: Todo simplu

| Metodă | Rută | Ce face | Body (JSON) |
|--------|------|---------|-------------|
| GET | `/todos` | lista tuturor task-urilor | – |
| POST | `/todos` | adaugă un task | `{ "title": "Cumpără lapte" }` |
| PATCH | `/todos/{id}` | modifică un task | `{ "title"?: "...", "done"?: true }` |
| DELETE | `/todos/{id}` | șterge un task | – |

**Un task:**

```json
{ "id": 1, "title": "Cumpără lapte", "done": false, "created_at": "2026-10-31T12:00:00Z" }
```

- `title` obligatoriu, maxim 255 caractere (altfel `422`).
- Task inexistent → `404`.

---

## v2: Login și useri

Se adaugă după primele două framework-uri. Un **user are mai multe todo-uri** (relație unu-la-mulți) și vede doar task-urile lui.

| Metodă | Rută | Ce face | Body (JSON) |
|--------|------|---------|-------------|
| POST | `/auth/register` | cont nou | `{ "name": "Ana", "email": "ana@example.com", "password": "..." }` |
| POST | `/auth/login` | primește token | `{ "email": "...", "password": "..." }` → `{ "token": "..." }` |
| GET | `/auth/me` | userul logat | – |

- Toate rutele `/todos` cer header-ul `Authorization: Bearer <token>` (token JWT). Fără token → `401`.
- Un task are în plus `user_id`. Task-ul altui user → `404` (nu dezvăluim că există).
- Parola: minim 8 caractere, salvată doar ca hash (niciodată în clar).

**Un user:**

```json
{ "id": 1, "name": "Ana", "email": "ana@example.com" }
```

---

## Teste minime pentru fiecare backend
1. `POST /todos` cu `title` valid → `201` și task-ul apare în `GET /todos`.
2. `POST /todos` fără `title` → `422`.
3. (v2) `GET /todos` fără token → `401`.
