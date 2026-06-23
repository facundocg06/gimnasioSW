# Cómo levantar con Docker

## Requisitos
- Docker y Docker Compose instalados

## Levantar el proyecto

```bash
docker compose up --build
```

Luego abre: http://localhost

## Apagar

```bash
docker compose down
```

Para borrar también los datos de postgres:

```bash
docker compose down -v
```

## Servicios
| Servicio   | URL interna          | Puerto expuesto |
|------------|----------------------|-----------------|
| nginx      | —                    | :80             |
| backend    | http://backend:8000  | :8000           |
| postgres   | postgres:5432        | :5432           |
| frontend   | (volumen compartido) | —               |
