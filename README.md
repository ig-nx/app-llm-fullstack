# Full Stack ToDo App (FastAPI + Next.js) - Backend

Aplicación full stack para la gestión de tareas (ToDo), construida con FastAPI en el backend y Next.js en el frontend. Incluye persistencia en PostgreSQL desplegado en Render y frontend en Vercel.

---

## Arquitectura del Proyecto

.
├── 001-fastapi-backend  
│   ├── routers  
│   ├── models.py  
│   ├── schemas.py  
│   ├── crud.py  
│   ├── database.py  
│   └── main.py  
│  
├── 002-nextjs-frontend  
│   └── todo-app  
│       ├── components  
│       ├── pages  
│       ├── styles  
│       └── package.json  

---

## Tecnologías

### Backend
- FastAPI  
- SQLAlchemy  
- PostgreSQL  
- Uvicorn  

### Frontend
- Next.js  
- React  
- Fetch API  

### Infraestructura
- Render  
- Vercel  

---

## Funcionalidades

- Crear tareas  
- Listar tareas  
- Filtrar tareas (completadas / pendientes)  
- Actualizar tareas  
- Eliminar tareas  

---

## Backend

### Endpoints

| Método | Endpoint      | Descripción        |
|--------|-------------|--------------------|
| GET    | /todos      | Obtener tareas     |
| POST   | /todos      | Crear tarea        |
| GET    | /todos/{id} | Obtener por ID     |
| PUT    | /todos/{id} | Actualizar tarea   |
| DELETE | /todos/{id} | Eliminar tarea     |

### Documentación

https://app-llm-fullstack.onrender.com/docs

---

## Base de Datos

CREATE TABLE todos (
    id BIGSERIAL PRIMARY KEY,
    name TEXT,
    completed BOOLEAN NOT NULL DEFAULT false
);

---

## Variables de Entorno

### Backend (Render)

DATABASE_URL=postgresql+psycopg2://user:password@host:port/dbname

### Frontend (Vercel)

NEXT_PUBLIC_API_URL=https://app-llm-fullstack.onrender.com

---

## Instalación Local

### Backend

cd 001-fastapi-backend  
pip install -r requirements.txt  
uvicorn main:app --reload  

### Frontend

cd 002-nextjs-frontend/todo-app  
npm install  
npm run dev  

---

## Despliegue

### Backend (Render)

Build Command:
pip install -r requirements.txt  

Start Command:
uvicorn main:app --host 0.0.0.0 --port 10000  

---

### Base de Datos (Render)

- Crear PostgreSQL  
- Copiar Internal Database URL  
- Usar en DATABASE_URL  

---

### Frontend (Vercel)

Root Directory:
002-nextjs-frontend/todo-app  

Variable:
NEXT_PUBLIC_API_URL  

---

## Estado

- Backend desplegado  
- Base de datos conectada  
- Frontend desplegado  
- Comunicación funcional  

---

