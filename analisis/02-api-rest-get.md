# Análisis 2: Petición GET — API REST (JSONPlaceholder)

## Información general

- URL: https://jsonplaceholder.typicode.com/posts/1
- Método: GET
- Código de estado: 304 Not Modified

Aunque se esperaba un código 200 OK, el navegador devolvió 304 Not Modified debido al uso de caché.

## Headers de Request

| Header     | Valor                         |
| ---------- | ----------------------------- |
| Host       | jsonplaceholder.typicode.com  |
| User-Agent | Mozilla/5.0 (Windows NT 10.0; |

               Win64; x64) AppleWebKit/537.
               36 (KHTML, like Gecko)Chrome/
               146.0.0.0 Safari/537.36       |

| Accept | text/html,application/xhtml+
xml,application/xml;q=0.9,
image/avif,image/webp,image/
apng,_/_;q=0.8 |

## Headers de Response

| Header          | Valor                               | Significado                                     |
| --------------- | ----------------------------------- | ----------------------------------------------- |
| ETag            | W/"124-yiKdLzqO5gfBrJFrcdJ8Yq0LGnU" | Identificador del recurso para control de caché |
| Cache-Control   | max-age=43200                       | Tiempo de vida en caché                         |
| Cf-Cache-Status | HIT                                 | Respuesta servida desde caché                   |
| Server          | cloudflare                          | CDN intermediario                               |
| X-Powered-By    | Express                             | Framework del backend                           |

📌 Análisis:
El servidor no envía el cuerpo porque el recurso no ha cambiado.

---

## Response (Cuerpo)

No se devuelve contenido debido al código 304.

---

## Prueba de recurso inexistente

- URL: https://jsonplaceholder.typicode.com/posts/999
- Método: GET
- Código de estado: **404 Not Found**

### Headers relevantes:

| Header         | Valor                           |
| -------------- | ------------------------------- |
| Content-Type   | application/json; charset=utf-8 |
| Content-Length | 2                               |

📌 Análisis:
El servidor devuelve un error indicando que el recurso no existe, cumpliendo con las prácticas REST.

---

## Comparación: HTTP tradicional vs API REST

| Característica    | HTML (example.com) | API REST                 |
| ----------------- | ------------------ | ------------------------ |
| Tipo de contenido | text/html          | application/json         |
| Uso               | Renderizar páginas | Intercambio de datos     |
| Código observado  | 304                | 304 / 404                |
| Caché             | Sí                 | Sí (ETag, Cache-Control) |
| Cliente           | Navegador          | Apps / frontend          |

---

## Conclusión

La petición a la API REST no devolvió un código 200 OK debido al uso de mecanismos de caché, respondiendo con un código 304 Not Modified. Esto indica que el recurso no ha cambiado desde la última solicitud y evita la transferencia innecesaria de datos. La presencia de headers como ETag e If-None-Match confirma el uso de validación de caché. Por otro lado, al solicitar un recurso inexistente, el servidor responde correctamente con un código 404 Not Found, cumpliendo con los principios de diseño REST. En general, se evidencia un manejo eficiente de recursos y errores en la API.
