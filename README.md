# Kingdom Lab — Cotizador

Sitio estático para **Kingdom Lab**, una agencia de fotografía, audiovisual y
diseño visual. No requiere build ni backend: HTML + Tailwind CSS (CDN) +
JavaScript vanilla, con el progreso guardado en `localStorage` del navegador.

## Páginas

| Archivo | Descripción |
| --- | --- |
| `index.html` (+ `app.js`) | Cotizador: asistente de 5 pasos — Tus datos, Organización, Servicios, Cantidades, Plan. |
| `anexo.html` | Servicios adicionales que Kingdom Lab también presta pero se cotizan aparte (auditorías, configuración de cuentas, publicidad paga, YouTube). |

## El cotizador

Asistente de 5 pasos:

1. **Tus datos** — nombre de contacto, marca/negocio, correo, teléfono, rubro.
2. **Organización** — el tipo de marca aplica un factor de precio: Marca
   personal (base), Marca comercial B2C (+20%), Fábrica/industria/B2B técnico
   (+40%), Institución u organismo (+60%).
3. **Servicios** — el cliente elige Fotografía, Audiovisual y/o Visuales
   (una o varias).
4. **Cantidades**, por categoría:
   - **Fotografía** — corporativa (por persona), comercial (por foto), de
     producto (por producto) y locación adicional (por foto extra), a
     cantidad libre.
   - **Audiovisual** — producción de video (IA, archivo listo, edición
     express, storyboard, grabación fuera o en el local del cliente) e
     historias/contenido hablado, a cantidad libre.
   - **Visuales** — posts, historias y carruseles, con un total sugerido
     mensual por sección que se reparte entre estilos y puede restablecerse.
5. **Plan** — resumen agrupado por categoría, subtotal, factor de
   organización y total, con botones para imprimir/guardar PDF y copiar el
   resumen.

`anexo.html` documenta los servicios que Kingdom Lab también presta pero que
**se cotizan aparte**, sin importar el rubro del negocio: auditorías,
configuración de cuentas, gestión de publicidad paga y producción de YouTube
en formato largo.

El progreso del cotizador se guarda en `localStorage` (clave
`kingdom-lab-cotizador`) — es local por navegador, no hay backend ni base de
datos compartida.

## Uso

No requiere instalación ni build. Abre `index.html` directamente en el
navegador, o sirve la carpeta con cualquier servidor estático:

```bash
npx serve .
# o
python3 -m http.server 8080
```
