# Análisis 1: Petición GET — example.com

## Información general

- URL: https://example.com
- Método: GET
- Código de estado: 304 Not Modified

## Headers de Request

| Header     | Valor                                     |
| ---------- | ----------------------------------------- |
| Host       | example.com                               |
| User-Agent | Mozilla/5.0 (Windows NT 10.0; Win64; x64) |

               AppleWebKit/537.36 (KHTML,like Gecko)
               Chrome/146.0.0.0 Safari/537.36

| Accept | text/html,application/xhtml+xml, |
application/xml;q=0.9,image/avif,image/
webp,image/apng,/;q=0.8,application/
signed-exchange;v=b3;q=0.7

## Headers de Response

| Header        | Valor            | Significado                                    |
| ------------- | ---------------- | ---------------------------------------------- |
| Content-Type  | text/html        | Indica que el contenido es una página web HTML |
| Cache-Control | No muestra valor | Controla cómo se almacena en caché la pagina   |

## Tiempos de carga

| Fase       | Tiempo (ms) |
| ---------- | ----------- |
| DNS Lookup | 0 ms        |
| TTFB       | 19.58 ms    |

## Conclusión

La petición HTTP realizada al servidor de example.com utiliza el método GET para solicitar un recurso web. El servidor responde con un código 304 Not Modified, lo que indica que el recurso no ha cambiado desde la última solicitud y puede ser cargado desde la caché del cliente. La presencia de encabezados como ETag y Last-Modified evidencia el uso de mecanismos de validación de caché, optimizando el rendimiento y reduciendo el consumo de red. Además, el uso de Cloudflare como servidor intermediario mejora la velocidad de respuesta, reflejado en un bajo tiempo TTFB de aproximadamente 19.58 ms. En general, se observa una comunicación eficiente y optimizada.
