# Mesadas

App personal para registrar los aportes en dinero (mesadas) para Piti y Emi. Cada vez que se anota un monto, se actualiza el total de la persona que lo recibió.

## Qué hace

- **Nuevo aporte**: se ingresa el monto, se elige si es para Piti o para Emi y se escribe el asunto (almuerzo, ropa, helados…). La fecha es la de hoy, y se puede cambiar.
- **Totales**: muestra el total acumulado de cada una, lo entregado en el mes en curso y el total de las dos.
- **Aviso del nuevo total**: al registrar, indica el monto anotado y el nuevo total de esa persona.
- **Historial**: lista de aportes por mes, con el total acumulado después de cada uno. Se puede filtrar por persona, y cada aporte se puede editar o eliminar.
- **Asuntos frecuentes**: los asuntos más usados aparecen como botones para no tener que escribirlos.
- **Respaldo**: copia todos los aportes como texto y los restaura desde ahí (los datos viven solo en el dispositivo).

Ejemplo:

| Monto | Para | Asunto | Nuevo total |
| --- | --- | --- | --- |
| $10.000 | Piti | Almuerzo | Piti: $10.000 |
| $3.000 | Piti | Ropa | Piti: $13.000 |
| $11.000 | Emi | Almuerzo | Emi: $11.000 |
| $5.000 | Emi | Helados | Emi: $16.000 |

## Instalar en el iPhone

1. La app se publica con GitHub Pages en `https://pablocarvallo.github.io/hijas/`.
2. Abre esa dirección en **Safari** en el iPhone.
3. Toca **Compartir → Agregar a inicio**.

Se abre como app independiente, con su icono, y funciona sin conexión después de la primera carga.

## Archivos

| Archivo | Uso |
| --- | --- |
| `index.html` | La app completa (HTML, CSS y JavaScript, sin dependencias ni compilación) |
| `manifest.webmanifest` | Nombre, colores e iconos de la app instalada |
| `sw.js` | Service worker para uso sin conexión |
| `icons/icon-full.svg` | Icono original a pantalla completa (fuente de los PNG) |
| `icons/icon.svg` | Icono con esquinas redondeadas (favicon) |
| `icons/apple-touch-icon.png` | Icono de 180 px para la pantalla de inicio del iPhone |
| `icons/icon-192.png`, `icons/icon-512.png`, `icons/icon-1024.png` | Iconos del manifiesto y archivo de alta resolución |
| `fonts/` | Tipografías Bricolage Grotesque y Figtree, distribuidas bajo la licencia SIL Open Font License 1.1 |

## Datos

Los aportes se guardan en `localStorage` del navegador bajo la clave `mesadas-aportes`. Cada aporte tiene persona (`piti` o `emi`), monto en pesos, asunto, fecha y momento de registro. No se envía nada a ningún servidor.
