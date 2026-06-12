# Sitio web de Anvavi Comercializadora

Bienvenido al sitio. Esta guía te explica TODO lo que necesitas saber para administrarlo, modificarlo y subirlo a internet.

## Estructura de archivos

```
anvavi-sitio/
├── index.html              ← Página de Inicio
├── areas.html              ← Página de Áreas y productos
├── personalizacion.html    ← Página de Bordado, DTF, sublimado
├── nosotros.html           ← Página Nosotros
├── cotiza.html             ← Página de cotización (con formulario)
├── styles.css              ← Estilos (colores, tipografías, look)
├── assets/
│   └── logo.jpg            ← Logo de Anvavi
└── LEEME.md                ← Este archivo
```

## Cómo PUBLICAR el sitio (paso a paso, sin conocimientos técnicos)

### Paso 1: Crear cuenta en Cloudflare (gratis, 5 min)
1. Entra a https://dash.cloudflare.com/sign-up
2. Regístrate con tu correo (idealmente con uno profesional cuando lo tengas)
3. Confirma el correo

### Paso 2: Subir el sitio a Cloudflare Pages (gratis, 10 min)
1. En el panel de Cloudflare, busca "Workers & Pages" en el menú izquierdo
2. Click en "Create application" → "Pages" → "Upload assets"
3. Ponle nombre al proyecto: `anvavi`
4. Arrastra TODA la carpeta `anvavi-sitio` al área de upload
5. Click en "Deploy site"
6. ¡Listo! En segundos te dará una URL tipo `anvavi.pages.dev`

### Paso 3: Conectar tu dominio (opcional, cuando lo compres)
1. Compra el dominio `anvavi.com.mx` en Cloudflare Registrar (~$300/año)
2. En el proyecto de Pages, ve a "Custom domains" → "Set up a custom domain"
3. Escribe `anvavi.com.mx`
4. Cloudflare configura todo automáticamente

## Cómo modificar el sitio

### Para cambiar UN TEXTO:
1. Abre el archivo .html que contiene el texto
2. Búscalo con Ctrl+F
3. Modifícalo
4. Guarda y vuelve a subirlo a Cloudflare (te toma 30 segundos)

### Para cambiar el TELÉFONO de WhatsApp:
- Está en TODOS los archivos como `5216621705229` (52 = México, 1 = celular, después el número)
- Si lo cambias, hazlo en TODOS los archivos .html

### Para cambiar UNA IMAGEN:
1. Pon la nueva imagen en la carpeta `assets/`
2. En el .html, busca dónde se llama y cambia el nombre

### Para cambiar COLORES del sitio:
Abre `styles.css`. Al inicio verás:
```css
:root {
  --azul-marca: #083E62;     ← cambia este código para cambiar el azul
  --verde-whatsapp: #25D366;
  ...
}
```

## IMPORTANTE: configurar el formulario de cotización

El formulario en `cotiza.html` está conectado a un placeholder. Para que los mensajes te lleguen:

### Opción A: Formspree (gratis, lo más fácil)
1. Entra a https://formspree.io/ y regístrate gratis
2. Crea un nuevo "Form" con el correo donde quieres recibir las cotizaciones
3. Formspree te dará un código tipo `https://formspree.io/f/xyzabc123`
4. En `cotiza.html` busca esta línea:
   ```
   <form action="https://formspree.io/f/REEMPLAZAR_AQUI" method="POST">
   ```
5. Reemplaza `REEMPLAZAR_AQUI` por tu código (queda `https://formspree.io/f/xyzabc123`)
6. Vuelve a subir el archivo a Cloudflare

### Opción B: WhatsApp directo (si no quieres ni Formspree)
Ya está activo. Los clientes pueden mandar mensajes por WhatsApp con un click. Es la opción más rápida para empezar.

## Próximos pasos recomendados (después de tener el sitio arriba)

1. **Crear Google Business Profile** (gratis) — registra tu negocio para aparecer en Google Maps
2. **Configurar Google Search Console** (gratis) — para ver cuántos te encuentran en Google
3. **Tomar fotos profesionales** de tu equipo, oficina, máquinas de bordado, entregas — irán en cada página
4. **Pedir reseñas en Google** a clientes actuales — esto sube tu credibilidad
5. **Configurar correos profesionales** en Zoho Mail (gratis) tipo andres@anvavi.com.mx

---

Cualquier duda sobre cómo modificar algo, pregúntame.
