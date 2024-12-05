# Backend encuestas NDT.

Necesitamos crear un backend con las siguientes caracteristicas:
- Servir archivos estaticos (index, login, visualizaciones...).
- Poder almacenar valoraciones.
- Poder almacenar usuarios.

## Base de datos.

Utilizaremos SQLite con dos tablas, `users` y `ratings`.

- Users
    - Name
    - Password

- Reviews
    - Rating
    - Message

## API

### POST /api/reviews

Endpoint para recibir los datos del usuario, los mandaremos por el body en formato JSON.

```json
{
    "rating": "good",
    "message": "lo que sea"
}
```

En rating solo pueden llegar tres valores posibles:

- good.
- neutral.
- bad.

En message:

Máximo de 256 caracteres.