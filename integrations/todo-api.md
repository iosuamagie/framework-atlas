# Contractul comun: Todo API

Toate backend-urile demo implementează exact aceste rute, ca frontend-ul să poată vorbi cu oricare.

**Base URL:** `http://localhost:<port>/api`

| Metodă | Rută | Ce face | Body (JSON) |
|--------|------|---------|-------------|
| GET | `/todos` | lista tuturor task-urilor | – |
| POST | `/todos` | adaugă un task | `{ "title": "Cumpără lapte" }` |
| PATCH | `/todos/{id}` | modifică un task | `{ "title"?: "...", "done"?: true }` |
| DELETE | `/todos/{id}` | șterge un task | – |

**Un task arată așa:**

```json
{ "id": 1, "title": "Cumpără lapte", "done": false, "created_at": "2026-10-31T12:00:00Z" }
```

**Reguli comune:** răspunsuri JSON, CORS permis pentru `http://localhost:5173` (frontend-ul React), `title` obligatoriu (altfel 422).
