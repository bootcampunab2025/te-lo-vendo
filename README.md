# Te lo Vendo - Documentación del Proyecto

## Descripción General

**Te lo Vendo** es una plataforma de comercio electrónico estática desarrollada como punto de entrada para un sistema de información más completo. El proyecto implementa las mejores prácticas de desarrollo frontend con enfoque en accesibilidad, responsive design y arquitectura de código escalable.

## Objetivos del Portal

### 1. Facilitar el Comercio Digital
- Crear una plataforma intuitiva que conecte compradores y vendedores
- Proporcionar una experiencia de usuario fluida y segura
- Implementar un catálogo organizado y fácil de navegar

### 2. Experiencia de Usuario Optimizada
- Diseño responsive que funciona en todos los dispositivos
- Navegación clara e intuitiva
- Tiempos de carga rápidos y rendimiento optimizado

### 3. Accesibilidad Web
- Cumplimiento con estándares WCAG 2.1
- HTML semántico para lectores de pantalla
- Contrastes apropiados y navegación por teclado

## Arquitectura del Proyecto

### Estructura de Archivos

```
te-lo-vendo/
├── index.html                 # Página principal
├── about.html                 # Página acerca del proyecto
├── catalog.html               # Catálogo de productos
├── product-detail.html        # Ficha de producto
├── contact.html               # Página de contacto
├── src/
│   ├── css/
│   │   ├── main.css          # CSS compilado
│   │   └── main.css.map      # Source map
│   ├── sass/
│   │   ├── main.scss         # Archivo principal SCSS
│   │   ├── abstracts/
│   │   │   └── _variables.scss    # Variables globales
│   │   ├── base/
│   │   │   └── _base.scss         # Estilos base
│   │   ├── components/
│   │   │   └── _button.scss       # Componente botón
│   │   ├── layout/
│   │   │   ├── _header.scss       # Header
│   │   │   └── _container.scss    # Contenedor
│   │   └── pages/
│   │       ├── _home.scss         # Página inicio
│   │       └── _pages.scss        # Otras páginas
│   └── img/
│       ├── *.jpg             # Imágenes de productos
│       └── icons/            # Iconos SVG
└── README.md                 # Documentación
```

### Metodología CSS: BEM (Block Element Modifier)

El proyecto implementa la metodología BEM para mantener el código CSS organizado y escalable:

```scss
// Bloque
.product-card { }

// Elemento
.product-card__title { }
.product-card__price { }
.product-card__image { }

// Modificador
.product-card--featured { }
.product-card--small { }
```

#### Ventajas de BEM implementadas:
- **Modularidad**: Cada componente es independiente
- **Reutilización**: Los bloques pueden reutilizarse en diferentes contextos
- **Mantenibilidad**: Código más fácil de mantener y modificar
- **Escalabilidad**: Fácil agregar nuevos componentes sin conflictos

## Tecnologías Implementadas

### 1. HTML5 Semántico
```html
<header class="main-header">
  <nav class="navbar">
  </nav>
</header>

<main>
  <section class="hero">
  </section>
  
  <article class="product-card">
  </article>
</main>

<footer class="main-footer">
</footer>
```

**Beneficios del HTML semántico:**
- Mejor SEO y accesibilidad
- Estructura clara para lectores de pantalla
- Código más legible y mantenible

### 2. CSS/SCSS con Arquitectura Modular

#### Variables Globales
```scss
// Colores
$primary-color: #d62828;
$text-dark: #121212;
$bg-light: #ffffff;

// Espaciado
$spacing-md: 1rem;
$spacing-lg: 1.5rem;

// Breakpoints
$breakpoint-md: 768px;
$breakpoint-lg: 992px;
```

#### Componentes Reutilizables
```scss
.button {
  background-color: $primary-color;
  padding: $spacing-md $spacing-xl;
  border-radius: $border-radius-md;
  
  &--secondary {
    background-color: transparent;
    border: 2px solid $primary-color;
  }
}
```

