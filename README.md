# Jimenez-post2-u1.

Laboratorio 2 - Peticiones HTTP/HTTPS y Postman

# Análisis de Peticiones HTTP — Unidad 1

## Descripción

Repositorio de análisis de peticiones HTTP/HTTPS realizado con
Chrome DevTools y Postman como parte del laboratorio 2 de
Programación Web — Séptimo Semestre.

## Herramientas utilizadas

- Google Chrome + DevTools (panel Network)
- Postman (petición POST con tests)

## Análisis realizados

| #   | Tipo               | URL                 | Código        |
| --- | ------------------ | ------------------- | ------------- |
| 1   | GET HTML           | https://example.com | 200 OK        |
| 2   | GET JSON (exitoso) | /posts/1            | 200 OK        |
| 3   | GET JSON (fallido) | /posts/999          | 404 Not Found |
| 4   | POST JSON          | /posts              | 201 Created   |

## Conclusiones

El análisis de peticiones HTTP permitió comprender el funcionamiento real de la comunicación entre cliente y servidor, identificando el uso de métodos como GET y POST en distintos contextos. Se evidenció la importancia de los códigos de estado HTTP, especialmente 200, 201, 304 y 404, para interpretar correctamente el resultado de una solicitud. Además, se observó cómo los mecanismos de caché (ETag, Cache-Control) optimizan el rendimiento evitando transferencias innecesarias de datos. La comparación entre contenido HTML y JSON permitió diferenciar claramente entre aplicaciones web tradicionales y APIs REST orientadas al intercambio de datos. Finalmente, el uso de herramientas como Chrome DevTools y Postman facilitó el análisis detallado de headers, tiempos de respuesta y validación de peticiones mediante pruebas automatizadas.
