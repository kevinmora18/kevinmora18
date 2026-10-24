# Ejemplo comentado del README de perfil

Aquí cada fragmento de la plantilla [`README.md`](README.md) va seguido de su explicación. Úsalo para enseñar en clase. Formato: **fragmento + explicación**.

---

## 1. Comentario de cabecera

```html
<!-- ✏️ EDITA: cambia el subtítulo por tu rol real -->
```

`<!-- ... -->` es un **comentario HTML**: GitHub no lo muestra en el perfil, solo se ve al editar. Lo usamos como nota para ti. Bórralos cuando ya no los necesites.

---

## 2. Título y subtítulo

```html
<h1 align="center">Bienvenidos a mi Portafolio</h1>
<h3 align="center">Desarrollador de software junior · Aprendiz SENA ADSO</h3>
```

- `<h1>` y `<h3>` son encabezados HTML (grande y mediano).
- `align="center"` los centra. Es de los pocos atributos de estilo que GitHub respeta.
- Con `#` de Markdown no se puede centrar; por eso aquí se usa HTML.

---

## 3. Banner con modo claro y oscuro

```html
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/banner.svg">
    <source media="(prefers-color-scheme: light)" srcset="assets/banner-claro.svg">
    <img alt="Banner de TU-NOMBRE: desarrollador de software" src="assets/banner.svg" width="100%">
  </picture>
</p>
```

| Parte | Qué hace |
|-------|----------|
| `<p align="center">` | Párrafo centrado que contiene la imagen |
| `<picture>` | Permite ofrecer varias imágenes alternativas |
| `<source media="(prefers-color-scheme: dark)">` | Si el visitante usa tema oscuro, carga esta imagen |
| `srcset="assets/banner.svg"` | Ruta **relativa** al archivo dentro del repo (carpeta `assets`) |
| `<img ... src=...>` | Imagen de respaldo si el navegador no entiende `<picture>` |
| `alt="..."` | Texto alternativo: accesibilidad y por si la imagen falla |
| `width="100%"` | Ocupa todo el ancho disponible |

---

## 4. Fila de badges

```html
<a href="https://github.com/TU-USUARIO?tab=followers"><img alt="Seguidores" src="https://img.shields.io/github/followers/TU-USUARIO?style=for-the-badge&logo=github&label=Seguidores"></a>
```

- `<a href>` vuelve la imagen un **enlace** (aquí a tu lista de seguidores).
- La imagen viene de **shields.io**, un servicio externo que genera el badge desde la URL.
- `github/followers/TU-USUARIO` pide el número de seguidores de ese usuario (cámbialo por el tuyo).
- Después del `?` van opciones separadas por `&`: `style=for-the-badge` (estilo grande), `logo=github` (icono) y `label=` (texto de la izquierda).

```html
<img alt="Visitas al perfil" src="https://komarev.com/ghpvc/?username=TU-USUARIO&style=for-the-badge&label=Visitas">
```

Contador de visitas de **komarev**: suma una visita cada vez que se carga la imagen. No tiene enlace porque es solo informativo.

---

## 5. Saludo y aviso

```markdown
## Hola, soy TU-NOMBRE 👋

> 📌 **Aviso:** estoy buscando mi primera oportunidad (práctica o empleo junior).
```

- `##` es un encabezado de segundo nivel; así quedan las secciones.
- `👋` es un emoji normal escrito como texto.
- `>` crea una **cita** con barra a la izquierda; sirve para avisos. `**texto**` es negrilla.

---

## 6. Sobre mí

```markdown
## 🚀 Sobre mí

Soy aprendiz del **Tecnólogo en Análisis y Desarrollo de Software del SENA** ...
```

Dos párrafos cortos separados por una **línea en blanco** (sin la línea en blanco, Markdown los junta en uno). Regla: solo cosas ciertas, sin cifras inventadas.

---

## 7. Sección desplegable

```html
<details>
<summary><b>➕ Más sobre mí</b></summary>
<br>

- 🎓 Estudiando: ...

</details>
```

- `<details>` crea un bloque que se abre y cierra con un clic.
- `<summary>` es el título visible cuando está cerrado.
- La **línea en blanco** después de `<br>` es obligatoria: sin ella GitHub no interpreta el Markdown de la lista.
- `- ` al inicio de línea crea una viñeta.

---

## 8. Tecnologías

