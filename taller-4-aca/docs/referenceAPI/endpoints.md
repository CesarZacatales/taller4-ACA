# Endpoints de la API

Esta sección documenta los endpoints principales de la API.

| Categoría       | Método | Endpoint            | Descripción                                      |
|-----------------|--------|---------------------|--------------------------------------------------|
| Autenticación   | POST   | `/auth/login`       | Inicia sesión y retorna un token de acceso.      |
| Autenticación   | POST   | `/auth/register`    | Registra un nuevo usuario.                       |
| Usuarios        | GET    | `/users`            | Lista todos los usuarios.                        |
| Usuarios        | GET    | `/users/{id}`       | Obtiene información de un usuario específico.     |
| Usuarios        | PUT    | `/users/{id}`       | Actualiza los datos de un usuario.               |
| Usuarios        | DELETE | `/users/{id}`       | Elimina un usuario.                              |

## Ejemplos de uso de endpoints en tres lenguajes

A continuación se muestran ejemplos de cómo consumir los endpoints de la API utilizando **cURL**, **Python (requests)** y **JavaScript (fetch)** para cada uno de los métodos principales:

### 1. Iniciar sesión (`/auth/login`)

=== "Python"
    ```python
    import requests

    url = "https://api.ejemplo.com/auth/login"
    payload = {"username": "usuario", "password": "contraseña"}
    response = requests.post(url, json=payload)
    print(response.json())
    ```

=== "cURL"
    ```bash
    curl -X POST https://api.ejemplo.com/auth/login \
        -H "Content-Type: application/json" \
        -d '{"username": "usuario", "password": "contraseña"}'
    ```

=== "JavaScript"
    ```javascript
    fetch("https://api.ejemplo.com/auth/login", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ username: "usuario", password: "contraseña" })
    })
        .then(res => res.json())
        .then(data => console.log(data));
    ```