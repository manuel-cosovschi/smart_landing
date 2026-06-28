# Smart Center Gym — Landing Page

Sitio web (landing) de **Smart Center Gym**, Mar del Plata. Es un sitio
estático (HTML + CSS + JavaScript, sin framework ni build) pensado para
captar contactos a través de **WhatsApp**.

## Estructura del proyecto

```
smart_landing/
├── index.html          # Página principal (landing)
├── admin.html          # Panel de administración (novedades / configuración)
├── logo.png            # Logo del gimnasio
├── hero-video.mp4      # Video de fondo del encabezado (hero)
├── sala principal.mp4  # Videos de las zonas / áreas (galería)
├── area funcional.mp4
├── zona calistenia.mp4
├── calistenia.mp4
├── clases grupales.mp4
└── README.md
```

> Todos los videos están en formato **vertical (9:16)**. Los marcos de la
> galería usan ese mismo formato para que el video se vea completo y sin
> recortes raros.

## Secciones de `index.html`

1. **Hero** — video de fondo, título y botones de acción.
2. **Stats** — contador animado (socios, años, actividades).
3. **Actividades** — Funcional, Stretching, Calistenia, Aerocombat, Strong,
   Musculación. Cada tarjeta enlaza a WhatsApp.
4. **Turistas** — propuesta para quienes están de vacaciones en Mar del Plata
   (pase por día / semana / 15 días). Los precios se consultan por WhatsApp.
5. **Membresías** — bloque simple: *"Tenemos una membresía adecuada a tus
   necesidades. No dudes en consultarnos"* + botón de WhatsApp. **No se
   publican precios**: todo se consulta por WhatsApp.
6. **Novedades** — se cargan desde el panel admin (se ocultan si no hay).
7. **Horarios**.
8. **Galería** — videos de las distintas zonas/áreas del gimnasio. Se
   reproducen automáticamente (en silencio) solo cuando entran en pantalla.
9. **Ubicación** — mapa, contacto y redes.

## Cómo verla localmente

Al usar videos, conviene servir los archivos con un servidor local (abrir el
HTML directamente con `file://` también funciona, pero un servidor evita
problemas con algunos navegadores):

```bash
# Opción 1: Python
python3 -m http.server 8000

# Opción 2: Node
npx serve .
```

Luego abrir <http://localhost:8000> en el navegador.

## Panel de administración (`admin.html`)

Permite cargar/editar **Novedades** que aparecen en la landing y cambiar la
contraseña de acceso. Los datos se guardan en el `localStorage` del navegador
(no hay backend), por lo que las novedades cargadas se ven en el mismo
dispositivo/navegador donde se publican.

- Acceso: enlace discreto **"admin"** en el pie de página.
- Contraseña por defecto: `smart2024` (se puede cambiar desde **Configuración**).
- Nota: es una protección básica del lado del cliente, pensada para uso
  interno.

## Contacto

- **WhatsApp:** +54 9 223 582-3460
- **Instagram:** [@smartcentergym](https://instagram.com/smartcentergym)
- **Dirección:** Av. Constitución y Marcos Sastre, Mar del Plata

## Dominio (pendiente)

El sitio todavía no está publicado en un dominio propio. Una vez que se tenga
acceso al proveedor donde se compró el dominio oficial, se configura ahí
(apuntando el dominio al hosting que se use) y se actualiza esta sección con
la dirección final.

## Despliegue

Al ser un sitio estático, se puede publicar en cualquier hosting estático
(GitHub Pages, Netlify, Vercel, etc.) subiendo el contenido de esta carpeta.
Hay que asegurarse de subir también los archivos `.mp4` y `logo.png`.