### 3. Bootstrap 5 Integration
- Sistema de grid responsivo
- Componentes de navegación
- Utilidades para espaciado y tipografía
- Compatibilidad con estilos custom

### 4. Responsive Design

#### Breakpoints Implementados:
- **Mobile**: < 576px
- **Tablet**: 576px - 768px
- **Desktop**: 768px - 1200px
- **Large Desktop**: > 1200px

```scss
// Mobile First Approach
.hero {
  padding: 2rem 1rem;
  
  @media (min-width: $breakpoint-md) {
    padding: 4rem 2rem;
  }
  
  @media (min-width: $breakpoint-lg) {
    padding: 6rem 4rem;
  }
}
```

## Rol del Desarrollador Frontend

### Responsabilidades Principales

1. **Arquitectura de Información**
   - Diseño de la estructura de navegación
   - Organización del contenido por prioridad
   - Creación de user flows optimizados

2. **Desarrollo de Interfaz**
   - Implementación de HTML semántico
   - Desarrollo de estilos CSS con metodología BEM
   - Integración responsive para múltiples dispositivos

3. **Optimización de Rendimiento**
   - Compresión y optimización de imágenes
   - Minificación de CSS y JavaScript
   - Implementación de lazy loading

4. **Accesibilidad Web**
   - Cumplimiento de estándares WCAG 2.1
   - Etiquetado apropiado para tecnologías asistivas
   - Navegación por teclado y contrastes apropiados

5. **Testing y Compatibilidad**
   - Pruebas en múltiples navegadores
   - Validación en diferentes dispositivos
   - Testing de accesibilidad

### Decisiones Técnicas Tomadas

#### 1. Metodología BEM
**Decisión**: Implementar BEM para organización CSS
**Razón**: Escalabilidad y mantenibilidad del código
**Impacto**: Código más limpio y reutilizable

#### 2. Mobile-First Design
**Decisión**: Desarrollar primero para móviles
**Razón**: Majority of users access via mobile
**Impacto**: Mejor rendimiento en dispositivos móviles

#### 3. HTML Semántico
**Decisión**: Uso extensivo de elementos semánticos
**Razón**: Accesibilidad y SEO
**Impacto**: Mejor posicionamiento y usabilidad

#### 4. Modularización CSS
**Decisión**: Separar estilos en archivos específicos
**Razón**: Mantenibilidad y colaboración en equipo
**Impacto**: Desarrollo más eficiente

## Guía de Estilos

### Paleta de Colores
- **Primario**: #d62828 (Rojo vibrante)
- **Secundario**: #f5f5f5 (Gris claro)
- **Texto**: #121212 (Negro carbón)
- **Texto secundario**: #666 (Gris medio)
- **Fondo**: #ffffff (Blanco)

### Tipografía
- **Fuente principal**: 'Poppins', sans-serif
- **Jerarquía**: H1 (2.5rem) > H2 (2rem) > H3 (1.5rem)
- **Texto body**: 1rem, line-height 1.6

### Espaciado
- **XS**: 0.25rem (4px)
- **SM**: 0.5rem (8px)
- **MD**: 1rem (16px)
- **LG**: 1.5rem (24px)
- **XL**: 2rem (32px)

### Componentes

#### Botones
```scss
.button {
  padding: 1rem 2rem;
  border-radius: 5px;
  font-weight: 500;
  transition: all 0.3s ease;
}
```

#### Cards
```scss
.product-card {
  background: white;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}
```

## Equipo de Desarrollo

### Integrantes del Proyecto

#### Noemi Fagerstrom (@NoemiFagerstromLinck)
- **Rol**: Desarrolladora Frontend
- **Responsabilidades**: Diseño y desarrollo de interfaces de usuario, implementación de HTML semántico, arquitectura CSS con metodología BEM, optimización de experiencia de usuario.

#### Nelson Valenzuela (@soyNelsonValenzuela)
- **Rol**: Desarrollador Frontend
- **Responsabilidades**: Desarrollo de componentes interactivos, implementación de JavaScript y optimización del rendimiento de la aplicación web.

