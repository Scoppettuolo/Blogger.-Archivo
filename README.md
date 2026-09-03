# Archivo Multilingüe para Blogger

Widget HTML/JavaScript que genera un archivo de entradas (por año, mes y día) para cualquier blog de Blogger (Blogspot). Incluye un selector de idioma para traducir automáticamente los meses y los días de la semana.

## Características

- **Visualización jerárquica**: Años → Meses → Días → Títulos de entradas.
- **Selector de 12 idiomas**: Español, Inglés, Alemán, Francés, Italiano, Portugués, Latín, Ruso, Japonés, Chino, Coreano y Tailandés.
- **Detección automática**: Por defecto, usa el idioma configurado en tu navegador.
- **Diseño responsive**: Se adapta a móviles y tablets.
- **Sin librerías externas**: Solo HTML, CSS y JavaScript puro.

## ¿Cómo usar?

1. Ve al **Panel de control** de tu blog en Blogger.
2. Entra en **Diseño** (o **Tema** → Personalizar → Diseño).
3. Haz clic en **"Añadir un gadget"**.
4. Selecciona **"HTML/JavaScript"**.
5. Copia **todo el contenido** del archivo `blogger-archive-widget.html` y pégalo en el recuadro.
6. Guarda los cambios y visualiza tu blog.

> **Importante**: El widget funcionará automáticamente con las entradas de tu propio blog, ya que usa rutas relativas (`/feeds/posts/summary`). No necesita configurar ninguna URL manualmente.

## Tecnologías utilizadas

- **JavaScript (ES5/ES6)**: Manejo de datos y eventos.
- **JSONP**: Consume el feed público de Blogger sin necesidad de API Key.
- **CSS3**: Estilos y diseño responsivo.

## Estructura del archivo

- **HTML**: Maquetación principal y selector de idioma.
- **CSS**: Estilos visuales (colores, sombras y espaciado).
- **JavaScript**: Lógica de carga del feed, construcción del árbol de archivos y cambio de idioma.

## Límites

- El script carga las entradas de 150 en 150 (hasta 450 con las 3 llamadas incluidas). Si tu blog tiene más de 450 entradas, puedes duplicar la línea del `<script>` aumentando el `start-index`.

```html
<!-- Ejemplo para cargar más entradas -->
<script src="/feeds/posts/summary?alt=json-in-script&amp;max-results=150&amp;start-index=451&amp;callback=LoadTheArchive"></script>

---

Svasti An Scoppettuolo
KatNya
