# assanbek-kazbek-student-api

Spring Boot CRUD application (Student API) with PostgreSQL, Docker Compose and Jenkins.

Author: Assanbek Kazbek

Status: initial version

## API

Base URL: `http://localhost:8080/assanbek-kazbek/api/students`

| Method | Path | Description |
|---|---|---|
| GET | /api/students | List all students |
| GET | /api/students/{id} | Get one student |
| POST | /api/students | Create a student |
| PUT | /api/students/{id} | Update a student |
| DELETE | /api/students/{id} | Delete a student |
| GET | /api/info | Student name and app version |

## Run

```bash
cp .env.example .env   # set POSTGRES_PASSWORD
docker compose up -d --build
```

## Changes by Assanbek Kazbek

- Added the **Update** operation: `PUT /api/students/{id}` replaces full name, email, group and course.
- Returns `404 Not Found` with a JSON error body when the student does not exist.
- Covered by the automated test `updatesStudent`.