#### Patricio Barahona (@barahona-gallardo)
- **Rol**: Desarrollador Frontend
- **Responsabilidades**: Implementación responsive, accesibilidad web e integración de frameworks CSS para una experiencia de usuario óptima.

#### Juan Pablo Berrios (@MasterdjinnCL)
- **Rol**: Desarrollador Frontend
- **Responsabilidades**: Estructura de proyectos, versionado de código e implementación de buenas prácticas de desarrollo frontend.

## Cumplimiento de Requerimientos

### ✅ Requerimientos Funcionales Cumplidos

1. **Página principal con presentación y novedades**
   - ✅ Sección hero con presentación
   - ✅ Sección de novedades con últimas actualizaciones
   - ✅ Productos destacados

2. **Catálogo: listado por categorías**
   - ✅ Página de catálogo con filtros
   - ✅ Categorías: Muebles, Decoración, Iluminación
   - ✅ Funcionalidad de filtrado por JavaScript

3. **Ficha de recurso: descripción breve, imagen de portada**
   - ✅ Página de detalle de producto
   - ✅ Especificaciones completas
   - ✅ Productos relacionados

4. **Página acerca del proyecto: objetivos del portal y responsables**
   - ✅ Información completa del proyecto
   - ✅ Objetivos claramente definidos
   - ✅ Información del equipo responsable

5. **Navegación clara, amigable y responsiva**
   - ✅ Menú de navegación funcional
   - ✅ Breadcrumbs en páginas internas
   - ✅ Responsive design completo

### ✅ Requerimientos Técnicos Cumplidos

1. **Uso de HTML semántico para accesibilidad**
   - ✅ Elementos semánticos: header, nav, main, section, article, footer
   - ✅ Etiquetado apropiado para accesibilidad
   - ✅ Estructura jerárquica de headings

2. **Aplicación de metodología BEM**
   - ✅ Implementación consistente de BEM
   - ✅ Bloques, elementos y modificadores claramente definidos
   - ✅ Código CSS modular y reutilizable

3. **Representación visual con guía de estilos clara**
   - ✅ Variables CSS definidas
   - ✅ Paleta de colores consistente
   - ✅ Tipografía y espaciado estandarizados

4. **Explicación documentada del rol del desarrollador front-end**
   - ✅ Documentación completa del proyecto
   - ✅ Decisiones técnicas justificadas
   - ✅ Descripción del rol y responsabilidades

5. **Buenas prácticas en estructura de carpetas y modularización**
   - ✅ Estructura de archivos organizada
   - ✅ Separación de responsabilidades
   - ✅ Componentes modulares

## Instalación y Desarrollo

### Requisitos Previos
- Node.js (para compilación SCSS)
- Navegador web moderno
- Editor de código (VS Code recomendado)

### Instalación
```bash
# Clonar el repositorio
git clone [repository-url]

# Navegar al directorio
cd te-lo-vendo

# Instalar dependencias para compilar SCSS
npm install -g sass

# Compilar SCSS
sass src/sass/main.scss src/css/main.css --watch
```

### Estructura de Desarrollo
1. Editar archivos SCSS en `src/sass/`
2. Los cambios se compilan automáticamente a `src/css/main.css`
3. Abrir `index.html` en el navegador para ver los cambios

## Futuras Mejoras

### Fase 2: Funcionalidad Dinámica
- Implementación de carrito de compras
- Sistema de búsqueda avanzada
- Filtros dinámicos por precio y características

### Fase 3: Backend Integration
- API REST para productos
- Sistema de autenticación
- Base de datos para catálogo

### Fase 4: Optimizaciones
- Service Workers para offline functionality
- Optimización de imágenes WebP
- Implementación de CDN

## Contacto y Soporte

- Documentación: Este archivo README.md
- Código fuente: Disponible en el repositorio del proyecto

---

*Este documento será actualizado conforme el proyecto evolucione y se agreguen nuevas funcionalidades.*
