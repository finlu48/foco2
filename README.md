
# 💡 Detras del Foco — Webzine Indie & Alternativo

> Fuera de lo mainstream. Todo sobre los mejores artistas indies y alternativos del momento.

---

## 📋 Descripción

**Detras del Foco** es un webzine estático dedicado a la música indie y alternativa. Cubre noticias, reseñas, giras y artistas emergentes que el mainstream ignora. El proyecto fue construido como ejercicio de maquetación web usando HTML semántico, CSS Grid y Flexbox.

---

## 🗂️ Estructura del proyecto

```
detras-del-foco/
├── detras-del-foco.html   # Estructura y contenido de la página
├── styles.css             # Todos los estilos visuales
└── README.md              # Este archivo
```

> ⚠️ Los dos archivos deben estar en la **misma carpeta** para que los estilos carguen correctamente.

---

## 📰 Contenido

El webzine incluye las siguientes secciones:

- **Portada** — Hero card destacado con las tres noticias principales
- **Índice** — Navegación interna hacia cada sección
- **Artículos** — Tres notas periodísticas, cada una con su aside de autor
- **Galería** — Cinco espacios para imágenes del número
- **Suscripción** — Formulario en el footer con email y checkboxes

### Artículos de esta edición (Febrero 2026)

| # | Título | Autor | Categoría |
|---|--------|-------|-----------|
| 1 | The Cure emociona al mundo alternativo con dos Grammy | Daniela Rojas | Premios |
| 2 | Peaches encabezará el cartel de The Great Escape 2026 | Marco Fuentes | Giras y Eventos |
| 3 | Shyeye lanza "Drowning" y confirma que es la artista a seguir en 2026 | Sofía Mendoza | Artistas Emergentes |

---

## 🛠️ Tecnologías utilizadas

- **HTML5** semántico (`<header>`, `<nav>`, `<main>`, `<article>`, `<aside>`, `<figure>`, `<figcaption>`, `<footer>`, `<form>`)
- **CSS3** con:
  - CSS Grid (`grid-template-areas`) para el layout principal
  - Flexbox para la navegación, mini cards y galería
  - Variables CSS (`--red`, `--yellow`, `--slate`, etc.)
  - `@media queries` para diseño responsivo
- **Google Fonts** — Anton (display) + Work Sans (cuerpo)

---

## 🎨 Paleta de colores

| Variable | Color | Uso |
|----------|-------|-----|
| `--red` | `#CC2200` | Color principal, etiquetas, acentos |
| `--black` | `#0A0A0A` | Texto y fondos oscuros |
| `--white` | `#FFFFFF` | Fondo general |
| `--yellow` | `#F5C518` | Acento cálido, bordes hero, botones |
| `--slate` | `#2E3A4E` | Cards de autor, footer, nav-btn |

---

## 🖼️ Cómo agregar imágenes

Los cuadros de imagen son placeholders que se reemplazan con una etiqueta `<img>`. Hay dos formas:

**Desde tu computador** (imagen en la misma carpeta):
```html
<img src="nombre-del-archivo.jpg" alt="Descripción"
     style="width:100%; height:200px; object-fit:cover;">
```

**Desde internet** (URL externa):
```html
<img src="https://url-de-la-imagen.jpg" alt="Descripción"
     style="width:100%; height:200px; object-fit:cover;">
```

### Placeholders disponibles

| Elemento | Clase / selector a reemplazar |
|----------|-------------------------------|
| Hero principal | `<div class="hero-placeholder">` |
| Mini card 1 (Peaches) | `<div class="mini-placeholder p1">` |
| Mini card 2 (Shyeye) | `<div class="mini-placeholder p2">` |
| Imagen artículo 1 | `<div class="art-img-placeholder a1">` |
| Imagen artículo 2 | `<div class="art-img-placeholder a2">` |
| Imagen artículo 3 | `<div class="art-img-placeholder a3">` |
| Galería foto 1–5 | `<div class="gal-img g1">` … `g5` |

---

## 📐 Layout y estructura semántica

```
<header>  ← logo + nav + portada hero
  <nav>   ← Flexbox horizontal
  <div class="portada">
    .hero-card        ← noticia destacada
    .mini-cards       ← Flexbox con 2 noticias secundarias

<div class="content-area">
  <div class="content-inner">  ← CSS Grid: indice / articles / galeria
    .indice           ← lista de navegación interna
    .articles-section
      .article-wrapper  ← CSS Grid: article (1fr) + aside (230px)
        <article>
        <aside>         ← datos estáticos del autor
    .galeria-section  ← Flexbox con flex-wrap

<footer>  ← marca + formulario de suscripción
```

---

## 📱 Responsivo

En pantallas menores a **720px**:

- El header apila logo y nav verticalmente
- Cada `article-wrapper` pasa a una sola columna (el aside va debajo del artículo)
- Las mini cards se apilan verticalmente
- El footer se reorganiza en columna

---

## ✏️ Cómo editar el contenido

Todo el texto editable está en `detras-del-foco.html`. Los estilos están centralizados en `styles.css` mediante variables CSS, por lo que cambiar un color o tipografía se hace en un solo lugar:

```css
/* styles.css — línea ~15 */
:root {
  --red:    #CC2200;
  --yellow: #F5C518;
  --slate:  #2E3A4E;
  /* etc. */
}
```

---

## 👩‍💻 Autores del proyecto

| Rol | Nombre |
|-----|--------|
| Diseño y desarrollo | Equipo Detras del Foco |
| Redactora jefe | Daniela Rojas |
| Corresponsal festivales | Marco Fuentes |
| Redactora emergentes | Sofía Mendoza |

---

*© 2026 Detras del Foco — Webzine independiente · Hecho con ruido y pasión*
