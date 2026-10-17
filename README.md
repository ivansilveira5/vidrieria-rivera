# Sitio web · Vidriería Rivera

Landing page de **una sola página**, pensada para celular, que lleva a la gente a **llamar o escribir por WhatsApp**. También sirve como página de destino para Google Ads.

* **Tecnología:** HTML + CSS + JS puro. No hay que compilar nada ni pagar hosting.
* **Peso total:** ~1 MB (la mayoría son fotos). Carga rápido aunque la señal del celular sea débil.

---

## 📁 Contenido de la carpeta

| Archivo | Para qué sirve |
| :--- | :--- |
| `index.html` | El sitio completo, con estilos y scripts dentro del mismo archivo. |
| `img/logo-vidrieria-rivera.png` | Logo oficial actualizado (insignia circular clásica pulida con monograma VR y anillo dorado). Ícono y favicon. |
| `img/*.jpg` | Fotos generadas con IA y optimizadas (ninguna pasa los 240 KB). |
| `robots.txt` / `sitemap.xml` | Indican a Google qué páginas indexar. |

---

## ✅ Antes de publicar: qué hay que editar

1. **Dominio:** buscá `vidrieriarivera.com.uy` en `index.html`, `robots.txt` y `sitemap.xml` y cambialo por el dominio que se compre. Si se usa otro, reemplazalo en todos lados.
2. **Medición (Google Ads / GA4):** en `index.html` buscá `window.VR_TRACKING` y poné los IDs reales:
   * `ADS_ID`: `AW-…` (Google Ads → Objetivos → Conversiones → Etiqueta de Google).
   * `ADS_LABEL_CALL`, `ADS_LABEL_WA`, `ADS_LABEL_FORM`: la etiqueta de cada acción de conversión (lo que va después de la `/` en `send_to`).
   * `GA4_ID`: `G-…` (opcional).
   * Mientras sigan los valores con `XXXX`, el sitio **no carga ningún script de Google**.
3. **Fotos reales (opcional):** para cambiar una foto, reemplazá el archivo en `img/` usando **el mismo nombre**. Conviene en formato horizontal 4:3, con unos 900 px de ancho.

### Eventos que se miden

| Acción del usuario | Evento (GA4 / dataLayer) | Conversión de Google Ads |
| :--- | :--- | :--- |
| Toca cualquier botón o enlace de llamada (`tel:`) | `click_llamar` | `ADS_LABEL_CALL` |
| Toca cualquier botón de WhatsApp | `click_whatsapp` | `ADS_LABEL_WA` |
| Envía el formulario de presupuesto | `envio_presupuesto` | `ADS_LABEL_FORM` |
| Toca el correo | `click_email` | — |

---

## 🚀 Cómo publicarlo gratis (elegí una opción)

### Opción A · Netlify Drop (la más fácil, 2 minutos)
1. Entrá a <https://app.netlify.com/drop>.
2. Arrastrá la carpeta **`sitio`** entera.
3. Listo: te da una dirección `https://algo.netlify.app`. Después podés conectar un dominio propio en *Domain settings*.

### Opción B · Cloudflare Pages
1. En <https://dash.cloudflare.com> andá a *Workers & Pages → Create → Pages → Upload assets*.
2. Subí la carpeta `sitio`.

### Dominio `.com.uy`
* Se registra en <https://nic.com.uy> (lo administra ANTEL). Después, en el DNS, apuntalo al hosting que elegiste (Netlify y Cloudflare te dicen exactamente qué registros cargar).

---

## 🔗 Después de publicar

1. **Google Business Profile:** agregá la URL del sitio en el campo *Sitio web* de la ficha de Maps.
2. **Google Ads:** usá la URL como *URL final* en las campañas de Búsqueda (Campaña 2 de [`GOOGLE_ADS_ESTRATEGIA.md`](../GOOGLE_ADS_ESTRATEGIA.md)) y cargá las conversiones de arriba.
3. **Search Console:** dá de alta el dominio y enviá `sitemap.xml`.
4. **Prueba rápida:** abrí el sitio en el celular y probá los botones *Llamar* y *WhatsApp* y el formulario.

---

## 📌 Datos que muestra el sitio (todos confirmados)

* Desde **1981**, con **urgencias 24 hs** (lo confirmó el cliente).
* **4,8 ★ con 65 opiniones** en Google Maps. Las 6 reseñas del sitio son textos reales y públicos, y se muestra solo el nombre con la inicial del apellido.
* Servicios: urgencias y vidrios rotos, vidrios a medida y tapas de mesa, espejos, mamparas, templado y laminado, DVH, cerramientos de aluminio. **No** se incluyen enmarcaciones ni cuadros, a pedido del cliente.
