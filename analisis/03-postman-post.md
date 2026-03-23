# Análisis 3: Petición POST — API REST (Postman)

## Información general

- URL: https://jsonplaceholder.typicode.com/posts
- Método: POST
- Código de estado: 201 Created

## Headers de Request

| Header       | Valor            |
| ------------ | ---------------- |
| Content-Type | application/json |

## Headers de Response

| Header        | Valor                                          | Significado                                     |
| ------------- | ---------------------------------------------- | ----------------------------------------------- |
| Content-Type  | application/json; charset=utf-8                | Indica que la respuesta es un JSON              |
| Location      | https://jsonplaceholder.typicode.com/posts/101 | URL del recurso creado                          |
| X-Powered-By  | Express                                        | Framework del servidor                          |
| Cache-Control | no-cache                                       | Indica que la respuesta no se almacena en caché |
| Server        | cloudflare                                     | CDN intermediario                               |

## Response (Cuerpo)

```json
{
  "title": "Laboratorio Programacion Web",
  "body": "Analisis de peticiones HTTP con Postman.",
  "userId": 1,
  "id": 101
}
```

## Comparación: GET vs POST

| Característica          | GET                                  | POST                                  |
| ----------------------- | ------------------------------------ | ------------------------------------- |
| Propósito               | Obtener datos del servidor           | Enviar datos y crear recursos         |
| Envío de datos          | En la URL (query params)             | En el cuerpo (body)                   |
| Body                    | No                                   | Sí                                    |
| Idempotencia            | Sí                                   | No                                    |
| Caché                   | Sí (puede cachearse)                 | No generalmente                       |
| Seguridad               | Menos seguro (datos visibles en URL) | Más seguro (datos no visibles en URL) |
| Código de estado típico | 200 OK / 304 Not Modified            | 201 Created                           |
| Uso en API REST         | Lectura de recursos                  | Creación de recursos                  |
| Ejemplo                 | GET /posts/1                         | POST /posts                           |

## Conclusión

La petición POST realizada mediante Postman permitió simular la creación de un recurso en la API REST. El servidor respondió con un código 201 Created, indicando que la operación fue exitosa. La respuesta incluye el objeto enviado junto con un identificador único asignado, lo que confirma el comportamiento esperado en una API REST. Además, el header Location proporciona la URL del nuevo recurso creado. Los tests ejecutados validaron correctamente tanto el estado de la respuesta como la estructura del JSON, garantizando la correcta ejecución de la petición.