```html
<img alt="Tecnologías: JavaScript, React, Node.js, PostgreSQL, Git" src="https://skillicons.dev/icons?i=js,react,nodejs,postgres,git">
```

- **skillicons.dev** une varios iconos en una sola imagen.
- Los nombres van tras `?i=` separados por comas. Busca los disponibles en su sitio (ej. `js`, `ts`, `py`, `html`, `css`).
- Si escribes un nombre inexistente, ese icono no sale.

```markdown
| Categoría | Tecnologías |
|-----------|-------------|
| 🎨 **Frontend** | HTML, CSS, JavaScript, React |
```

Una **tabla** de Markdown: la primera fila es el encabezado, la segunda (`|---|---|`) es obligatoria y separa; después van las filas. Las barras `|` separan columnas.

---

## 9. Mapa de proyectos

```markdown
### 🌐 Aplicaciones web
- **Proyecto Uno** — Tienda en línea de ejemplo. [Repo](https://github.com/TU-USUARIO/proyecto-uno) · [Demo](https://TU-USUARIO.github.io/proyecto-uno)
```

- `###` crea una subsección con emoji por tipo de proyecto.
- `**Nombre** — descripción` es el formato de cada viñeta.
- `[texto](url)` es un **enlace** de Markdown. Repo = código; Demo = sitio funcionando (si lo desplegaste, módulo 3).

```html
<a href="https://github.com/TU-USUARIO/proyecto-uno">
  <img src="assets/captura-ejemplo.svg" alt="Captura de pantalla del Proyecto Uno" width="480">
</a>
```

Una imagen con enlace: al hacer clic va al repo. `width="480"` limita el tamaño para que no ocupe toda la pantalla. `<sub>` escribe texto más pequeño (para el pie de la imagen).

---

## 10. Estadísticas

```html
<img alt="Estadísticas de GitHub de TU-USUARIO" height="170" src="https://github-readme-stats.vercel.app/api?username=TU-USUARIO&show_icons=true&theme=tokyonight&hide_border=true">
```

| Parámetro | Efecto |
|-----------|--------|
| `username=` | De quién se muestran los datos |
| `show_icons=true` | Muestra iconos junto a cada número |
| `theme=tokyonight` | Esquema de colores |
| `hide_border=true` | Quita el borde de la tarjeta |

La tarjeta de **racha** (`streak-stats.demolab.com`) funciona igual. Ambas son **servicios externos**: pueden fallar o cambiar. Por eso la plantilla incluye una nota de advertencia.

---

## 11. Repositorios destacados y contacto

```markdown
| Repositorio | Descripción | Tecnologías |
|-------------|-------------|-------------|
| [proyecto-uno](https://github.com/TU-USUARIO/proyecto-uno) | Tienda en línea de ejemplo | HTML, CSS, JS |
```

Tabla con enlaces dentro de las celdas. Complementa los repos fijados (pinned) de tu perfil.

```markdown
| ✉️ Correo | [tu@correo.com](mailto:tu@correo.com) |
| 💬 WhatsApp | [Escríbeme](https://wa.me/57TU-NUMERO) |
```

- `mailto:` abre el programa de correo del visitante.
- `https://wa.me/57NUMERO` abre un chat de WhatsApp (57 es el indicativo de Colombia, seguido del número sin espacios ni signos). **Publica un número solo si quieres que sea público.**

---

## 12. Cierre

```html
---

<p align="center">
  Gracias por visitar mi perfil 💚<br>
  <sub>...</sub>
</p>
```

- `---` dibuja una **línea horizontal** (con una línea en blanco antes, para que no se confunda con el título de la sección anterior).
- `<br>` es un salto de línea dentro del párrafo.

---

## Resumen de reglas de oro

1. Markdown para lo simple, HTML solo para centrar, cambiar tamaño, `<picture>` y `<details>`.
2. GitHub **ignora** CSS (`style`), JavaScript e `<iframe>`.
3. Rutas de imágenes **relativas** (`assets/...`) y nombres en minúsculas, sin espacios.
4. Siempre un `alt` descriptivo en cada imagen.
5. Línea en blanco antes y después de bloques (tablas, listas, `<details>`).
6. Reemplaza todo `TU-...` antes de publicar y no incluyas datos sensibles.

Para el paso a paso completo, vuelve a la [guía](GUIA.md).
