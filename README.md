# Backend

## Run locally

```bash
cd backend
npm install
cp .env.example .env
# update MONGO_URI and JWT_SECRET in backend/.env
npm run dev
```

## API Endpoints
- `POST /api/auth/signup` - register new user
- `POST /api/auth/login` - authenticate and receive JWT
- `GET /api/tasks` - get tasks for authenticated user
- `POST /api/tasks` - create a task
- `PUT /api/tasks/:id` - update title, description, or completed status
- `DELETE /api/tasks/:id` - delete a task

## Swagger Docs
Visit `http://localhost:5000/api/docs` after starting the backend.

## Docker
Build the backend image:

```bash
docker build -t task-app-backend .
```

## Notes
- Protected routes require `Authorization: Bearer <token>` header.
- Task operations are scoped to the authenticated user.
