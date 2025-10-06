# 🌐 Portafolio Web Personal — Migración a Astro + TailwindCSS

## 🧩 1. Descripción General
Este proyecto consiste en la creación de un portafolio web personal.  
Inicialmente, se desarrolló a partir de una **plantilla base HTML/CSS**, la cual fue **personalizada** y posteriormente **migrada a Bootstrap**.  
Finalmente, se **migró a Astro con TailwindCSS**, para mejorar la organización, el rendimiento y la facilidad de mantenimiento.

---

## 🚀 2. Tecnologías utilizadas

### Etapas del proyecto
| Etapa | Tecnologías principales | Descripción |
|-------|--------------------------|--------------|
| Versión inicial | HTML5, CSS3, JS | Plantilla base brindada por el docente |
| Versión intermedia | Bootstrap 5 | Reestructuración con componentes y diseño responsive |
| Versión final | Astro, TailwindCSS | Migración completa con arquitectura modular y optimización |

---

## ⚙️ 3. Estructura del proyecto en Astro

📁 src/
┣ 📁 components/
┣ 📁 layouts/
┃ ┗ 📄 Base.astro
┣ 📁 pages/
┃ ┣ 📄 index.astro
┃ ┣ 📄 sobremi.astro
┃ ┣ 📄 proyectos.astro
┃ ┣ 📄 habilidades.astro
┃ ┗ 📄 contacto.astro
┣ 📁 styles/
┃ ┣ 📄 global.css
┃ ┣ 📄 index.css
┃ ┣ 📄 sobremi.css
┃ ┣ 📄 proyectos.css
┃ ┣ 📄 habilidades.css
┃ ┗ 📄 contacto.css
┗ 📁 public/
┃ ┣ 📁 img/
┗ otros recursos

---

## 🔧 4. Proceso de Migración

### 🔹 Paso 1: Análisis de la plantilla original
- Se revisó la estructura del HTML original (etiquetas `<header>`, `<section>`, `<footer>`).  
- Se identificaron los estilos repetidos y las partes que podían modularizarse.

### 🔹 Paso 2: Conversión a Bootstrap
- Se reemplazaron los estilos personalizados por clases de Bootstrap (`container`, `row`, `col`, `btn`, etc.).  
- Se mejoró la **adaptabilidad (responsive design)**.  
- Se mantuvo la misma paleta de colores y estructura visual.

### 🔹 Paso 3: Migración a Astro
- Se creó el proyecto Astro con el comando:
  ```bash
  npm create astro@latest

Se trasladaron las secciones del portafolio a páginas individuales (index.astro, sobremi.astro, etc.).

Se implementó un layout principal (Base.astro) para reutilizar el encabezado y pie de página.

Se configuró la carpeta public/ para alojar las imágenes del portafolio.

### 🔹 Paso 4: Integración de TailwindCSS

Instalación y configuración:

npm install -D tailwindcss
npx tailwindcss init


Se integró Tailwind con Astro añadiendo las directivas en global.css:

@tailwind base;
@tailwind components;
@tailwind utilities;


Se reemplazaron las clases de Bootstrap por utilidades de Tailwind, como:

text-center, bg-blue-600, rounded-xl, shadow-lg, etc.

Se añadieron animaciones y transiciones personalizadas para mejorar la experiencia visual.

### 🔹 Paso 5: Optimización final

Se eliminaron archivos innecesarios (JS de Bootstrap, estilos antiguos).

Se probaron las rutas y la compatibilidad en distintos dispositivos.

Se mejoró el SEO mediante el uso de metadatos en Base.astro.

## ✨ 5. Cambios principales realizados
| Elemento        | Antes (Bootstrap)                  | Después (Astro + Tailwind)                         |
| --------------- | ---------------------------------- | -------------------------------------------------- |
| Estructura HTML | En archivos html `index.html`      | Páginas separadas (`.astro`)                       |
| Estilos         | Archivos `.css` y clases Bootstrap | Clases utilitarias de Tailwind y `global.css`      |
| Navegación      | Navbar de Bootstrap                | Navbar personalizada en Astro                      |
| Animaciones     | Limitadas                          | Transiciones con `hover`, `transform`, y `animate` |
| Layout          | Manual por página                  | Reutilización con `Base.astro`                     |

## 6. Conclusiones

Astro permitió una estructura más ordenada y modular.

TailwindCSS facilitó la personalización del diseño sin necesidad de archivos CSS extensos.

La migración mejoró la velocidad de carga, la responsividad y el mantenimiento del código.

Este proceso ayudó a comprender la diferencia entre un enfoque basado en frameworks (Bootstrap) y un enfoque modular y optimizado (Astro + Tailwind).
